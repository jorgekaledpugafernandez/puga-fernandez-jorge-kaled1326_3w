# puga-fernandez-jorge-kaled1326_3w
![image](https://github.com/user-attachments/assets/c360b153-f1c2-48b4-9d5a-b219d17a16c7)

print("PUGA FERNANDEZ JORGE KALED_3W")
print(" ")

class Alumno:
    def __init__(self, nombre, nota):
        self.nombre = nombre
        self.nota = nota
    
    def imprimir_datos(self):
        print(f"Nombre: {self.nombre}")
        print(f"Nota: {self.nota}")
    
    def resultado(self):
        if self.nota >= 6:
            print(f"{self.nombre} ha aprobado con una nota de {self.nota}.")
        else:
            print(f"{self.nombre} ha reprobado con una nota de {self.nota}.")

# Ejemplo de uso
alumno1 = Alumno("j.puga", 8)

alumno1.imprimir_datos()
alumno1.resultado() 


