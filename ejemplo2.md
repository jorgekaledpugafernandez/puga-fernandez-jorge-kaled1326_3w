![image](https://github.com/user-attachments/assets/278644f9-39f5-4d07-ab7c-69a4ec849c0d)
print("puga fernandez jorge kaled_3w")
print(" ")

class Persona:
    def __init__(self, nombre, edad):
        self.nombre = nombre
        self.edad = edad
    
    def mostrar_datos(self):
        print(f"Nombre: {self.nombre}")
        print(f"Edad: {self.edad}")
    
    def es_mayor_de_edad(self):
        if self.edad >= 18:
            print(f"{self.nombre} es mayor de edad.")
        else:
            print(f"{self.nombre} no es mayor de edad.")

# Ejemplo de uso
persona1 = Persona("j.puga", 16)

persona1.mostrar_datos()
persona1.es_mayor_de_edad()

