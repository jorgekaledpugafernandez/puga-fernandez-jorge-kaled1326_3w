![image](https://github.com/user-attachments/assets/95b7a623-eef1-4728-beda-5648d40294a0)
![image](https://github.com/user-attachments/assets/bc3c74a4-a8b9-4979-9ffa-0f65bb55fcb9)
![image](https://github.com/user-attachments/assets/2aad059c-d66e-4284-8ede-976d7578d9d4)

class Contacto:
    def __init__(self, nombre, telefono, email):
        self.nombre = nombre
        self.telefono = telefono
        self.email = email

    def __str__(self):
        return f"Nombre: {self.nombre}, Teléfono: {self.telefono}, Email: {self.email}"

class Agenda:
    def __init__(self):
        self.contactos = []

    def anadir_contacto(self):
        nombre = input("Ingrese el nombre: ")
        telefono = input("Ingrese el teléfono: ")
        email = input("Ingrese el email: ")
        contacto = Contacto(nombre, telefono, email)
        self.contactos.append(contacto)
        print("Contacto añadido con éxito.\n")

    def lista_contactos(self):
        if not self.contactos:
            print("La agenda está vacía.\n")
        else:
            for contacto in self.contactos:
                print(contacto)
            print()

    def buscar_contacto(self):
        nombre = input("Ingrese el nombre del contacto a buscar: ")
        encontrado = False
        for contacto in self.contactos:
            if contacto.nombre.lower() == nombre.lower():
                print(contacto)
                encontrado = True
                break
        if not encontrado:
            print("Contacto no encontrado.\n")

    def editar_contacto(self):
        nombre = input("Ingrese el nombre del contacto a editar: ")
        for contacto in self.contactos:
            if contacto.nombre.lower() == nombre.lower():
                contacto.telefono = input(f"Ingrese el nuevo teléfono para {contacto.nombre} (actual: {contacto.telefono}): ")
                contacto.email = input(f"Ingrese el nuevo email para {contacto.nombre} (actual: {contacto.email}): ")
                print("Contacto actualizado con éxito.\n")
                return
        print("Contacto no encontrado.\n")

    def cerrar_agenda(self):
        print("Cerrando agenda...")
        exit()

# Función principal
def main():
    agenda = Agenda()
    while True:
        print("1. Añadir contacto")
        print("2. Lista de contactos")
        print("3. Buscar contacto")
        print("4. Editar contacto")
        print("5. Cerrar agenda")
        opcion = input("Seleccione una opción: ")
        if opcion == '1':
            agenda.anadir_contacto()
        elif opcion == '2':
            agenda.lista_contactos()
        elif opcion == '3':
            agenda.buscar_contacto()
        elif opcion == '4':
            agenda.editar_contacto()
        elif opcion == '5':
            agenda.cerrar_agenda()
        else:
            print("Opción no válida. Por favor, seleccione una opción del 1 al 5.\n")

# Ejecutar el programa
if __name__ == "__main__":
    main()
