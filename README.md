# mini_turtle_oo

EJERCIO 2

mini_turtle_oo_task (carpeta)

mini_turtle_oo (carpeta)

turtle_class.py (archivo)

class Tortuga:
    def _init_(self):
        # Estado encapsulado (antes era global)
        self.espacios = ""

    def adelante(self, pasos):
        print(self.espacios + "- " * pasos + ">")
        self.espacios += "  " * pasos

    def abajo(self, pasos):
        linea_vertical = self.espacios + "|\n"
        print(linea_vertical * pasos, end='')

    def reiniciar(self):
        self.espacios = ""
        print("Tortuga reiniciada")

_init_.py (archivo)

from .turtle_class import Tortuga

_all_ = ["Tortuga"]


main.py (archivo)

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

### ✅ Solución en Python

<img width="601" height="311" alt="image" src="https://github.com/user-attachments/assets/76ab789d-a78a-49bc-b47e-79b392ab2824" />
