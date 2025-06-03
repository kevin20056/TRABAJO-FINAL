Algoritmo MenuCompleto
	Definir opcion, edad, calif, n1, n2, n3, mayor, dia, num, suma Como Entero
    Definir dias Como Cadena
    
    Repetir
        Escribir "=== MENÚ PRINCIPAL ==="
        Escribir "1. Verificar mayor de edad"
        Escribir "2. Verificar aprobación"
        Escribir "3. Encontrar el mayor de 3 números"
        Escribir "4. Mostrar día de la semana"
        Escribir "5. Sumar números ingresados"
        Escribir "6. Salir"
        Escribir "Seleccione una opción (1-6):"
        Leer opcion
        
        Segun opcion Hacer
            1:
                Escribir "Ingrese su edad:"
                Leer edad
                Si edad >= 18 Entonces
                    Escribir "Es mayor de edad"
                Sino
                    Escribir "Es menor de edad"
                FinSi
                
            2:
                Escribir "Ingrese calificación (0-10):"
                Leer calif
                Si calif >= 6 Entonces
                    Escribir "APROBADO"
                Sino
                    Escribir "REPROBADO"
                FinSi
                
            3:
                Escribir "Ingrese tres números:"
                Leer n1, n2, n3
                
                mayor <- n1
                Si n2 > mayor Entonces
                    mayor <- n2
                FinSi
                Si n3 > mayor Entonces
                    mayor <- n3
                FinSi
                Escribir "El número mayor es: ", mayor
                
            4:
                Escribir "Ingrese número de día (1-7):"
                Leer dia
                
                dias <- "Lunes,Martes,Miércoles,Jueves,Viernes,Sábado,Domingo"
                
                Si dia >1 Y dia <= 7 Entonces
                    Escribir "El día es: ", Subcadena(dias, (dia-1)*9+1, dia*9)
                Sino
                    Escribir "Número de día inválido"
					
                FinSi
                
            5:
                suma <- 0
                Repetir
                    Escribir "Ingrese número (0 para terminar):"
                    Leer num
                    suma <- suma + num
                Hasta Que num = 0
                Escribir "La suma total es: ", suma
                
            6:
                Escribir "Saliendo del programa..."
                
            DeOtroModo:
                Escribir "Opción no válida. Intente nuevamente."
        FinSegun
        
        Escribir "" // Salto de línea
        
    Hasta Que opcion = 6
FinAlgoritmo
