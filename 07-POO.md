# Programacion orientada a objetos

La programación orientada a objetos nos ayudará a estructurar mejor nuestros programas. PHP a partir de su versión 5 tiene implementaciones orientadas a objetos, lo que lo hace tener código más reutilizable y mantenible.

Una clase es una plantilla o definición de algo. Y una instancia es la representación concreta de la clase.

Encapsulamiento será el nivel de visibilidad que queramos darle a alguna variable, para ello podemos utilizar los modificadores de acceso private, public y protected.

Con la palabra reservada this estaremos haciendo referencia a la variable que pertenece a la clase.

```php
<?php

class Job {
    private $title;
    public $description;
    public $visible;
    public $months;

    public function getTitle() {
        return $this->$title;
    }

    public function setTitle($title) {
        $this->$title = $title;
    }
}

$job1 = new Job();
$job1->setTitle('PHP Developer');
$job1->description = 'An aweson job!!';
$job1->visible = true;
$job1->months = 15;

echo $job1->getTitle(); // PHP Developer
?>
```