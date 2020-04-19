# Funciones

Las funciones en PHP se denotan por la palabra reservada function seguida por el nombre de la función, las funciones nos servirán para llamar y reutilizar código en nuestros proyectos.

Cuando trabajemos con funciones es muy importante cuidar el scope (alcance) de las variables pues, algunas podrían entrar en su scope y otras no.

Las funciones en PHP pueden o no regresar un dato particular. Si deseamos hacerlo podemos indicarlo con la palabra reservada return.


```php
<?php 
// Retorna el numero de años segun el numeros de meses que se pasen por parametro
function getDuration($months){
  $years = floor($months / 12);
  $extraMonths = $months % 12;
  if($years != 0 & $extraMonths != 0){
    return "$years years $extraMonths months";
  }else if($years =! 0){
    return "$years years";
  }else {
    return "$extraMonths months";
  }
}

getDuration(15) // 1 years 3 months
?>
```