
![image](https://github.com/user-attachments/assets/4ab599b0-aa18-4e04-bb2f-f13024891c98)

class Triangulo:
    def __init__(self, lado1, lado2, lado3):
        self.lado1 = lado1
        self.lado2 = lado2
        self.lado3 = lado3
    
    def imprimir_lado_mayor(self):
        lado_mayor = max(self.lado1, self.lado2, self.lado3)
        print(f"El lado con el tamaño mayor es: {lado_mayor}")

    def tipo_triangulo(self):
        if self.lado1 == self.lado2 == self.lado3:
            tipo = "equilátero"
        elif self.lado1 == self.lado2 or self.lado2 == self.lado3 or self.lado1 == self.lado3:
            tipo = "isósceles"
        else:
            tipo = "escaleno"
        print(f"El triángulo es {tipo}.")

# Ejemplo de uso
# Crear una instancia de la clase Triangulo con lados específicos
triangulo = Triangulo(2, 55, 50)

# Imprimir el valor del lado con un tamaño mayor
triangulo.imprimir_lado_mayor()

# Imprimir el tipo de triángulo
triangulo.tipo_triangulo()
