carreras: tuple[str, ...] = (
    "Ingeniería de Software",
    "Contabilidad",
    "Derecho"
)

personas: list[tuple[str, str, int, int]] = [
    # nombre, apellido, edad, carrera
]

estudiantes: list[dict[str, str | int]] = [
    # Lista de diccionario con nombre, apellido, edad, carrera
]

for _ in range(5):
    nombre = input("Ingrese el nombre: ")
    apellido = input("Ingrese el apellido: ")
    edad = int(input("Ingrese la edad: "))
    carrera = int(input(
        "Ingrese la carrera (0: Ingeniería de Software, "
        "1: Contabilidad, 2: Derecho): "
    ))

    persona = (nombre, apellido, edad, carrera)
    personas.append(persona)

    print("")

for persona in personas:
    nombre = persona[0]
    apellido = persona[1]
    edad = persona[2]
    carrera = carreras[persona[3]]

    estudiante = {
        "nombre": nombre,
        "apellido": apellido,
        "edad": edad,
        "carrera": carrera
    }

    estudiantes.append(estudiante)

for estudiante in estudiantes:
    print(
        f"{estudiante['nombre']} {estudiante['apellido']} "
        f"tiene {estudiante['edad']} años y estudia "
        f"{estudiante['carrera']}"
    )
