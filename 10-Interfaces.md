# Interfaces

Las interfaces se pueden ver como un contrato o un acuerdo en el que se pueden estandarizar ciertas cosas.

La palabra reservada que utilizaremos para declarar una interfaz será interface. Y la que nos indicará que estamos usando una interfaz en una clase será implements.

Usando Type Hinting estableceremos el tipo de dato que esperamos ya sea una clase o un tipo de dato específico.

La herencia en PHP será de forma sencilla es decir solo que podrá hacer herencia de una sola clase, por lo contrario, con las interfaces que sí podemos implementar varias al mismo tiempo.

```php
<?php 

    interface WebPage{

        public function printFooter();
    } 
    
    class Page implements WebPage {

        public function prinFooter(){
            // implementar la funcion
        }
    }
?>
```