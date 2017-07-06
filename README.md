# My main project

## Description

This *project* is a **demo** of how to write text with ***markdown***

Done in [SkylabCoders](http://www.skylabcoders.com/es)

![Random Image](http://tuspuzzles.es/puzzles/original/atardecer-568470fbef6d4.jpg)

- Item 1
- Item 2 
- Item 3
    + SubItem1
    + SubItem2
        * SubSubItem1
        * SubSubItem2

The function sum will return the `sum` of 2 numbers
```
function sum(a,b){
    return a + b;
}
sum(3,4) // 7
```

# cd Change directory

# ls Mostar archivos

# ls -la Mostrar archivos en detalle

```
Deberes:
    Configurar el terminal para abrir directamente sublime desde el terminal de mac.
```

# Sistema de control de versiones
Es muy importante ser capaces de controlar los cambios, al trabajar con mucho codigo y archivos es muy importante tener el control de los cambios.

Sirve para controlar las versiones o cambios que hacemos en nuestros documentos con la finalidad de tener un control de ellos y tener siempre una versión inicial, para ello utilizaremos GIT.

Para eliminar git hemos de processar en consola el comando **rm -rf .git** . Estamos con rf forzando el borrado de la carpeta oculta con extensión git, ergo borramos git.

Podemos observar todos los comandos de git tecleando en consola **git help** .

Para trackear los cambios añadimos todos los archivos que queremos guardar los cambios y los estamos pasando a **Staging Area**. Una vez en Staging Area tenemos todos nuestros archivos con los pertinentes cambios hacemos **commit** y pasan a estar guardados en el repositorio local como una nueva versión, con su respectivo nombre y fecha.

Para **pasar el archivo de Staging Area al local repository** hacemos **git commit -m "index created"** (con -m lo que hacemos es darle un comentario a cada cambio).

Hacinedo **git log** podemos ver todos los commit realizados. Haciendo **git log --stat** nos esta dando más info que git log dandonos la cantidad de líneas creadas.
```
Para crear un archivo vacío lo podemos hacer mediante el comando touch my-file.txt por ejemplo.
```

Para linkear el repositorio local de git con un repositorio de github lo hacemos mediante:
```
git remote add origin https://github.com/ddmarin94/notes-bootcamp.git
```

Hacemos git diff para ver los cambios que vamos a trackear cuando ya tenemos el archivo en track con los cambios sin guardar ergo sin hacer commit.

**git dift**

Cuando hacemos **git remote -v** podemos ver los repositorios remotos definidos en esa carpeta.

Si hacemos **git push origin master** conseguimos sincronizar el repositorio local con el repositorio remoto.

En caso de hacer **git push -u origin master** las siguientes veces no tendremos que hacer git push origin master.

### Día 2

**Cuando hagamos git commit sin el -m"**y sin el comentario" se nos abre bin. Es bastante complicado de utilizar y se usa mediante comandos. Lo mehor para salir de aquí es usar el comando: **git: escape y escribimos el comando que es q!**.

Como recuperar versiones anteriores de archivos mediante git:

Para volver a un estado anterior utilizamos el comando **git checkout**. Podemos volver a un punto determinado de varias maneras, la mas sencilla es usar el **identificador de cada commit** (que lo vemos cuando hemos hecho git log). Para ello hacemos git log vemos todas las versiones que hay y entonces hacemos **git checkout y añadimos todo el codigo del commit.** 

Cuando hagamos git checkout master nos vuelve al último checkout de branch o rama. 

### Que es Javascript:

Es un lenguaje de programación.
Es interpretado y no compilado, existe una maquina intermedia que lo traduce.
Puede ser ejecutado tanto en navegador como en servidor.
Usa el estandard ECMAScript.
```
Javascript se encarga del comportamiento. Distinguimos tres capas principales las cuales son:
Content - HTML
Design - CSS
Behaviour _ JS
```

Al haber un standard como ECMAScript se establecen las pautas y especificaciones del lenguaje de programación Javascript. Se establecen las reglas como por ejemplo para declarar una variables escribir var x = 10;.

En cambio TypeScript es un pseudo-lenguaje de programación. Es como una versión ampliada de JS, no se puede ejecutar en un navegador. Si queremos trabajar en Typescript se ha de compilar previamente antes de ejecutarlo. El proceso de compilación detecta errrores de tipo y da mucha info, de manera que el JS final al que se ha convertido ha pasado diversos checkeos o controles. 

##Que es Ajax##
AJAX es Asynchronus Javascript XML. Aunque aparece XML nosotros lo utilizaremos mediante JSON. 

##Primitibe and data types##
Number
String
Boolean
Undefinied
Null

##Type of
Con type of ejecutandolo en la consola nos revela el tipo de datos que estamos manejando.

## Trabajando con booleans:


## AND Operator ##

true && true      → true
true && false     → false
false && true     → false
false && false    → false

## OR Operator ##

true || true      → true
true || false     → true
false || true     → true
false || false    → false 

##Functions Scope:

El scope de las variables se define a nivel de función y no a nivel de bloque.

```
function checkAge(){
    
    var age = 30

    if (age >= 20){
        console.log('Young');
    }else{
        console.log('Old');
    }
}
```

Las variables de definen a nivel de función, para toda la funcion y no para nivel de bloque. A nivel de bloque no estamos refiriendo a que no declararemos una variable llamada a en un if.

La visibilidad de las variables queda definida por las funciones. Desde fuera de una funció no puedo acceder a las variables de dentro de una función. Pero las variables de fuera de una función si pueden ser visibles des de dentro de una función. En este caso estamos hablando de variables globales.

**Simplificando de dentro de una función podemos acceder a una variable de fuera pero de fuera acceder a una variable de dentro de una función no es posible.**

```
    scope local = variable dentro de función.
    scope global = variable fuera de funciones.
```

Diferenciamos así entre **scope local** es decir de dentro de una función y **scope global** donde podemos apreciar variables fuera de una función a las que podemos acceder a nivel interno de una función.

```
var newAge = 50; // En este caso esto es una variable global a la que podemos acceder desde dentro de cualquier función.

function checkAge(){
    
    var age = 30 // En este caso estamos declarando una función a la que solo podemos acceder des de dentro de nuestra función checkAge.

    if (age >= 20){
        console.log('Young');
    }else{
        console.log('Old');
    }
}
```

Las funciones pueden ser definidas mediante un nombre o bien una función anonima puede ser asignada a una varibale.

```
 var sum = function(a,b) {return a + b}

 Esta es una funcion anónima a la que se le asigna una variable y su callback se realizará mediante la variable que tiene asignada ergo sum();
```

```
function sum(a,b) {return a + b}
 En este caso estamos hablando de una variable que tiene asignado un nombre.

```

## IFE Immediately-invoked function expression:

## Function callback
**Cuando pasamos una función a como argumento de otra funcion b y b ejecuta a decimos que a es una función callback**. En este caso **one() y two()** son una función callback.

Esto nos permite pasarle cualquier parametro a invoke_and_add(one, two); y nos los va a ejecutar. Si lo modificamos y hacemos **function three() {return 3;} //3**  **invoke_and_add(one, three); // 4** nos va a devolver 4.

Invoke an add nos va a ejecutar siempre ambas funciones. Funcionará con cualquier tipo de funciones que nosotros le pasemos como parametro. Así como si le pasamos una función anonima como: **invoke_and_add(one,function(){return 23}); // 4**

Ejemplo: 
```
function invoke_and_add(a,b){
    return a+b;
}

function one() {return 1;} //1
function two() {return 2;} //2

invoke_and_add(one, two); // 3

function three() {return 3;} //3

invoke_and_add(one, three); // 4

```

En este caso si ejectuamos **one() devuelve uno**, si ejecutamos **two() devuelve 2** y si ejecutamos **invoke_and_add(one,two) nos devuelve 3**.

Cuando hablamos de una funcion dentro de otra función. Esta ultima puede acceder a las variables de su función superior que le envuelve, y podrá acceder a las variables globales fuera de la función que la envuelve.

En cambio des de fuera de ambas funciones no podremos acceder a las variables que tienen en su interior.

Si defino una función n dentro de una función f:

```
function f(){
    var b = 1;
    function n(){
        var x = 5;
    }
}

```

La n tendra acceso a las variables de la funcion padre y a la vez a las variables de la función del padre del padre. Se produce el encadenamiento de scope. 

En este caso:

```
    function f1(){ var a = 1; return f2();}
    function f2(){ return a;}
    f1()
```

Podemos ver dos funciones totalmente independientes, la función f1 esta ejecutando la función f2 a la vez que declara la variable a. Esta variable a no es global sino que es local.

La función f2 nos esta devolviendo el valor de a, este valor no esta definido puesto que a nivel local la variable a no esta establcida al igual que a nivel global tampoco esta definida.

**Por lo cual nos aparece el error de que a no esta definida.**

En el siguiente ejemplo:

```
 var a = 123;
 function f() {
    alert(a);
    var a = 1;
    alert(a);
 }
 f();
```

Cualquier uso que haga de a dentro de f va a ser una a local. Hay dos momentosdistintos puesto que en f hay una variable local a y el primero de ellos nos devolverá undefined puesto que a no tiene valor. En cambio en el segundo alert a nos devolverá el alert de 1, puesto que tiene prioridad ante la var a global.

Las variables las podemos definir siempre al principio de una función. Esta buena práctica es conocida como: **hoisting**.

###Dia 3

##Lexical scope:
Las variables a las que puede acceder queda definido cuando creamos el scope. 
Ejemplo:

```
    var a = 10;

    function one_() {
        var a = 1;
        return a;
    }
```

Tenemos una a global y una a local. A la que definimos la "A" local tiene preferencia sobre la global por lo que el scope es local.

En el siguiente caso:

```
    var a = 10;

    function one_() {
        var a 
        return a;
    }
```

En este caso nos devuelve indefinido. Al tener la a local que es la que tiene preferencia y no tiene valor establecido.

En el siguiente caso:

```
    var a = 10;
    function one_() {
        return a;
    }
```

En este caso nos devuelve a que esta definidia de manera global.

En el siguiente caso:

```
    var a = 10;
    function one_() {
        var a = 500
        return a;
    }
    var z = one();
    return z
```

En este caso nos devolvera 500 ya que la a local con valor a 500 prevalece frente a la global y posteriormente es llamada la función one() que guarda el valor en z y ese valor vuelve a ser 500, por el mismo motivo, prevalece el valor de la "A" local.

```
    var a = 10;
    function one_() {
         a = 500
        return a;
    }
    var z = one();
    return z
```

El "A" que no tiene var asignado estamos diciendo que esa variable es GLOBAL. En este caso tendremos dos var "A", la a = 500 es global pasaria a posicionarse encima de var a = 10. primero leeriamos var a = 500, luego var a = 10 y luego entrariamos en la funcion donde a = 500, cogeria este ultimo valor en el momento de ejecutar la función.

##Scope chain:


###Arrays

Para crear una array usamos [].

Un ejemplo de array:

```
var array = [1,2,3,4];
```

Tambien podemos crear una array vacia y posteriormente llenarla, como en el siguiente ejemplo:


```
var array = [];
array[0] = 'david'
array[1] = 'true'
array[2] = funcion(){return 1}
array[3] = { name: 'David'}
```

El array puede contener diferentes tipos de datos como en el siguiente ejemplo. Tambien podemos llenar un array vacía mediante el metodo **push()**.

Un array tambien puede contener diversas arrays, por ejemplo:

```
var array = [ [1,2,3,4,5], [1,2,3,4,5] ]
```

Si hicieramos array.length obtendriamos 2 puesto que estamos obteniendo el lenght del array que lo engloba todo.

En canvio si quisieramos saber el length de la primera parte del array deberiamos hacer:

```
array[0].lenght // Obtendriamos el lenght del array que esta en la posición 0 de array.
```

###Objetos

Tenemos el siguiente objeto:

```
var hero = {
    type : 'turtle',
    name : 'donatelo',
}
```

Podemos acceder a este objeto a través de hero[type] por ejemplo y accederiamos a type. En ningún caso podemos tratarlo como array puesto que no lo es y si hicieramos hero[0] no nos devolvería ningun resultado.

Un objeto puede contener diversos datos como:

```
 var hero = {
    type: 'turtle',
    name : 'donatelo',
    age : 23,
    brother: {
        name : 'Angelo',
        age: 30,
    }
 }

```

Para acceder al siguiente objeto podemos hacer lo siguiente:

```
    hero.type // turtle
    hero.name // donatelo
    hero.brother.name // Angelo
```

Tambien podriamos incorporar una función en un objeto de la siguiente manera:

```


```

En la siguiente funcion podemos crear un objeto, le pasamos dos parametros a una función que posteriormente nos los devuelve en forma de objetos:

```
function getData(name, location){
    return{
        you: name,
        city: location,
    }
}
```


Tambien podemos hacer lo mismo de la siguiente manera:

```
function skylabcoders(location, classroom){
    this.place = location
    this.group = classroom
}

var me = new skylabcoders('poblenou', 'Abbey Road');

```

En caso de no poner la particula new en var me lo que haremos es declarar una variable global seria undefined. El this no sabe la aplicación que tiene.
