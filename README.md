# 🐢 mini_turtle_oo

## Ejercicio 2 – Programación Orientada a Objetos

Este proyecto implementa una versión de la tortuga usando **Programación Orientada a Objetos (POO)** en Python. A diferencia del ejercicio anterior, el estado de la tortuga se encapsula dentro de una clase, permitiendo crear múltiples tortugas con comportamientos independientes.

---

## 📁 Estructura del proyecto

```text
mini_turtle_oo_task/
├── mini_turtle_oo/
│   ├── __init__.py
│   └── turtle_class.py
└── main.py
```

---

## 🧩 Clase principal de la tortuga

### 📄 Archivo: `turtle_class.py`

En este archivo se define la clase `Tortuga`, la cual encapsula el estado y los comportamientos del movimiento.

```python
class Tortuga:
    def __init__(self):
        # Estado encapsulado (antes era global)
        self.espacios = ""

    def adelante(self, pasos):
        """
        Dibuja el movimiento horizontal de la tortuga hacia la derecha.
        """
        print(self.espacios + "- " * pasos + ">")
        self.espacios += "  " * pasos

    def abajo(self, pasos):
        """
        Dibuja el movimiento vertical de la tortuga hacia abajo.
        """
        linea_vertical = self.espacios + "|\n"
        print(linea_vertical * pasos, end="")

    def reiniciar(self):
        """
        Reinicia la posición de la tortuga.
        """
        self.espacios = ""
        print("Tortuga reiniciada")
```

---

## 📦 Inicialización del paquete

### 📄 Archivo: `__init__.py`

Este archivo permite importar la clase `Tortuga` directamente desde el paquete.

```python
from .turtle_class import Tortuga

__all__ = ["Tortuga"]
```

---

## ▶️ Ejecución del programa

### 📄 Archivo: `main.py`

En este archivo se crean varias instancias de la clase `Tortuga` para demostrar que cada una mantiene su propio estado.

```python
from mini_turtle_oo import Tortuga

# Crear dos tortugas independientes
t1 = Tortuga()
t2 = Tortuga()

# Tortuga 1
t1.adelante(5)
t1.abajo(2)
t1.adelante(5)

print("\n--- Cambio de tortuga ---\n")

# Tortuga 2 (estado independiente)
t2.adelante(3)
t2.abajo(1)

print("\n--- Reinicio tortuga 1 ---\n")

t1.reiniciar()
t1.adelante(2)
t1.abajo(1)
```

---

### ✅ Resultado en consola

![Resultado mini\_turtle\_oo](https://github.com/user-attachments/assets/76ab789d-a78a-49bc-b47e-79b392ab2824)

---

## 📝 Conclusión

El ejercicio **mini_turtle_oo** demuestra las ventajas de la Programación Orientada a Objetos, como la encapsulación del estado y la creación de múltiples instancias independientes. Este enfoque mejora la organización del código, su reutilización y escalabilidad, facilitando el mantenimiento y la comprensión del prog
