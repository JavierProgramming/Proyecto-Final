Proyecto-Final
# Se define el precio base inicial
precio_base = 2000

# Se solicita cotizaciones hasta que el usuario ingrese "Salir"
while True:
    respuesta = input("¿Desea cotizar un seguro? (Ingrese 'Salir' para terminar): ")
    
    if respuesta.lower() == "salir":
        print("Gracias por utilizar nuestro servicio de cotización. ¡Hasta luego!")
        break
    
    # Se solicitan los datos del asegurado
    nombre_asegurado = input("Ingrese el nombre del asegurado: ")
    edad_asegurado = int(input("Ingrese la edad del asegurado: "))
    cantidad_hijos = int(input("Ingrese la cantidad de hijos del asegurado: "))
    cantidad_propiedades = int(input("Ingrese la cantidad de propiedades del asegurado: "))
    salario_asegurado = float(input("Ingrese el salario del asegurado: "))

    # Se calcula el recargo por cada hijo (20% sobre el precio base por cada hijo)
    recargo_por_hijo = 0.20 * precio_base * cantidad_hijos
    
    # Se calcula el recargo por cada propiedad (35% de la cotización por propiedad)
    recargo_por_propiedad = 0.35 * precio_base * cantidad_propiedades
    
    # Se calcula el recargo por salario (5% sobre el salario del asegurado)
    recargo_por_salario = 0.05 * salario_asegurado
    
    # Se calcula el precio total de la cotización sumando los recargos al precio base
    precio_total = precio_base + recargo_por_hijo + recargo_por_propiedad + recargo_por_salario

    # Se muestra el precio total de la cotización del seguro
    print("Cotización para", nombre_asegurado)
    print("Precio base:", precio_base)
    print("Recargo por hijo:", recargo_por_hijo)
    print("Recargo por propiedad:", recargo_por_propiedad)
    print("Recargo por salario:", recargo_por_salario)
    print("Precio total de la cotización del seguro:", precio_total)


Aquí hay una solución modificada del programa que cumple con los requisitos adicionales:

python
Copy code
# Se define el precio base inicial
precio_base = 2000

# Se solicita cotizaciones hasta que el usuario ingrese "Salir"
while True:
    respuesta = input("¿Desea cotizar un seguro? (Ingrese 'Salir' para terminar): ")
    
    if respuesta.lower() == "salir":
        print("Gracias por utilizar nuestro servicio de cotización. ¡Hasta luego!")
        break
    
    # Se solicitan los datos del asegurado
    nombre_asegurado = input("Ingrese el nombre del asegurado: ")
    edad_asegurado = int(input("Ingrese la edad del asegurado: "))
    cantidad_hijos = int(input("Ingrese la cantidad de hijos del asegurado: "))
    cantidad_propiedades = int(input("Ingrese la cantidad de propiedades del asegurado: "))
    salario_asegurado = float(input("Ingrese el salario del asegurado: "))

    # Se calcula el recargo por cada hijo (20% sobre el precio base por cada hijo)
    recargo_por_hijo = 0.20 * precio_base * cantidad_hijos
    
    # Se calcula el recargo por cada propiedad (35% de la cotización por propiedad)
    recargo_por_propiedad = 0.35 * precio_base * cantidad_propiedades
    
    # Se calcula el recargo por salario (5% sobre el salario del asegurado)
    recargo_por_salario = 0.05 * salario_asegurado
    
    # Se calcula el precio total de la cotización sumando los recargos al precio base
    precio_total = precio_base + recargo_por_hijo + recargo_por_propiedad + recargo_por_salario

    # Se muestra el precio total de la cotización del seguro
    print("Cotización para", nombre_asegurado)
    print("Precio base:", precio_base)
    print("Recargo por hijo:", recargo_por_hijo)
    print("Recargo por propiedad:", recargo_por_propiedad)
    print("Recargo por salario:", recargo_por_salario)
    print("Precio total de la cotización del seguro:", precio_total)
El funcionamiento del programa consiste en solicitar al usuario que ingrese los datos del asegurado (nombre, edad, cantidad de hijos, cantidad de propiedades y salario), calcular los recargos adicionales según la cantidad de hijos y propiedades, así como el salario del asegurado, y finalmente mostrar el precio total de la cotización del seguro. El programa continuará solicitando cotizaciones hasta que el usuario ingrese la palabra "Salir".

Para mejorar el programa, se podría agregar validación de datos para asegurarse de que el usuario ingrese valores válidos, manejar posibles errores de entrada del usuario de manera más robusta y modularizar el código para hacerlo más legible y mantenible. Además, se podría agregar documentación y comentarios más detallados para facilitar la comprensión del código.
