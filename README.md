# Laboratorio_2_DSVII
Nombre: Genesis Luo
Cédula: 8-1020-1006
Salón: 1GS131

1. Introducción
Laravel es un framework de PHP muy utilizado para desarrollar aplicaciones web de forma rápida y ordenada. Ofrece herramientas que facilitan tareas como la autenticación, manejo de rutas y conexión con bases de datos.
En este instructivo se explica cómo instalar Laravel desde cero y cómo implementar un sistema básico de autenticación con registro e inicio de sesión.

2. Requisitos del sistema
Antes de empezar, asegúrate de tener instalado lo siguiente:
PHP versión 8.1 o superior
Composer (gestor de dependencias de PHP)
Node.js y npm
Un servidor local como XAMPP o Laragon
MySQL para la base de datos

3. Creación del proyecto Laravel
Para crear un nuevo proyecto, abre la terminal y ejecuta:
composer create-project laravel/laravel mi_proyecto
Luego entra a la carpeta del proyecto:
cd mi_proyecto

4. Configuración básica
Se debe preparar el entorno con estos comandos:
cp .env.example .env
php artisan key:generate
Esto genera una clave única que Laravel necesita para funcionar correctamente.

5. Configuración de la base de datos
En el archivo .env se colocan los datos de conexión:
DB_DATABASE=mi_base_datos
DB_USERNAME=root
DB_PASSWORD=tu_contraseña
Después se crean las tablas con:
php artisan migrate

6. Sistema de autenticación
Para agregar login y registro, se instala Laravel UI:
composer require laravel/ui
Luego se ejecuta:
php artisan ui bootstrap --auth
Esto crea automáticamente las vistas, rutas y controladores necesarios para manejar usuarios.

7. Instalación del frontend
Para que la interfaz funcione correctamente:
npm install
npm run dev

8. Levantar el servidor
Para ejecutar el proyecto:
php artisan serve
Y se abre en el navegador:
http://127.0.0.1:8000

9. Funcionamiento del sistema
El sistema permite:
Crear cuentas nuevas
Iniciar sesión
Validar datos de usuario
Guardar información en la base de datos
Laravel se encarga de proteger las contraseñas mediante encriptación automática, lo que mejora la seguridad del sistema.

10. Experiencia del laboratorio
Durante el laboratorio, al descargar y usar Laravel tuve varias dificultades, sobre todo al momento de conectarlo con la base de datos en WampServer. Al inicio, sin darme cuenta, estaba usando SQLite en lugar de MySQL, y además el archivo .env estaba mal configurado, por lo que las migraciones no funcionaban. También tuve problemas con la contraseña de la base de datos y errores porque algunas tablas ya existían. A esto se sumó que me faltaba actualizar algunas aplicaciones como WAMP, lo que causaba advertencias y errores adicionales. En general, lo más complicado fue configurar bien todo el entorno para que Laravel funcionara correctamente con la base de datos. 
