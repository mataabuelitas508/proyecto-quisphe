agenda = {}

def mostrar_menu():
    print("\n--- AGENDA PERSONAL ---")
    print("1. Agregar evento")
    print("2. Ver eventos")
    print("3. Eliminar evento")
    print("4. Salir")

def agregar_evento():
    fecha = input("Ingresa la fecha (YYYY-MM-DD): ")
    evento = input("Descripción del evento: ")

    if fecha in agenda:
        agenda[fecha].append(evento)
    else:
        agenda[fecha] = [evento]
    
    print(" Evento agregado.")

def ver_eventos():
    if not agenda:
        print(" No hay eventos registrados.")
        return

    print("\n Eventos en tu agenda:")
    for fecha in sorted(agenda):
        for i, evento in enumerate(agenda[fecha], start=1):
            print(f"{fecha} - {i}. {evento}")

def eliminar_evento():
    ver_eventos()
    fecha = input("\nIngresa la fecha del evento a eliminar (YYYY-MM-DD): ")

    if fecha in agenda:
        for i, evento in enumerate(agenda[fecha], start=1):
            print(f"{i}. {evento}")
        try:
            num = int(input("Número del evento a eliminar: "))
            if 1 <= num <= len(agenda[fecha]):
                eliminado = agenda[fecha].pop(num - 1)
                if not agenda[fecha]:
                    del agenda[fecha]
                print(f"🗑 Evento eliminado: {eliminado}")
            else:
                print("Número inválido.")
        except ValueError:
            print("Entrada inválida.")
    else:
        print("No hay eventos en esa fecha.")

# Bucle principal
while True:
    mostrar_menu()
    opcion = input("Selecciona una opción (1-4): ")

    if opcion == "1":
        agregar_evento()
    elif opcion == "2":
        ver_eventos()
    elif opcion == "3":
        eliminar_evento()
    elif opcion == "4":
        print(" ¡Hasta luego!")
        break
    else:
        print("Opción no válida.")
