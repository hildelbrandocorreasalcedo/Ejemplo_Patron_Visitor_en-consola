# Ejemplo_Patron_Visitor_en-consola
Ejemplo del Patron Visitor en consola C#

Diagrama UML el Patron Visitor (Visitante)
![uml patron visitor](https://user-images.githubusercontent.com/63067085/227310550-5d945ca4-58be-40b3-bc46-41bb17f31842.png)

- Propósito del Patron Visitor (Visitante)

* Representa una operación sobre los elementos de una estructura de objetos. Permite definir una nueva operación sin cambiar las clases de los elementos sobre los que opera.
* Es una forma de separar el algoritmo de la estructura de un objeto.

- Aplicabilidad del Patron Visitor (Visitante)

* Una estructura de objetos contiene muchas clases de objetos con diferentes interfaces, y queremos realizar operaciones sobre esos elementos que dependen de su clase concreta.
* Se necesita realizar muchas operaciones distintas y no relacionadas sobre objetos de una estructura de objetos y no se desea contaminar sus clases con estas operaciones
* Las clases que definen las estructuras de objetos rara vez cambian, pero muchas veces queremos definir nuevas operaciones sobre la estructura.
* Utiliza el patrón Visitor cuando necesites realizar una operación sobre todos los elementos de una compleja estructura de objetos

- Cómo implementarlo el Patron Visitor (Visitante)

1) Declara la interfaz visitante con un grupo de métodos “visitantes”, uno por cada clase de elemento concreto existente en el programa.
2) Declara la interfaz de elemento. Si estás trabajando con una jerarquía de clases de elementos existente, añade el método abstracto de “aceptación” a la clase base de la jerarquía. 
3) Implementa los métodos de aceptación en todas las clases de elementos concretos.
4) Las clases de elemento sólo deben funcionar con visitantes a través de la interfaz visitante. Los visitantes, sin embargo, deben conocer todas las clases de elemento concreto, referenciadas como tipos de parámetro de los métodos de visita.
5) Por cada comportamiento que no pueda implementarse dentro de la jerarquía de elementos, crea una nueva clase concreta e implementa todos los métodos visitantes.

