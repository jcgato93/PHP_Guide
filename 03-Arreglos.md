# Arreglos

Como vimos en la clase anterior almacenamos datos en una variable, ahora trataremos de almacenar más datos en una misma variable.

Estas variables que almacenan más de un dato se conocen como arreglos y su sintaxis se va a indicar con [ ] (corchetes).

PHP utiliza índices para localizar a los elementos dentro de la variable.

La estructura de arreglos en PHP es conocida como mapa, lo que quiere decir que tiene una composición de llave valor. Además, un arreglo puede contener más arreglos y cada uno de ellos seguirá la misma estructura.

Algo que debes saber es que en PHP podrás almacenar diferentes tipos de datos en un mismo arreglo.

```php
<?php 
$jobs = [
    'php developer',
    'python dev',
    'devops'
];

echo $jobs[1]; // python dev

// Array llave valor
$asMap = [
    'title' => 'item 1',
    1 => 'item 2',
    2 => 'item 3'
];

echo $asMap['title']; // item 1

// arreglo complejo
$arr = [
    [
        'title' => 'job 1'
    ],
    [
        'title' => 'job 2'
    ],
    [
        'title' => 'job 3'
    ]
];

echo $arr[1]['title']; // job 2
?>
```
