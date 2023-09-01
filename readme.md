# Triangulo rectangulo

Este es un programa simple para imprimir distintos triangulos rectangulos

## Pseudocódigo

//Aplicacion para Imprimir triangulos rectangulos


Algoritmo Triangulo_rectangulo
    Definir num como entero
    Escribir "Ingrese un número entero positivo:"
    Leer num
	
	Si num >= 0 Entonces
	
    Escribir "Elija el tipo de triángulo rectángulo:"
    Escribir "1. Triángulo rectángulo con base a la izquierda"
    Escribir "2. Triángulo rectángulo con base a la derecha"
    Escribir "3. Triángulo rectángulo con base arriba"
    Escribir "4. Triángulo rectángulo con base abajo"
    Escribir "Seleccione una opción:"
    Leer eleccion
	
    Segun eleccion Hacer
        1:
            para i desde 0 hasta num - 1 con paso 1 Hacer
                para j desde 0 hasta i con paso 1 Hacer
                    Escribir Sin Saltar "* "
                FinPara
                Escribir ""
            FinPara
        2:
            para i desde 0 hasta num - 1 con paso 1 Hacer
                para espacio desde 0 hasta num - 2 - i con paso 1 Hacer
                    Escribir Sin Saltar "  "
                FinPara
                para j desde 0 hasta i con paso 1 Hacer
                    Escribir Sin Saltar "* "
                FinPara
                Escribir ""
            FinPara
        3:
            para i desde num - 1 hasta 0 con paso -1 Hacer
                para j desde 0 hasta i con paso 1 Hacer
                    Escribir Sin Saltar "* "
                FinPara
                Escribir ""
            FinPara
        4:
            para i desde 0 hasta num - 1 con paso 1 Hacer
                para espacio desde 0 hasta i con paso 1 Hacer
                    Escribir Sin Saltar "  "
                FinPara
                para j desde i hasta num - 1 con paso 1 Hacer
                    Escribir Sin Saltar "* "
                FinPara
                Escribir ""
            FinPara
        De Otro Modo:
            Escribir "Opción no válida."
    Fin Segun
	
SiNo
	Escribir "Número no valido."
FinSi

FinAlgoritmo 


## C++

//Aplicacion para Imprimir triangulos rectangulos

#include <iostream>

using namespace std;

int main() {
    int num;
    cout << "Ingrese un numero entero positivo:";
    cin >> num;
    
    if (num >= 0) {
        cout << "Elija el tipo de triangulo rectangulo:" << endl;
        cout << "1. Triangulo rectangulo con base a la izquierda" << endl;
        cout << "2. Triangulo rectangulo con base a la derecha" << endl;
        cout << "3. Triangulo rectangulo con base arriba" << endl;
        cout << "4. Triangulo rectangulo con base abajo" << endl;
        cout << "Seleccione una opcion:";
        
        int eleccion;
        cin >> eleccion;
        
        switch (eleccion) {
            case 1:
                for (int i = 0; i < num; i++) {
                    for (int j = 0; j <= i; j++) {
                        cout << "* ";
                    }
                    cout << endl;
                }
                break;
           case 2:
               for (int i = 0; i < num; i++) {
                   for (int espacio = 0; espacio < num - 1 - i; espacio++) {
                      cout << "  ";
                      }
                   for (int j = 0; j <= i; j++) {
                      cout << "* ";
                      }
                   cout << endl;
                }
                break;

            case 3:
                for (int i = num - 1; i >= 0; i--) {
                    for (int j = 0; j <= i; j++) {
                        cout << "* ";
                    }
                    cout << endl;
                }
                break;
            case 4:
                for (int i = 0; i < num; i++) {
                    for (int espacio = 0; espacio < i; espacio++) {
                        cout << "  ";
                    }
                    for (int j = i; j < num; j++) {
                        cout << "* ";
                    }
                    cout << endl;
                }
                break;
            default:
                cout << "Opcion no valida." << endl;
                break;
        }
    } else {
        cout << "Numero no valido." << endl;
    }

    return 0;
}

## Python
 

//Aplicacion para Imprimir triangulos rectangulos

def main():
    num = int(input("Ingrese un numero entero positivo: "))
    
    if num >= 0:
        print("Elija el tipo de triangulo rectangulo:")
        print("1. Triangulo rectangulo con base a la izquierda")
        print("2. Triangulo rectangulo con base a la derecha")
        print("3. Triangulo rectangulo con base arriba")
        print("4. Triangulo rectangulo con base abajo")
        eleccion = int(input("Seleccione una opcion: "))
        
        if eleccion == 1:
            for i in range(num):
                for j in range(i + 1):
                    print("* ", end="")
                print()
        elif eleccion == 2:
            for i in range(num):
                for espacio in range(num - 1 - i):
                    print("  ", end="")
                for j in range(i + 1):
                    print("* ", end="")
                print()
        elif eleccion == 3:
            for i in range(num, 0, -1):
                for j in range(i):
                    print("* ", end="")
                print()
        elif eleccion == 4:
            for i in range(num):
                for espacio in range(i):
                    print("  ", end="")
                for j in range(i, num):
                    print("* ", end="")
                print()
        else:
            print("Opcion no valida.")
    else:
        print("Numero no valido.")

if __name__ == "__main__":
    main()




