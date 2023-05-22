# Metodo-de-matriz-JavaScript
Los métodos de arrays en JavaScript son funciones predefinidas que se pueden aplicar a los objetos de tipo array para realizar diversas operaciones. Estos métodos permiten agregar, eliminar, modificar, buscar y transformar elementos dentro de un array de manera eficiente. 

A contiunacion, definiiremos cada uno de los metodos, sus sintaxis, ejemplos y una situacion en el que podriamos aplicarlo dentro de una aplicacion.

# includes()

Se utiliza para verificar si un array contiene un determinado elemento y devuelve un valor booleano (true o false) según el resultado de la búsqueda.

Sintaxi:
    array.includes(elemento)

Ejemplo:

    var numeros = [1, 2, 3, 4, 5];
    var incluyeTres = numeros.includes(3);
    // incluyeTres es true

    var incluyeDiez = numeros.includes(10);
    // incluyeDiez es false

Situacion: Qué hay en la tienda

Usaremos el método includes para buscar un elemento en un arreglo. arreglo.includes() devolverá true o false dependiendo de si el elemento se encuentra.

     let productosExistentes = [
          'camisa',
          'televisor',
          'plancha',
          'radio',
          'celulares',
          'ventilador',
          'libros',
      ];

      let listaCompras = [
          'zapato',
          'camisa',
          'libros'
      ];


      for (producto of listaCompras){
          console.log(producto + ':' + productosExistentes.includes(producto));
      };


Utilizamos el método .includes() con un for loop para verificar si cada elemento en el arreglo listaCompras se puede encuentran en el arreglo productosExistentes.

Resultado:

    zapato:false
    camisa:true
    libros:true


# indexOf()

Se utiliza para obtener el índice de la primera aparición de un elemento especificado en un array. Devuelve el índice del elemento si se encuentra en el array, y -1 si el elemento no está presente.

Sintaxis:

    array.indexOf(elemento)

Ejemplo:

    var frutas = ['manzana', 'plátano', 'naranja'];
    var indiceManzana = frutas.indexOf('manzana');
    // indiceManzana es 0

    var indicePera = frutas.indexOf('pera');
    // indicePera es -1
    
Utilizaremos el método indexOf para encontrar el número de indice de nuestra fruta favorita.

    let frutas = ['manzana', 'plátano', 'naranja'];

    let favorita = 'naranja';
    
    let frutaFavorita = frutas.includes(favorita) ? frutas.indexOf(favorita) : 'No se encuentra en la lista';
    console.log('Posicion:', frutaFavorita);
    
Dentro de la variable frutaFavorita, obtenemos el indice de nuestra fruta que deseamos, primeramente verificamos si existe dentro de la lista, para posteriormente obtener su indice, en caso contrario nos arrojara una mensaje que no se encuentra en la lista;


# findLastIndexOf()

Se utiliza para encontrar el índice del último elemento en un array que cumple con una condición especificada. Retorna el índice del último elemento que satisface la condición de una función de prueba proporcionada, o -1 si no se encuentra ningún elemento que cumpla con la condición.
