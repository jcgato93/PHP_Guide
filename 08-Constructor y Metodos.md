# Constructor y Métodos

El método constructor nos permitirá inicializar valores por default, así como también pasar datos como parámetro al momento de inicializar un objeto.

Todas las funciones que tienen __ antes del nombre de la función se conocen como métodos mágicos


```php
<?php

class Job {
    private $title;
    public $description;
    public $visible;
    public $months;

    // Constructor
    public function __construct($title) {
        $this->title = $title;
    }

    public function getTitle() {
        return $this->title;
    }

    public function setTitle($title) {
        $this->title = $title;
    }

    // Metodo
    public function getDuration() {
        $years = floor($this->months / 12);
        $extraMonths = $this->months % 12;

        return "$years years $extraMonths months";
    }
}

$job1 = new Job('title');
$job1->setTitle('PHP Developer');
$job1->description = 'An aweson job!!';
$job1->visible = true;
$job1->months = 15;

echo $job1->getTitle(); // PHP Developer

?>
```