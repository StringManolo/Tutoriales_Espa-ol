# Iniciación Javascript

### Qué es?
  Es un lenguaje de programación de propósito general. Esto significa que puede usarse en programas para móvil, programas de windows, drones, sistemas aeroespaciales, parquímetros, sistemas de contabilidad... Pero donde cobra mayor trascendencia es en la web. Originalmente en páginas web, pero también en el lado del servidor.

### Para qué sirve?
  Para hacer cualquier tipo de programa. Sobre todo haciendo funcionar las páginas web, donde html se usa para definir el contenido, css modifica y estiliza la apariencia y javascript se ocupa de "lo que hace" la web. Desde mostrar algo al pulsar un botón, hasta descargarse una web entera, obtener algo que nos interesa de ella, almacenarlo, mostrarlo, enviarlo...

### Qué conocimientos necesito?
  Ninguno. Se usará html mínimo para crear un documento e indicar donde está el código con javascript.
  


## Programación General.

  Javascript y la mayoría de lenguajes de uso actual utilizan varios elementos que suelen ser comunes entre ellos:
  + Expresiones o sentencias.
  + Variables.
  + Operadores.
  + Condicionales.
  + Bucles.
  + Metodos y Funciones.
  + Arrays.
  + Objetos.

_Nota_: A continuación un resumen de que es cada cosa. No te preocupes si no lo entiendes todo ahora mismo o es demasiada información nueva o abstracta. Vas a ver ejemplos detallados de su uso que facilitaran asimilar los conceptos. 

###### Expresiones o sentencias:
  Son lineas de código que sirven para expresar una acción o un contenido. Por ejemplo _1 + 3;_ es una expresión que suma dos números. El punto y coma sirve para indicar el final de una expresión. 

###### Variables:
  Son contenedores para guardar algo que vamos a querer utilizar más tarde. Por ejemplo _var resultado = 1 + 3;_ nos almacenará 4 dentro de una variable a la que pusimos de nombre resultado. Hay distintos tipos de datos y contenedores.

###### Operadores: 
  Sirven para realizar operaciones de todo tipo. Tenemos los operadores matemáticos básicos pero también tenemos algunos otros útiles como el menor o igual que _<=_ el de asignación _=_ o el de comparación _==_ entre otros muchos.

###### Condicionales:
  Sirven para realizar una acción cuando se cumpla la condición que le indiquemos. Ejemplo _if (resultado == 4)_ se cumplirá si la variable resultado es igual a 4. Lo veremos en más detalle.

###### Bucles:
  Sirven para poder realizar una acción en bucle, es decir, de forma repetida hasta alcanzar el resultado deseado. Ejemplo _while (resultado == 4)_ se repetira en bucle la expresión que le indiquemos entre corchetes mientras la variable resultado sea igual a 4.

###### Metodos y Funciones:
  Los métodos y las funciones se utilizan para agrupar código designado para una tarea. Por ejemplo podemos agrupar un programa entero que haga la declaración de la renta y otro que mustre los datos de diversas empresas. De esta forma podremos llamar a todo el código para hacer la declaración de la renta de una forma sencilla sin tener que rescribirlo de cero cada vez que queramos hacer la declaración a una persona distinta. Al final nos quedara una función que podremos usar tal que: _hacerDeclaración("Paco");_ _hacerDeclaración("Antonio");_ ... Los métodos son prácticamente iguales.

###### Arrays:
  Los arrays son contenedores al igual que las variables, pero nos permiten almacenar varios datos y también variables. Ejemplo: _var colores = ["rojo", "verde", "azul"];_
  Para acceder a ellos usaremos índices que empiezan a contar desde 0. Por ejemplo si quiero mostrar la palabra rojo:
  _alert(colores[0]);_
 

###### Objetos:
  Los objetos son agrupaciones de datos o funciones que están relacionados de alguna forma. Por ejemplo podemos hacer un objeto persona que va a tener variables como nombre, altura, edad... Y métodos como hablar, caminar, comer...


## Primeros Pasos.

#### Creando el documento:
  Antes de empezar a programar en javascript necesitas un documento HTML para indicarle al navegador que vamos a usar javascript:
```
<html>
<body>
<script>

</script>
</body>
</html>
```

Solo son 3 etiquetas html. Dentro de las etiquetas script vas a escribir el código javascript que quieras. Si quieres utilizar acentos y caracteteres especiales debes añadir las etiquetas head y meta charset. Por lo general puedes usar el ejemplo anterior, o si lo prefieres añadir más datos quedando:
```
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<title>Título de la pestaña</title>
</head>
<body>
Este texto lo veras en el documento.
<script>

</script>
</body>
</html>
```
Este código HTML debes escribirlo y guardarlo en un archivo con cualquier editor de texto. Por ejemplo el notepad o bloc de notas de windows. Guárdalo como NombreDeMiDocumento.html 
  
Vamos a trabajar en este archivo que abriremos en el navegador para ver los resultados. De momento no hace nada. Si ponemos 1 + 3; hará la suma, pero no veremos el resultado porque no se lo indicamos. 
Existen multitud de formas de ver los resultados, nosotros veremos la más básica de todas, la función alert. 

### Conociendo alert

alert es una función (que ya viene definida en el navegador) que muestra una ventana pequeña en pantalla con el valor que le indiquemos.

Vamos a utilizar alert para mostrar el resultado de la suma:
```
<html>
<body>
<script>
alert(1 + 3);
</script>
</body>
</html>
```

Asegúrate de guardar los cambios y abre el archivo con extensión tuArchivo.html en el navegador. Para ello puedes hacer click derecho y seleccionar abrir con ... Ahí deberás elegir Chrome, Mozilla, Edge, Internet Explorer, Safari, Opera... El explorador que tú tengas. Debes ver una ventana que muestre el número 4. Si no es así repite el proceso y asegúrate que todo está correcto.

A parte de realizar operaciones también puedes mostrar texto si lo encierras entre comillas. Ejemplo:
```
<html>
<body>
<script>
alert("Bienvenido a mi primer programa con javascript");
</script>
</body>
</html>
```

### Trabajando con variables.

También puedes guardar el resultado de la operación o el texto en una variable y mostrarlo desde el alert.
```
<html>
<body>
<script>
var resultado = 4;
var saludo = "bienvenido a mi primer programa";
var nombre = "Juan";
alert("Hola");
alert(nombre);
alert(saludo);
alert(resultado);
</script>
</body>
</html>
```

Es un poco incómodo mostrar 4 alerts distintos y que el usuario necesite pulsar 4 veces en aceptar para leer todos nuestros mensajes. Hay secuencias de caracteres que tienen funcionalldad especial, como \n que nos permite hacer una **n**ueva línea. Y el operador **+** sirve también para unir texto, no solo para sumar números, asique podemos mostrarlo todo en un solo alert.
```
<html>
<body>
<script>
var resultado = 4;
var saludo = "bienvenido a mi primer programa";
var nombre = "Juan";
alert("Hola " + nombre + " " + saludo + ".\n" + "Ya no necesito utilizar " + resultado + " alerts para mostrarte este texto");
</script>
</body>
</html>
```

Pruébalo, verás el siguiente texto:
```
Hola Juan bienvenido a mi primer programa.
Ya no necesito utilizar 4 alerts para mostrarte este texto.
```

Probablemente nuestro usuario no se llame Juan. Hay otra función muy similar a alert llamada prompt que da al usuario la posibilidad de escribir algo en la ventana, y a nosotros de obtenerlo.

Vamos a hacer un programa que pida el nombre, la edad y le dedique un saludo personalizado.

```
<html>
<body>
<script>
var saludo = "Hola ";
var nombre = prompt("Cual es tu nombre?");
var edad = prompt("Cuantos años tienes?");
alert(saludo + nombre + " tienes " + edad + " años.");
</script>
</body>
</html>
```

### Los condicionales.

Esto está genial! Pero a todos los saludamos igual. Vamos a usar los condicionales para personalizar más el saludo:
__A partir de ahora se asume que sabes que se debe poner el código en el documento entre las etiquetas y se omite por brevedad.__ 
```
var nombre = prompt("Cual es tu nombre?");
var edad = prompt("Cuantos años tienes?");

if(edad < 18) {
  var saludo = "Qué pasa ";
  var postSaludo = " qué tal los estudios?";
}

if(edad >= 18 && edad < 65) {
  var saludo = "Hola ";
  var postSaludo = " qué tal la familia?";
}

if(edad >= 65) {
  var saludo = "Adelante ";
  var postSaludo = " qué tal está usted?";
}

alert(saludo + nombre + postSaludo);
```

El condicional if tiene una condición que va entre paréntesis y lo que queramos que pase si se cumple la condición va entre corchetes. También usamos el operador and __&&__ que sirve para añadir más de una condición que se tiene que cumplir.

Ahora vamos a hacer un programa que pida una contraseña, si se cumple la condición, es decir si se puso la contraseña correcta mostraremos un texto indicándolo, y en caso contrario mostraremos otro distinto.

```
var contraseña = "abc123";
var introducida = prompt("Adivina la contraseña");

if (contraseña == introducida) {
  alert("Enhorabuena, introduciste la contraseña correcta.");
} else {
  alert("Ohh, fallaste!");
}
```

La palabra clave else sirve para poner código que se ejecute cuando no se cumpla la condición del if.

Este programa tiene un problema, y es que si queremos que el usuario tenga 10 intentos, tendrá que abrir la página 10 veces  o tendremos que pegar 10 veces el código. No parece algo tan malo, pero y si le quisiésemos dar 1000 intentos? Sería una locura copiar y pegar tanto y el archivo ocuparía mucho espacio. Para evitar esto tenemos los bucles.

### Los bucles.

El bucle while se parece mucho al condicional if, pero en lugar de ejecutarse una vez, lo hace hasta que la condición se cumpla:
```
var contraseña = "abc123"
var introducida = "aún no se pidió";

while (contraseña != introducida) {
  introducida = prompt("Adivina la contraseña");
}
```

Aquí usamos el operador __desigual a__ en la condición. Es decir mientras la contraseña sea desigual a la introducida, ejecuta el código entre corchetes. Como ves __var__ solo es necesario utilizarlo para crear la variable, después se puede omitir.

Otro bucle de uso muy amplio es el for, que se puede ver de varias formas. Solo vamos a ver la forma clásica que en lugar de utilizar un condicional usa 3 expresiones. Es común su uso para contar o hacer acciones un determinado número de veces:
```
for (var contador = 0; contador < 10; contador += 1) {
  alert(contador);
}
```

Como ves entre paréntesis hay 3 expresiones. La primera es para indicar la variable que se usará de contador. La segunda para indicar que condición se debe cumplir. La tercera para indicar cuanto debe aumentar o disminiur el contador.

### Funciones y métodos.

Las funciones y métodos son de las herramientas más útiles. Hasta ahora usamos alert y prompt, 2 funciones que nos sirven para interactuar con el usuario de forma sencilla. Nosotros haremos una función que nos permita obtener múltiples datos de una persona y la utilizaremos en un bucle en base al número de personas que nos indique el usuario. Es decir, si el usuario quiere darnos los datos de 2 personas, de 8, etc, nosotros tomaremos los datos de todos ellos.
Primero vamos a preguntarle al usuario:
```
var miembrosUnidadFamiliar = prompt("Con cuantas personas convive en su domicilio?");
```

El siguiente paso sería preguntarle los datos que queremos saber de cada miembro:
```
var nombre = prompt("Introduzca el nombre de un miembro de su unidad familiar");
var edad = prompt("Dígame la edad de " + nombre);
var sexo = prompt(nombre + " es hombre o mujer?");
var estadoCivil = prompt(nombre + " está casado/a, soltero/a, viudo/a o divorciado/a");
```

Ahora podemos meter todas estas preguntas en una sola función. Y de paso hacemos que la función nos retorne todo organizado:
```
function obtenerDatos() {
  var nombre = prompt("Introduzca el nombre de un miembro de su unidad familiar");
  var edad = prompt("Dígame la edad de " + nombre);
  var sexo = prompt(nombre + " es hombre o mujer?");
  var estadoCivil = prompt(nombre + " está casado/a, soltero/a, viudo/a o divorciado/a");

  return "Nombre:" + nombre + "\nEdad:" + edad + "\nSexo:" + sexo + "\nEstado Civil:" + estadoCivil;
}
```

Ya tenemos definido lo que hace. Ahora podemos usarla siempre que queramos de la misma forma que un prompt. Solo nos falta el bucle para acabar el programa, quedando tal que:
```
var miembrosUnidadFamiliar = prompt("Con cuantas personas convive en su domicilio?");

for (var contador = 0; contador < miembrosUnidadFamiliar; ++contador) {
  var datosDeFamiliar = obtenerDatos();
  alert(datosDeFamiliar);
}


function obtenerDatos() {
  var nombre = prompt("Introduzca el nombre de un miembro de su unidad familiar");
  var edad = prompt("Dígame la edad de " + nombre);
  var sexo = prompt(nombre + " es hombre o mujer?");
  var estadoCivil = prompt(nombre + " está casado/a, soltero/a, viudo/a o divorciado/a");

  return "Nombre:" + nombre + "\nEdad:" + edad + "\nSexo:" + sexo + "\nEstado Civil:" + estadoCivil;
}
```

A lo largo del tiempo podríamos hacer funciones y almacenarlas en un archivo para poder utilizarlas sin tener que crearlas de nuevo de la misma forma que prompt y alert.


### Arrays.

  En lugar de retornar la cadena de texto, nos puede ser de interes separar los datos para acceder a ellos de forma individual:
```
var datosDeFamiliar = [nombre, edad, sexo, estadoCivil];
```

Así nos es posible tener todos los datos en un solo lugar y a la vez poder acceder a ellos individualmente:
```
alert(datosDeFamiliar);
alert("Hola " + datosDeFamiliar[0] + " estás " + datosDeFamiliar[3] + " eres " + datosDeFamiliar[2] + " y tienes " + datosDeFamiliar[1] + " años.");
```

### Métodos.

Qué pasa si queremos mostrar solo la inicial del nombre? Para ello javascript al igual que con alert y prompt, nos da un método llamado _substr_ cuya finalidad es a partir de un texto formar otro. Por ejemplo a partir del nombre Paco podremos obtener la P. Los métodos tienen una diferencia con las funciones, y es que estos son específicos de un objeto. Esto significa que no podemos crear un subtexto de un número, porque como es obvio un número no es un texto. Como ya vimos en ejemplos anteriores, el texto va entre comillas, mientras que los números no.
Veamos un ejemplo del método substr:
```
var nombre = "paco";
var inicial = nombre.substr(0, 1);
alert(inicial);
```

En este caso substr acepta 2 números separados por comas. El primero nos permite seleccionar la posición desde la que empezar a obtener caracteres. El segundo número nos permite indicar cuantos caracteres vamos a obtener a partir de la posición que indicamos. En el ejemplo a partir de la letra 0, obtendremos 1 letra. Es decir de _paco_ obtendremos la _p_. Si quisiesemos obtener _ac_ haríamos _var letrasCentrales = nombre.substr(1, 2);_ es decir, desde el caracter _a_ obtenemos 2 letras. 

Hay muchos métodos predefinidos en javascript y se pueden encadenar. Por ejemplo si queremos mostrar la inicial de un nombre en mayúsculas podremos usar _substr(0, 1)_ y _toUpperCase()_ ejemplo:
```
var nombre = prompt("Cómo te llamas?"):
var inicial = nombre.substr(0, 1);
var inicialEnMayuscula = inicial.toUpperCase();
alert(inicialEnMayuscula);
```

También podemos encadenar métodos en una sola línea:
```
var nombre = prompt("Cómo te llamas?");
var inicialEnMayuscula = nombre.substr(0, 1).toUpperCase();
alert(inicialEnMayuscula);
```

Esto es posible debido a que javascript va evaluando las expresiones de izquierda a derecha remplazándolas por su resultado. Qué signifca esto? Significa que podemos simplificar mucho el código agrupando la funcionalidad en una sola linea, de tal forma que el ejemplo anterior también lo podemos hacer tal que:
```
alert(prompt("Cómo te llamas?").substr(0, 1).toUpperCase());
```

El navegador hará lo siguiente:
  Hay paréntesis? Entonces evaluo lo que hay dentro:

  Encuentro _prompt("Cómo te llamas?")_ ejecuto la función y la remplazo por el resultado quedando el código tal que:
  _alert("paco".substr(0, 1).toUpperCase());_

  Hay paréntesis? Entonces evaluo lo que hay dentro:

  Encuentro _"paco".substr(0, 1)_ ejecuto el método y lo remplazo por el resultado quedando el código tal que:
  _alert("p".toUpperCase());_

  Hay paréntesis? Entonces evaluo lo que hay dentro:

  Encuentro _"p".toUpperCase()_ ejecuto el método y lo remplazo por el resultado quedando el código tal que:
  _alert("P");_

  Como se puede apreciar ya no quedan expresiones que evaluar, asique el navegador pasará a hacer alert de "P".


### Objetos.

  Todo lo que hemos usado hasta ahora son objetos. Un objeto no es más que un contenedor en el que podemos guardar variables y funciones. Cuando una variable o una función pertenece a un objeto, nos referiremos a ellas como propiedades y métodos.
Los objetos de momento los veremos como una forma sencilla de agrupar variables y funciones que tengan que ver entre sí. Para crear un objeto usaremos:
```
var vehiculo = {};
```

Para añadir una variable(propiedad) usaramos el operador _._ que ya vimos:
```
vehiculo.velocidadActual = 0;
```

Para añadir una función(método) también usaremos el mismo operador, pero asignaremos una función sin nombre:
```
vehiculo.acelerar = function() {
  vehiculo.velocidadActual += 1;
};
```







