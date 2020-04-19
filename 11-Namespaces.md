# Namespaces

Esta es una forma de mantener únicos los nombres de los archivos en el mismo directorio.

Esto nos permite tener mejor organizado el proyecto.

Para declarar un espacio de nombres privado se utiliza la palabra reservada namespace.

```php
// Lib1/Project.php
<?php 
namespace Lib1;

class Project {

}
?>

// App/Models/Poject.php
<?php 
namespace App\Models;

class Project {
    
}
?>


// Importar la Clase Project segun el Namespace
<?php 
// utilizando solo una de las 2
use App\Models\Project;

// para utilizar las 2 en el mismo archivo
$projectLib = Lib1\Project();
$projectApp = App\Project();
?>

```