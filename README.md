# login-lab
<<<<<<< HEAD
 # Login-Lab (Laravel)
- Laravel + Breeze (Blade), MySQL (XAMPP)
- Pasos clave: composer create-project, .env a MySQL, php artisan migrate, breeze:install blade, npm run dev, php artisan serve.
- Evidencias: Home con Login/Register, Register ok, Login ok, phpMyAdmin con tablas (users, migrations, sessions).

=======
# Laboratorio #2 – Login en Laravel con Breeze
1. Introducción

Este laboratorio tuvo como objetivo implementar un módulo de autenticación (registro, login y logout) en Laravel, aplicando la arquitectura Modelo–Vista–Controlador (MVC).

Modelos (Models): gestionan la lógica y comunicación con la base de datos.

Vistas (Views): muestran la interfaz al usuario.

Controladores (Controllers): coordinan la lógica entre modelos y vistas.
Rutas (Routes): definen los accesos a controladores y vistas.

Con esto se consolidó la comprensión del patrón MVC y el uso de Laravel Breeze para simplificar la autenticación.

# 2. Requisitos Previos

PHP ≥ 8.0
Composer (última versión)
Laravel 11
Node.js y npm
Servidor local (XAMPP con Apache y MySQL)
Editor de código (Visual Studio Code)
Navegador web (Chrome o similar)

# 3. Flujo de Comandos Utilizados
# Crear el proyecto
composer create-project laravel/laravel login-lab
cd login-lab

# Preparar entorno
copy .env.example .env
php artisan key:generate

# Instalar Breeze
composer require laravel/breeze --dev
php artisan breeze:install

# Instalar dependencias frontend
npm install
npm run build   # se usó build en lugar de dev para mejor rendimiento

# Migrar base de datos
php artisan migrate

# Levantar el servidor
php artisan serve --host=127.0.0.1 --port=8000

# 4. Configuración de la Base de Datos

En el archivo .env se configuró la conexión con MySQL:

DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=login_lab
DB_USERNAME=root
DB_PASSWORD=

SESSION_DRIVER=file
CACHE_DRIVER=file
QUEUE_CONNECTION=sync


Se creó la base de datos login_lab en phpMyAdmin y se ejecutaron las migraciones con php artisan migrate.
El respaldo se generó desde phpMyAdmin → Exportar → SQL y se guardó en:

database_backup/login_lab.sql

# 5. Evidencias
![Imagen de WhatsApp 2025-09-28 a las 16 23 17_cd375b7e](https://github.com/user-attachments/assets/0a9e77b3-cbaa-4892-8723-c26bdd4ac41a)

![Imagen de WhatsApp 2025-09-28 a las 16 54 43_b7c69a3f](https://github.com/user-attachments/assets/73a18064-b30a-434a-ad18-aa67bff8f91d)

![Imagen de WhatsApp 2025-09-28 a las 16 55 06_24b0f2b6](https://github.com/user-attachments/assets/0bd3ad7c-89a0-43c2-9e51-96eb47f4b618)


# 6. Dificultades y Soluciones

Problema: El CSS no cargaba en las vistas.

Solución: Ejecutar npm run build para compilar los assets en public/build.


# 7. Referencias

[Documentación oficial de Laravel](https://laravel.com/docs/12.x)

[Laravel Breeze en GitHub](https://github.com/laravel/breeze)

https://stackoverflow.com/questions/tagged/laravel

# Footer
Nombre: Danna Dawkins

Correo: danna.dawkins@utp.ac.pa

Curso: Ingeniería Web

Instructor: Ing. Irina Fong

Fecha de ejecución:28/09/2025

