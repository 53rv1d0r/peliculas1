## API en Laravel 8 y front vuetify (VUE)

Archivos en la rama master:

- Los propios del proyecto en Laravel.

- Carpeta pelisvuetifycrud

## Base de datos en MySql

Inicialmente se crea base de datos en MySql vacía.

Posteriormente va a quedar una sola tabla (mediante php artisan migrate) con los campos:

id (defecto)

descripcion (Nombre de interfaz: Pelicula)

precio (Nombre de interfaz: Precio)

stock (Nombre de interfaz: Inventario)

timestamp (hora de creación defecto)

timestamp (hora de edición defecto)

## Modelo Articulo

Se crea el modelo Articulo

php artisan make model Articulo

## Tabla articulos

Se crea la migración para la creación de la tabla articulos

php artisan make: migration create_articulos_table

Se agregan a la migración los campos descripcion, precio, stock y sus respectivos tipos de dato

se ejecuta una nueva migración php artisan migrate

## Controlador Articulo

Se crea el Articulo controller, se invoca el modelo Articulo

php artisan make: controller ArticuloController --resource

Aquí se definen los métodos del CRUD para la API

Index + all trae todos los articulos (peliculas)

Create

Store + objeto request captura a la base de datos

Show

Edit

Update + método findorfail

Delete + destry ($request ->id)

## Configuración de rutas

Usamos la misma ruta /articulos para las operaciones de CRUD, por el método HTTP se identifica la operación CRUD a realizar.

## Front en VUE JS

- Framework vuetify

- Cargado mediante CDN´s 

- Plugin de Jquery Sweetalert para optimizar la presentación de los mensajes

- Se crea la tabla

- Variable let url tiene la ruta de la api (se pone a correr el proyecto y se ejecuta el front que apunta al proyecto)

- Definimos variables y métodos GET, POST, PUT, DELETE (API)

##

<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400"></a></p>

<p align="center">
<a href="https://travis-ci.org/laravel/framework"><img src="https://travis-ci.org/laravel/framework.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>

## About Laravel

Laravel is a web application framework with expressive, elegant syntax. We believe development must be an enjoyable and creative experience to be truly fulfilling. Laravel takes the pain out of development by easing common tasks used in many web projects, such as:

- [Simple, fast routing engine](https://laravel.com/docs/routing).
- [Powerful dependency injection container](https://laravel.com/docs/container).
- Multiple back-ends for [session](https://laravel.com/docs/session) and [cache](https://laravel.com/docs/cache) storage.
- Expressive, intuitive [database ORM](https://laravel.com/docs/eloquent).
- Database agnostic [schema migrations](https://laravel.com/docs/migrations).
- [Robust background job processing](https://laravel.com/docs/queues).
- [Real-time event broadcasting](https://laravel.com/docs/broadcasting).

Laravel is accessible, powerful, and provides tools required for large, robust applications.

## Learning Laravel

Laravel has the most extensive and thorough [documentation](https://laravel.com/docs) and video tutorial library of all modern web application frameworks, making it a breeze to get started with the framework.

If you don't feel like reading, [Laracasts](https://laracasts.com) can help. Laracasts contains over 1500 video tutorials on a range of topics including Laravel, modern PHP, unit testing, and JavaScript. Boost your skills by digging into our comprehensive video library.

## Laravel Sponsors

We would like to extend our thanks to the following sponsors for funding Laravel development. If you are interested in becoming a sponsor, please visit the Laravel [Patreon page](https://patreon.com/taylorotwell).

### Premium Partners

- **[Vehikl](https://vehikl.com/)**
- **[Tighten Co.](https://tighten.co)**
- **[Kirschbaum Development Group](https://kirschbaumdevelopment.com)**
- **[64 Robots](https://64robots.com)**
- **[Cubet Techno Labs](https://cubettech.com)**
- **[Cyber-Duck](https://cyber-duck.co.uk)**
- **[Many](https://www.many.co.uk)**
- **[Webdock, Fast VPS Hosting](https://www.webdock.io/en)**
- **[DevSquad](https://devsquad.com)**
- **[Curotec](https://www.curotec.com/services/technologies/laravel/)**
- **[OP.GG](https://op.gg)**

## Contributing

Thank you for considering contributing to the Laravel framework! The contribution guide can be found in the [Laravel documentation](https://laravel.com/docs/contributions).

## Code of Conduct

In order to ensure that the Laravel community is welcoming to all, please review and abide by the [Code of Conduct](https://laravel.com/docs/contributions#code-of-conduct).

## Security Vulnerabilities

If you discover a security vulnerability within Laravel, please send an e-mail to Taylor Otwell via [taylor@laravel.com](mailto:taylor@laravel.com). All security vulnerabilities will be promptly addressed.

## License

The Laravel framework is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).
"# apirest_crud_laravel8" 
