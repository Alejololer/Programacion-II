# Programación II
## Carlos Alejandro Aleman Osorio
### 23.11.2022 Algoritmia
Ciencia de estudios de los algoritmos y estos últimos nos sirven para solucionar problemas.
Dentro de esta ciencia tenemos el pseudocódigo, los diagramas de flujo, el código y el trace junto al debug.
> Diagramas de flujo
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/3d/LampFlowchart_es.svg/1200px-LampFlowchart_es.svg.png" width="30%">


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
![image](https://user-images.githubusercontent.com/42527062/211204415-4c3b38ae-3844-42af-85a6-eb931909c282.png)

## Programación orientada a objetos
Tenemos una clase, que al usar New se crea una nueva instancia
entonces, los objetos se crean en la memoria ram.

En Public Class Name tenemos un ámbito, un método y una
propiedad.

En ámbitos podemos tener:
-public
-private 
-protect/friend
>Ejemplo
```java
    public class CreditCard{
        Protect String nrotar;
        Public String nombprop;
        public boolean retirar(string code){
            return true;
        }
    }
```
### Herencia
Es el proceso donde una superclase comparte sus atributos y metodos a una subclase, siendo un ejemplo:

```java
    public class Padre{
        Private String nombre;
        Private Int edad;
        public void dormir(){
        }
        public void comer(){
        }
    }
```
Si usamos la palabra "extends" en la subclase, este adquiriria los atributos y los metodos de la clase Padre.
```java
    public class Hijo extends Padre{
    }
```
![image](https://user-images.githubusercontent.com/42527062/211204447-8efeffe1-1de3-4ef6-998d-981a3e7c2d55.png)

Ya poseeria nombre, edad, dormir, correr y podria utilizarlos.
>Es importante saber que ambas clases deben estar en el mismo paquete.
### Interface
Es una manera de compartir y crear una especie de plantilla para clases, se declara de la manera:

```java
    public interface EjemploInterfaz(){
    //Cuerpo de la interfaz
    }
```
Para implementarse en una clase se usa la palabra "implements".
```java
    public class Ejemplo implements EjemploInterfaz(){
    //Cuerpo de la clase
    }
```
Para realizar una herencia multiple podemos usar la jerarquia de clases.

![image](https://user-images.githubusercontent.com/42527062/211204509-d6a27aec-e75c-4089-a7bd-3e6cc4732974.png)

### GUI
En cuanto a GUI solo se va a realizar una rapida explicacion del uso de Jframe, este es una clase de una utilidad de Java para poder crear y modificar las propiedades de una ventana.

```java
    import javax.swing.*;
    public class Ventana
    {
        public static void main( String[] args ) 
        {
            JFrame miVentana = new JFrame( "Mi Ventana" );
            miVentana.setDefaultCloseOperation( JFrame.EXIT_ON_CLOSE);
            miVentana.setSize( 300, 200 );
            miVentana.setVisible( true );
            
            ImageIcon image=new ImageIcon("logo.png");
            frm.setIconImage(image.getImage());
            frm.getContentPanel().setBackground(new Color(12,111,54);
            
        }   //fin del método main
    }   //fin de la clase ventana
```
Los botones son igualmente una clase ya creada en las utilidades de Java, siendo la clase JButton.

```java
    public class Botones
    {
        public static void main( String[] args ) 
        {
            JButton btnP1=new JButton("Panel 1");
            JButton btnP2=new JButton("Panel 2");
            JButton btnP2=new JButton("Panel 2");
        }   //fin del método main
    }   //fin de la clase Botones
```
### Workshop
Realizamos un trabajo grupal basado en la creación de una red social para mascotas llamada Tinder Pets, debíamos hacer que sea totalmente funcional con la capacidad de hacer matches entre mascotas, el resultado de mi grupo fue subido a github al siguiente link: https://github.com/emilioale04/TinderPetLover
El trabajo no fue totalmente completo debido a la falta de tiempo pues nos hubiera gustado añadirle algunas features extra para que el programa se sienta completo, aún así el programa base es totalmente funcional y tiene todas las features solicitadas en el 
