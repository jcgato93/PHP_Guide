# Variables tipos de datos y cadenas


Una variable puede ser una pequeña cajita en la que puedes almacenar un valor y este lo pueden usar para realizar alguna operación.

Para declararla usaremos el símbolo de $ y en seguida el nombre, este puede ser un _ o una letra.

PHP no es estáticamente tipado, es decir que no tenemos que decirle qué tipo de dato es esa variable. Además, es débilmente tipado porque podemos fácilmente cambiar el tipo de dato, es decir PHP ejecuta una conversión de datos interna.

Al momento de trabajar con PHP una cosa muy importante es hacer debugging a nuestras variables, para ello utilizamos la función var_dump(); pasándole por parámetro la variable a revisar.

```php
<?php 
    $var1 = 1;
    $name = 'Juan';   

    // Para conocer el tipo de dato
    var_dump($name);

    // Concatenar
    echo $var1 . $name // 1Juan
    echo "$var1 $name" // 1 Juan
?>

<h1>Hola <?php echo $name; ?></h1>
```

# Tipos de datos escalares

- boolean:
Representa solamente un valor verdadero o falso. http://php.net/manual/es/language.types.boolean.php
Valores válidos: true (verdadero) false (falso)

```php
<?php
$a = true; 
$b = false; 
?>
```

- Integer:
Representa un número entero positivo, negativo o 0. http://php.net/manual/es/language.types.integer.php

```php
<?php
$a = -123;
$b = 0;
$c = 7763;
?>
```

- float o double:
Representa un número de punto flotante, existen problemas de precisión con los números flotantes debido a la naturaleza binaria de las computadoras. http://php.net/manual/es/language.types.float.php

```php
<?php
$a = 12.24; 
$b = 1.5e3; 
$c = 7E-10;
?> 
```

- string:
    – Representa una cadena de caracteres.
    – Existen 4 formas de representar una cadena. Las 2 principales son usando comillas simples o comillas dobles.
    ---- Usando comillas simples donde el texto será exactamente como se escribe.
    ---- Usando comillas dobles permite usar caracteres de escape y además expanden los nombres de las variables, es decir sustituye el valor de las variables dentro de las cadenas.
    – Hay 2 formas adicionales llamadas Heredoc y Nowdoc que sirven para crear cadenas de múltiples líneas.

```php
<?php
$a = "Hola"; 
$b = 'Mundo'; 
?>
```

# Tipos de datos compuestos

- array:
Representa una colección de valores, aunque por defecto PHP usara índices numéricos, la realidad es que la estructura se representa como un mapa que colecciona pares llave-valor. La sintaxis para definir un arreglo será a partir de corchetes cuadrados, aunque en versiones anteriores de PHP era necesario usar la función array(). Las llaves pueden ser enteros o cadenas y los valores pueden ser de cualquier tipo de PHP, incluso de tipo array. http://php.net/manual/es/language.types.array.php

```php
<?php
$array = array(
    "curso1" => "php",
    "curso2" => "js",
);

// a partir de PHP 5.4
$array = [
    "curso1" => "php",
    "curso2" => "js",
];

// índices numéricos
$array = [
    "php",
    "js",
];
?>
```

- object:
Representa una instancia de una clase.

```php
<?php
class Car
{
    function move()
    {
        echo "Going forward..."; 
    }
}

$myCar = new Car();
$myCar->move();
?>
```

- callable:
Es un tipo de dato especial que representa a algo que puede ser “llamado”, por ejemplo una función o un método.

```php
<?php
// Variable que guarda un callable
$firstOfArray = function(array $array) {
    if (count($array) == 0) { return null; }
    return $array[0];
};

// Este es nuestro arreglo
$values = [3, 2, 1];

// Usamos nuestro callable y se imprime el valor 3
echo $firstOfArray($values);
?>
```

- iterable:
A partir de PHP 7.1 iterable es un pseudo tipo de datos que puede ser recorrido.

```php
<?php

function foo(iterable $iterable) {
    foreach ($iterable as $valor) {
        // ...
    } 
}

?>
```

# Tipos especiales

- resource:
Es un tipo de dato especial que representa un recurso externo, por ejemplo un archivo externo a tu aplicación.

```php
<?php
$res = fopen("c:\\dir\\file.txt", "r");
?>
```

- NULL:
Es un valor especial que se usa para representar una variable sin valor. http://php.net/manual/es/language.types.null.php

```php
<?php
$a = null; 
?>
```