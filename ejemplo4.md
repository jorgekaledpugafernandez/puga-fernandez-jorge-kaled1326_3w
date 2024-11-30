![image](https://github.com/user-attachments/assets/dc83a8f0-5e84-4094-ab5c-591c6fea9bb5)
print("puga fernnadez jorge kaled_3w")
print(" ")

class Calculadora:
    def __init__(self):
        self.valor1 = int(input("Ingrese el primer valor entero: "))
        self.valor2 = int(input("Ingrese el segundo valor entero: "))
    
    def sumar(self):
        return self.valor1 + self.valor2
    
    def restar(self):
        return self.valor1 - self.valor2
    
    def multiplicar(self):
        return self.valor1 * self.valor2
    
    def dividir(self):
        if self.valor2 != 0:
            return self.valor1 / self.valor2
        else:
            return "No se puede dividir por cero"

# Crear una instancia de la clase Calculadora
calculadora = Calculadora()

# Realizar y mostrar los cálculos
print(f"Suma: {calculadora.sumar()}")
print(f"Resta: {calculadora.restar()}")
print(f"Multiplicación: {calculadora.multiplicar()}")
print(f"División: {calculadora.dividir()}")



