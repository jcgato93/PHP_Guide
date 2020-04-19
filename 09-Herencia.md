# Herencia

La herencia permite que ciertas clases tengan características de una clase padre. Esta clase se llamará hijo.

Como una buena práctica en PHP lo mejor es tener dividido el código en diferentes archivos. Justo esto es lo que haremos con la definición de la clase Jobs que ahora deberá tener el mismo nombre del archivo, este será BaseElement.php.

Ahora en otro archivo crearemos la clase Job que será hija de BaseElement.php. La herencia la expresaremos con la palabra reservada extends.

Es muy conveniente utilizar require_once cuando queremos utilizar herencia e incluir clases que están en otros archivos.

Dentro de nuestra clase hijo podemos sobrescribir algún método del padre, esto es un concepto que conocemos como polimorfismo. Lo que polimorfismo quiere decir es que tendremos un método que va a funcionar de acuerdo con su contexto donde es llamado.

Si tenemos propiedades con la palabra private en nuestra clase padre, desde nuestra clase hija no podremos acceder a esta propiedad, pero si queremos que siga siendo privada y que las clases hijas tengan acceso podemos usar la palabra clave protected.

```php
<?php
class Padre{
	public carro;
	public casa;
	public televisor;

	function venderCarro(){
	//CODE
	}
	function venderCasa(){
	//CODE
	}
	function venderTelevisor(){
	//CODE
	}
	function venderCarro(){
	//CODE
	}
	function venderCasa(){
	//CODE
	}
	function venderTelevisor(){
	//CODE
	}
	
}
class HijoJunior extends Padre{
	public guitarra;
	public celular;
	public computadora;
	
	function venderGuitarra(){
	//CODE
	}
	function venderCelular(){
	//CODE
	}
	function venderComputadora(){
	//CODE
	}
	
}
?>
```


En este ejemplo, HijoJunior tiene propiedades que son exclusivas en él. Como Celular, Guitarra y Computadora y sus propios métodos VENDER.

Al usarextends, Padre le entrega una copia de sus propiedades a HijoJunior y tambien sus métodos.

Entonces, ahora HijoJunior tiene como propiedades: Celular, Guitarra, Computadora, Casa, Carro y televisor.

Y tambien los metodos para poder vender Casa, Carro, Televisor, Guitarra, Celular y Computadora. Todos los métodos y propiedades que obtuvo por el PADRE no están declarados de manera explicita (directa) , sino implícita (haciendo referencia con la palabra extends al crearse la clase).

Si el hijo desea modificar algun método que heredó del padre, solo es necesario sobreescribir el método dentro de la clase hijo.