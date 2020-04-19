# Agregando archivos externos

Organizaremos mejor nuestro código para ello lo separaremos en otro archivo llamado jobs.php.

Usaremos la palabra reservada include para hacer que el archivo index incluya el archivo jobs.php, si lo encuentra lo incluye, pero si no nos mostrará un warning. Existe otro llamado require que si no lo encuentra nos muestra un error en todo el archivo.

Los métodos include y require ejecutan el código del archivo cada vez que lo incluyen, esto puede traer errores en la ejecución de tu código si tienes archivos con funciones pues te dirá que no puedes declarar dos veces una función con el mismo nombre. Para resolver esto existen include_once y require_once que obligan a incluir una sola vez el archivo.

## Crear archivo con la logica

variables.php

```php
<?php

$var1 = 1
$var2 = 2
```

principal.php

```php
<?php
// warning
include('variables.php');

// error fatal y detiene la ejecucion
// require('variables.php)

echo $var1 // 1
?>
```