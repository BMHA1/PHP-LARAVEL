# PHP-LARAVEL 🚀
Primero pasos con PHP y su framework laravel! 

***
### Laravel ### 

Laravel: Es un framework de código abierto para desarrollar aplicaciones y servicios web PHP 5 y PHP 7. 
fue creado en 2011 y tiene una gran influencia DE FRAMEWORKS como Ruby on Rails, Sinatra y ASP.NET
***
### Sus caracteristicas: 

- Sistema de ruteo, también RESTful3
- Blade, Motor de plantillas4 5
- Peticiones Fluent6
- Eloquent ORM7
- Basado en Composer8 : herramienta de gestión de paquete 
- Soporte para el caché9
- Soporte para MVC10
- Usa componentes de Symfony11
- Adopta las especificaciones PSR-212 y PSR-4

***
## intalación Compose 🔧 
ir a la pagina https://getcomposer.org/download/ y descargar

***
## Crear Proyecto  
Existen dos formas de generar una estructura de proyecto nuevas: 
 - laravel new (NOMBRE DEL PROYECTO)
 o
 - composer create-project --prefer-dist laravel/laravel (NOMBRE DEL PROYECTO, (VERSIÓN))

***
## Servidor interno 
Mediente el CLI artisan podremos realizar múltiples acciones entre ellas, lanzar el servidor de puebras con el comando

- php artisan serve

***
## Enrutado Básico 
 La ruta definida en el esqueleto del proyecto instalado, define 3 conceptos: 
 - El método que recibe 
 - La ruta
 - Y la accion a realizar

`Route::get('/', function () {
return view('welcome');
});`

## Actividades de clase
```
 - Error vista : generamos una plantilla personalizada para gestionar la vista de los error
 - Creación de nuevas vista.Blade
 - Creación de controller mediante el CLI artisan : php artisan help make:controller
 
```
 ## Reto 1 🔩
 
 A partir de un nuevo proyecto o el proyecto que
se trabaja en clase:
1. Crear un nuevo controlador que se
denomine HomeController
2. Crear un template básico
3. Crear una nueva vista
4. Crear la ruta para que el por defecto de la
web se muestre

## Conexión con base datos - MySQL - CLI Artisan
 
 * Creamos desde Workbench un sckema
 * Configuramos las variables de entorno  desde el archivo .env  colocando el nombre de la BBDD y la contraseña
 * Migramos por defecto unas tablas que PHP nos brinda. en este caso son 4
## llamar a la base de datos desde el controlador 

## crear un nueva migración con CLI Artisan


## Artisan thinker::
Request => al body

## rutas con parametros

##  Creando migración
Creamos una migración con : 
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


    
* Creamos un controlador, cabe descatar que el **-r** nos genera un controlador con todos los métodos:  
```php artisan make:controller "Nombredelcontrolador" -r```
* y desde api, enlazamos al controlador. **EN LA RUTA URL DEBEMOS COLOCAR /API/**  
``` Route::apiResource('/plate', App\Http\Controllers\PlateController::class);``` 
   * Cabe destacar que sí utilizamos el metedo estatico apiResource, nos genera todas las rutas para un CRUD básico. 
 ```php artisan make:controller PacoController -r```

* usar y crear Factory  
```


## Autores ✒️
* **Brajin Hanna Miguel Azrak** - *Conociendo PHP* - [BMHA1](https://github.com/BMHA1/)
