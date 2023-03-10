# Segundo Bimestre
## 17.1.2023
Clase de retroalimentación del primer bimestre donde buscamos encontrar los puntos donde, tanto la clase como los estudiaantes, podrían mejorar. Para esto
usamos Mentimeter.
## Librerías de terceros
Clase variada donde observamos la manera de importar librerías y clases personalizadas a nuestro Workspace de Java, especialmente en el área de GUI, importando temas 
y aplicándolos sobre nuestros programas en su GUI.
## Interfaz
Es el comportamiento de las clases, obligandolas a adoptar dicho comportamiento.

![image](https://user-images.githubusercontent.com/42527062/224433213-dee56d84-4252-45ad-a3fc-4eb5009f20b4.png)

## Relaciones en UML

Todas las variables deben tener el mismo nombre en UML que en el codigo.

-Relación bidireccional: nos sirve para cuando necesitamos implementar una clase que tiene una conexión necesaria en ambos casos, ambas son propiedades mutuas.

-Relación direccional: nos sirve para denotar cuando una clase es la que puede contener a otra clase como propiedad.

-Bidireccional con multiplicidad: como la original pero la cantidad de datos de la segunda clase es grande, usualmente necesita de listas de clase.

![image](https://user-images.githubusercontent.com/42527062/221737399-4cba687d-2830-4623-b8d4-7ffbe802dbd9.png)

## Base de datos
Clase de como guardar informacion en bases de datos y los casos de uso donde son utiles, cada base de dato posee su propio lenguaje. En este caso se usará principalmente SQLITE.
![image](https://user-images.githubusercontent.com/42527062/224433480-fd6d217b-a0c8-46a4-b93c-23008b7337db.png)

### Programación de la base de datos
> Un ejemplo de la sintaxis de SQL
```sql
/**
*   pat_mic : 20.ene.2k23
*   script de base de datos
CRUD
CREATE  --> Insert
READ    --> leer
UPDATE  --> actu+alziar
DELETE  --> borrar
*/

-- revisar el entorno de trabajo
.version
.database
.show

.tables

DROP TABLE PERSONA;
DROP TABLE MascotaTipo;


CREATE TABLE MascotaTipo
(
    IdMascotaTipo   INTEGER PRIMARY KEY AUTOINCREMENT,
    Nombre          VARCHAR(10) NOT NULL,
    Estado          VARCHAR(1) NOT NULL DEFAULT('A')
);

CREATE TABLE Sexo 
(
    IdSexo INTEGER  NOT NULL PRIMARY KEY AUTOINCREMENT
    ,Nombre         VARCHAR (100)
    ,Estado         VARCHAR(1) NOT NULL DEFAULT('A')
);

-- JOSUE PERALTA LLENE TABLA SEXO
INSERT INTO Sexo (NOMBRE) VALUES ("HEMBRA");
INSERT INTO Sexo (NOMBRE) VALUES ("MACHO");
INSERT INTO Sexo (NOMBRE) VALUES ("SIN SEXO");
select * from sexo;
--Jonathan Luzuriaga :v y los copiones 
CREATE TABLE Mascota
(
     IdMascota       INTEGER PRIMARY KEY AUTOINCREMENT
    ,IdMascotaTipo   INTEGER NOT NULL
    ,IdSexo          INTEGER NOT NULL
    ,Nombre          VARCHAR (100) NOT NULL
    ,Edad            INTEGER NOT NULL
    ,Estado          VARCHAR(1) NOT NULL DEFAULT('A')
)
--Gabriel Jaya (Marca Registrada)
INSERT INTO Mascota(IdMascotaTipo, IdSexo, Nombre, Edad)            VALUES (1,2,"Luzu",4);
INSERT INTO Mascota(IdMascotaTipo, IdSexo, Nombre, Edad)            VALUES (2,1,"Eva",2);
INSERT INTO Mascota(IdMascotaTipo, IdSexo, Nombre, Edad, Estado)    VALUES (2,2,"Dani",3,'X');

-- Sebastian Guerra (No copiar // Derechos Registrados // Cualquier intento de copia sera denunciado ante la ley)

INSERT INTO Mascota (IdMascotaTipo, IdSexo, Nombre, Edad, Estado) VALUES  (1, 1, "Pepe", 3, 'A');
INSERT INTO Mascota ( IdMascotaTipo, IdSexo, Nombre, Edad, Estado) VALUES ( 1, 2, "Poliperro", 2, 'A');
INSERT INTO Mascota ( IdMascotaTipo, IdSexo, Nombre, Edad, Estado) VALUES ( 1, 3, "Poliperro2", 6, 'B');

-- Estefano Proaño

INSERT INTO Mascota (IdMascotaTipo, IdSexo, Nombre, Edad) VALUES (1,1,"Nala", 2);
INSERT INTO Mascota (IdMascotaTipo, IdSexo, Nombre, Edad) VALUES (2,2,"Coco", 2);
INSERT INTO Mascota (IdMascotaTipo, IdSexo, Nombre, Edad) VALUES (3,2,"Simba", 2);

-- Luis Rocha (No copiar // Derechos Registrados // Cualquier intento de copia sera denunciado ante la ley)
INSERT INTO Mascota(IdMascotaTipo, IdSexo, Nombre, Edad, Estado      ) VALUES (3,1, "Davicho", 19);
INSERT INTO Mascota(IdMascotaTipo, IdSexo, Nombre, Edad, Estado      ) VALUES (1,3, "Luchito", 21);
INSERT INTO Mascota(IdMascotaTipo, IdSexo, Nombre, Edad, Estado      ) VALUES (12,1, "Pepito", 9);

-- David Quille
INSERT INTO Mascota(IdMascotaTipo, IdSexo, Nombre, Edad, Estado      ) VALUES (3,1, "juancho", 9);
INSERT INTO Mascota(IdMascotaTipo, IdSexo, Nombre, Edad, Estado      ) VALUES (5,3, "lupita", 2);
INSERT INTO Mascota(IdMascotaTipo, IdSexo, Nombre, Edad, Estado      ) VALUES (1,1, "toño", 9);

-- Emilio Armas
INSERT INTO Mascota(IdMascotaTipo, IdSexo, Nombre, Edad, Estado      ) VALUES (1,1, "Raya", 4);
INSERT INTO Mascota(IdMascotaTipo, IdSexo, Nombre, Edad, Estado      ) VALUES (3,1, "Dory", 1);
INSERT INTO Mascota(IdMascotaTipo, IdSexo, Nombre, Edad, Estado      ) VALUES (5,2, "Rocky",8);

-- Anthony Morales 
INSERT INTO MASCOTA (IdMascotaTipo, IdSexo, Nombre, Edad, Estado     ) VALUES (1,2, "MalumaBaby", 6)
INSERT INTO MASCOTA (IdMascotaTipo, IdSexo, Nombre, Edad, Estado     ) VALUES (2,1, "Anuel", 3)
INSERT INTO MASCOTA (IdMascotaTipo, IdSexo, Nombre, Edad, Estado     ) VALUES (5,2, "Mufasa", 9)

-- Damaris Suquillo
INSERT INTO Mascota (IdMascotaTipo, IdSexo, Nombre, Edad, Estado    ) VALUES  (9, 1, "Lucy", 3);
INSERT INTO Mascota ( IdMascotaTipo, IdSexo, Nombre, Edad, Estado   ) VALUES  (10, 2, "Lupe", 2);
INSERT INTO Mascota ( IdMascotaTipo, IdSexo, Nombre, Edad, Estado   ) VALUES  (11, 3, "Chico", 6, 'X');

-- ANAEL MOLINA
INSERT INTO Mascota (IdMascotaTipo, IdSexo,Nombre, Edad, Estado) VALUES(40,1, "Bruno",2,'X');
INSERT INTO Mascota (IdMascotaTipo, IdSexo,Nombre, Edad, Estado) VALUES(45,2, "Akira",1);
INSERT INTO Mascota (IdMascotaTipo, IdSexo,Nombre, Edad, Estado) VALUES(45,2, "Qucky",7);
-- Josue Peralta
--Gabriel Jaya (Marca Registrada)
INSERT INTO Mascota(IdMascotaTipo, IdSexo, Nombre, Edad)            VALUES (1,2,"ROCKY",4);
INSERT INTO Mascota(IdMascotaTipo, IdSexo, Nombre, Edad)            VALUES (2,2,"DAMARIS",2);
INSERT INTO Mascota(IdMascotaTipo, IdSexo, Nombre, Edad, Estado)    VALUES (2,2,"A",2);
--Mercedes Martinez 

INSERT INTO Mascota(IdMascotaTipo, IdSexo, Nombre, Edad, Estado      ) VALUES (12,1, "Oso", 4,'B');
INSERT INTO Mascota(IdMascotaTipo, IdSexo, Nombre, Edad, Estado      ) VALUES (14,1, "Pepe", 5,'A');
INSERT INTO Mascota(IdMascotaTipo, IdSexo, Nombre, Edad, Estado      ) VALUES (15,1, "Nino", 6, 'A');

-- Alejo Aleman "Sex Enjoyer"

INSERT INTO Mascota (IdMascotaTipo, IdSexo, Nombre, Edad) VALUES (1,1,"ElPepe", 2);
INSERT INTO Mascota (IdMascotaTipo, IdSexo, Nombre, Edad) VALUES (2,2,"C", 2);
INSERT INTO Mascota (IdMascotaTipo, IdSexo, Nombre, Edad) VALUES (3,2,"Simba", 2);

INSERT INTO MascotaTipo ( Nombre, Estado)  VALUES ( "Perros", "A");  
INSERT INTO MascotaTipo ( Nombre)          VALUES ( "Gatos");
INSERT INTO MascotaTipo ( Nombre)          VALUES ( "Peces");
INSERT INTO MascotaTipo ( Nombre)          VALUES ( "Cuyes");
INSERT INTO MascotaTipo ( Nombre)          VALUES ( "Leona");
--DELETE FROM MascotaTipo WHERE IdMascotaTipo > 9;
SELECT * from MascotaTipo;

UPDATE MascotaTipo SET Estado = "X" 
WHERE IdMascotaTipo in (6,12);

SELECT * from MascotaTipo 
WHERE Nombre like '%e%';


-- DROP TABLE T1;
-- DROP TABLE T2;

INSERT INTO PERSONA (ID,    NOMBRE,     APELLIDO)   VALUES  (1, "Pepe ",  "perez");
INSERT INTO PERSONA (ID,    NOMBRE,     APELLIDO)   VALUES  (2, "Ana",  "Suarez");
INSERT INTO PERSONA (ID,    NOMBRE,     APELLIDO)   VALUES  (3, "Juan",  "Sanchez");
INSERT INTO PERSONA (ID,    NOMBRE,     APELLIDO)   VALUES  (4, "Lucas Juan",  "Montalvo");

SELECT ID,    NOMBRE,     APELLIDO FROM PERSONA;

SELECT ID,    NOMBRE,     APELLIDO 
FROM PERSONA
WHERE ID = 2;

SELECT ID,    NOMBRE,     APELLIDO 
FROM PERSONA
WHERE NOMBRE LIKE '%JUAN%';

----------------------------------------------
CREATE TABLE PET
(
    ID          INTEGER PRIMARY KEY,
    NOMBRE      VARCHAR(10),
    EDAD        INTEGER 
);
--DROP TABLE PET;
INSERT INTO PET (ID,    NOMBRE,     EDAD)   VALUES  (1, "VALUMA", 1);
INSERT INTO PET (ID,    NOMBRE,     EDAD)   VALUES  (2, "JUANA",  2);
INSERT INTO PET (ID,    NOMBRE,     EDAD)   VALUES  (3, "COMOTU", 3);
SELECT * FROM PET;
------------------------------------------------
```
En este caso creamos una tabla de mascotas usando varias tablas de forma concatenada.
## UML + Asociacion cardinal
![image](https://user-images.githubusercontent.com/42527062/224434394-b77e3264-e49f-4b61-98d9-4ee857647072.png)
Usar 1..* significa que empezamos desde 1 hasta un numero mayor de esta clase.
![image](https://user-images.githubusercontent.com/42527062/224434477-d13d2b05-b3dc-44e4-a9a9-6e8206a7771f.png)
El rombo nos indica la composicion, significando que el constructor para el objeto es ahora obligatorio.
Java no posee doble herencia.
## Automatas finitos
Se nos dio por ultimo una clase rapida de un automata finito y determinista siendo el ejemplo el de una maquina expendedora de comida donde los estados de la misma son alcanzables por medio del ingreso, que en este caso son monedas. Estos estados siendo el valor total que ha sido ingresado en la maquina.
```c++
#include <iostream>
using namespace std;

int const TKErr=-1;         // Token de Error
int const TKFin=-2;         // Token de Fin
string const ALFA[] = {"25","50","s","\\t"};

int **newMatriz(int f, int c)
{    
    int **m=NULL;
    m = new int*[f];
    for (int i = 0; i < f; i++)
        m[i] = new int[c];

    return m;
}

void showMatriz(int **pd, int f,int c)
{
    for (int i = 0; i < f; i++)
    {
            for (int j = 0; j < c; j++)
                cout<< pd[i][j] <<"\t";   
            cout<< endl;
    }
}

int getIndexAlfabeto(string str)
{
    //int index = ALFA.find(c);
    for (int i = 0; i < sizeof(ALFA) / sizeof(ALFA[0]); i++) 
        if (ALFA[i] == str) 
            return i;
    return TKErr;    
}

int main( void) 
{
/*  Automata finito determinista : Cobra un dolar $1

                         _ _ _ _ _ _ _  50   _ _ _ _ _ _ _  
                       |                                  |
    [q0] --- $25 ---> [q1]  --- $25 ---> [q2]  --- $25 ---> [q3]  --- $25 ---> [[q4]] 
    |                                      |                                     |
    |  _ _ _ _ _ _ _  $50  _ _ _ _ _ _ _ _ |  _ _ _ _ _ _   $50  _ _ _ _ _ _ _ _ | 


     _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ 
     Q     |  { 25          50         ' '  }
     _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ 
     0     |    1           2           er         
     1     |    2           3           er
     2     |    3           4           er
     3     |    4           er          er
     4     |    er          er          ok
     _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ 

*/
    int **mt=NULL;         // mt =  matriz de transicion
    int Q=5, L=3;
    mt = newMatriz(Q,L);
    
    //matriz de transicion [Q][L]
    mt[0][0]= 1;     mt[0][1]= 2;      mt[0][2]= TKErr;
    mt[1][0]= 2;     mt[1][1]= 3;      mt[1][2]= TKErr;
    mt[2][0]= 3;     mt[2][1]= 4;      mt[2][2]= TKErr; 
    mt[3][0]= 4;     mt[3][1]= TKErr;  mt[3][2]= TKErr; 
    mt[4][0]= TKErr; mt[4][1]= TKErr;  mt[4][2]= TKFin; 
    //showMatriz(mt,Q,L);
    
    //string palabra[] = {"25","25","25","25","s"};
    int q=0, l=0;
    string moneda;
    cout <<endl << "Ingresa un $1 en monedas de 25 y 50 centavos"  <<endl;
    do
    {
        cout<< "(s para salir) >> Ingresa una moneda: ";
        cin >> moneda;
        l = getIndexAlfabeto(moneda);
        q = mt[q][l];

        //cout<< "\t" + moneda << q <<","<< l <<endl;
        if(q == TKErr || q > Q){
            cout<<">> Error, devolviendo tu dinero" <<endl;
            exit(0);
        }
        if(q == TKFin){
            cout<<">> OK, recibe tu gaseosa" <<endl;
            exit(0);
        }
    }while (true);
}
```
> A este codigo se lo tradujo a Java y se le aumento estados y entradas.
```java
import java.util.Scanner;

public class App {
    public static final int TKFin2 = -3;    //papas exacto
    public static final int TKFin = -2;     //cola exacto
    public static final int TKErr = -1;     //falta de dinero
    public static final String ALFA[]={"5","10","25","50","s","\\t"};
    public static void main(String[] args) throws Exception {
        int[][] mt= new int[21][5];
        mt[0][0]= 1;     mt[0][1]= 2;      mt[0][2]= 5; 	mt[0][3]= 10;    mt[0][4]= TKErr;
        mt[1][0]= 2;     mt[1][1]= 3;      mt[1][2]= 6;     mt[1][3]= 11;    mt[1][4]= TKErr;
        mt[2][0]= 3;     mt[2][1]= 4;      mt[2][2]= 7;     mt[2][3]= 12;    mt[2][4]= TKErr;
        mt[3][0]= 4;     mt[3][1]= 5;      mt[3][2]= 8;     mt[3][3]= 13;    mt[3][4]= TKErr;
        mt[4][0]= 5;     mt[4][1]= 6;      mt[4][2]= 9;     mt[4][3]= 14;    mt[4][4]= TKErr;
        mt[5][0]= 6;     mt[5][1]= 7;      mt[5][2]= 10;    mt[5][3]= 15;    mt[5][4]= TKErr;
        mt[6][0]= 7;     mt[6][1]= 8;      mt[6][2]= 11;    mt[6][3]= 16;    mt[6][4]= TKErr;
        mt[7][0]= 8;     mt[7][1]= 9;      mt[7][2]= 12;    mt[7][3]= 17;    mt[7][4]= TKErr;
        mt[8][0]= 9;     mt[8][1]= 10;     mt[8][2]= 13;    mt[8][3]= 18;    mt[8][4]= TKErr;
        mt[9][0]= 10;    mt[9][1]= 11;     mt[9][2]= 14;    mt[9][3]= 19;    mt[9][4]= TKErr;
        mt[10][0]= 11;   mt[10][1]= 12;    mt[10][2]= 15;   mt[10][3]= 20;   mt[10][4]= TKFin2;
        mt[11][0]= 12;   mt[11][1]= 13;    mt[11][2]= 16;   mt[11][3]= 20;  mt[11][4]= TKErr;
        mt[12][0]= 13;   mt[12][1]= 14;    mt[12][2]= 17;   mt[12][3]= 20;  mt[12][4]= TKErr;
        mt[13][0]= 14;   mt[13][1]= 15;    mt[13][2]= 18;   mt[13][3]= 20;  mt[13][4]= TKErr;
        mt[14][0]= 15;   mt[14][1]= 16;    mt[14][2]= 19;   mt[14][3]= 20;  mt[14][4]= TKErr;
        mt[15][0]= 16;   mt[15][1]= 17;    mt[15][2]= 20;   mt[15][3]= 20;  mt[15][4]= TKErr;
        mt[16][0]= 17;   mt[16][1]= 18;    mt[16][2]= 20;   mt[16][3]= 20;  mt[16][4]= TKErr;
        mt[17][0]= 18;   mt[17][1]= 19;    mt[17][2]= 20;   mt[17][3]= 20;  mt[17][4]= TKErr;
        mt[18][0]= 19;   mt[18][1]= 20;    mt[18][2]= 20;   mt[18][3]= 20;  mt[18][4]= TKErr;
        mt[19][0]= 20;   mt[19][1]= 20;    mt[19][2]= 20;      mt[19][3]= 20;  mt[19][4]= TKErr;
        mt[20][0]= 20;   mt[20][1]= 20;       mt[20][2]= 20;         mt[20][3]= 20;  mt[20][4]= TKFin;

        int q=0,l=0;
        String moneda;
        Scanner sc=new Scanner(System.in);
        System.out.println("Ingresa $1 o 50 centavos en monedas de 5, 10, 25 y 50 centavos. !Cuidado! La maquina NO da vuelto");
        do{
            System.out.println("(s para salir) >> Ingresa una moneda: ");
            
            moneda=sc.nextLine();
            l=getIndexAlfabeto(moneda);
            q=mt[q][l];
            if(q==TKErr){
                System.out.println("Error, inicie de nuevo");
                System.exit(0);
            } 
            if(q==TKFin){
                System.out.println("Ok, toma tu cola");
                System.exit(1);
            }
            if(q==TKFin2){
                System.out.println("Ok, toma tu papita.");
                System.exit(1);
            }
        }while(true);
    }

    public static void showMatriz(int[][] pd, int f, int c){
        for(int i=0;i<f;i++){
            for(int j=0;j<c;j++)
                System.out.println(pd[i][j]);
            System.out.println();
        }
    }

    public static int getIndexAlfabeto(String str){
        for(int i=0;i<ALFA.length;i++)
            if(str.equals(ALFA[i])){
                return i; 
            }
        return TKErr;
    }
}
```
Con su grafo correspondiente siendo:
![Diag](https://user-images.githubusercontent.com/42527062/224436443-aa37cda3-769d-41e2-a68b-5027597d8133.png)
