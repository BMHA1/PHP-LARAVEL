# PHP-LARAVEL 馃殌
Primero pasos con PHP y su framework laravel! 

***
### Laravel ### 

Laravel: Es un framework de c贸digo abierto para desarrollar aplicaciones y servicios web PHP 5 y PHP 7. 
fue creado en 2011 y tiene una gran influencia DE FRAMEWORKS como Ruby on Rails, Sinatra y ASP.NET
***
### Sus caracteristicas: 

- Sistema de ruteo, tambi茅n RESTful3
- Blade, Motor de plantillas4 5
- Peticiones Fluent6
- Eloquent ORM7
- Basado en Composer8 : herramienta de gesti贸n de paquete 
- Soporte para el cach茅9
- Soporte para MVC10
- Usa componentes de Symfony11
- Adopta las especificaciones PSR-212 y PSR-4

***
## intalaci贸n Compose 馃敡 
ir a la pagina https://getcomposer.org/download/ y descargar

***
## Crear Proyecto  
Existen dos formas de generar una estructura de proyecto nuevas: 
 - laravel new (NOMBRE DEL PROYECTO)
 o
 - composer create-project --prefer-dist laravel/laravel (NOMBRE DEL PROYECTO, (VERSI脫N))

***
## Servidor interno 
Mediente el CLI artisan podremos realizar m煤ltiples acciones entre ellas, lanzar el servidor de puebras con el comando

- php artisan serve

***
## Enrutado B谩sico 
 La ruta definida en el esqueleto del proyecto instalado, define 3 conceptos: 
 - El m茅todo que recibe 
 - La ruta
 - Y la accion a realizar

`Route::get('/', function () {
return view('welcome');
});`

## Actividades de clase
```
 - Error vista : generamos una plantilla personalizada para gestionar la vista de los error
 - Creaci贸n de nuevas vista.Blade
 - Creaci贸n de controller mediante el CLI artisan : php artisan help make:controller
 
```
 ## Reto 1 馃敥
 
 A partir de un nuevo proyecto o el proyecto que
se trabaja en clase:
1. Crear un nuevo controlador que se
denomine HomeController
2. Crear un template b谩sico
3. Crear una nueva vista
4. Crear la ruta para que el por defecto de la
web se muestre

## Conexi贸n con base datos - MySQL - CLI Artisan
 
 * Creamos desde Workbench un sckema
 * Configuramos las variables de entorno  desde el archivo .env  colocando el nombre de la BBDD y la contrase帽a
 * Migramos por defecto unas tablas que PHP nos brinda. en este caso son 4
## llamar a la base de datos desde el controlador 

## crear un nueva migraci贸n con CLI Artisan


## Artisan thinker::
Request => al body

## rutas con parametros

##  Creando migraci贸n
Creamos una migraci贸n con : 
``` php artisan make:migration create_plates```                                                
 * Definimos un modelo:  
```php artisan make:model Blog``` 

    * Estructura del modelo creado:
    
    ```use Illuminate\Database\Eloquent\Factories\HasFactory;
use Illuminate\Database\Eloquent\Model;

class Plate extends Model
{
    use HasFactory;
    protected $fillable = [
        'name',
        'comensales',
        'content_gluten',
    ];
    protected $casts = [
        'content_gluten' => 'boolean',
    ];
}```


    
* Creamos un controlador, cabe descatar que el **-r** nos genera un controlador con todos los m茅todos:  
```php artisan make:controller "Nombredelcontrolador" -r```
* y desde api, enlazamos al controlador. **EN LA RUTA URL DEBEMOS COLOCAR /API/**  
``` Route::apiResource('/plate', App\Http\Controllers\PlateController::class);``` 
   * Cabe destacar que s铆 utilizamos el metedo estatico apiResource, nos genera todas las rutas para un CRUD b谩sico. 
 ```php artisan make:controller PacoController -r```

* usar y crear Factory  
```


## Autores 鉁掞笍
* **Brajin Hanna Miguel Azrak** - *Conociendo PHP* - [BMHA1](https://github.com/BMHA1/)
