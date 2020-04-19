# Composer

Manejador de dependencias de PHP llamado [Composer](https://getcomposer.org/), no solo nos ayudara a traer librerías de tercero al proyecto además va a implementar el estándar PSR4 que nos va a permitir tener el cargado de archivos automático.

composer.phar será un documento que nos servirá para manejar las dependencias en PHP, esta va muy de la mano con otro archivo llamado composer.json.

## Instalacion

1. https://getcomposer.org/ en la opcion de Download y seguir los pasos para la descarga.

2. Crear archivo composer.json

```json
{
    "autoload": {
        "psr-4": {
            "App\\": "app/"
        }
    },
    "require": {}
}
```

3. Actulizar o descargar las dependencias utilizando composer

        $composer update