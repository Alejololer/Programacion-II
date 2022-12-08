# Programación II
## Carlos Alejandro Aleman Osorio
### 23.11.2022 Algoritmia
Ciencia de estudios de los algoritmos y estos últimos nos sirven para solucionar problemas.
Dentro de esta ciencia tenemos el pseudocódigo, los diagramas de flujo, el código y el trace junto al debug.
> Diagramas de flujo

El óvalo sirve para demostrar el inicio, el trapezoide la entrada el usuario, el rectángulo los procedimientos, el rombo un condicional, además de otras formas para representar los mensajes al usuario, etc.

>Ejemplo: Determine el > de 2#
```java
    public class MayorNum{
        public static void main(){
            int a=20,b=10;
            if(a>b){
                System.out.print("a es el numero mayor");
            } else if(a==b){
                System.out.print("Son iguales");
            } else{
                System.ot.print("b es el numero mayor");
            }
        }
```
Realizando todo este proceso acompañado el tracing, creando tablas de tabulación.
>Error, bug y issue

Un error es algo fatal, que causa que el programa se cierre totalmente.
Un bug es un hueco que se aprovecha de una función o procedimiento mal diseñada para causar problemas en el programa.
Un issue es un problema no tan fatal que a pesar de dañar el programa sigue funcionando.

### 7.12.2022
Sobrecarga
```java
    private static int suma(int a,int f){
        return a+f;
    }
    private static float suma(int a,float f){
        return a+f;
    }
    private static float suma(float a,float f){
        return a+f;
    }
    private static float suma(float a,int f){
        return a+f;
    }
```
## Programación orientada a objetos
Tenes uno clase, que al usar New se crea una nueva instancia
entonces, los objetos se crean en la memoria ram.

En Public Class Name tenemos un ámbito, un método y una
propiedad.

En ámbitos podemos tener:
-public
-private 
-protect/friend

