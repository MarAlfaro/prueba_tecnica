
# Prueba Técnica - Sistema de Autenticación de Usuarios

Este es un proyecto de prueba técnica que implementa un sistema de autenticación de usuarios utilizando **Laravel Sanctum**. La API permite registrar usuarios, iniciar sesión, proteger rutas y gestionar el perfil del usuario autenticado.

## Requisitos

Para ejecutar este proyecto, necesitas tener instalados los siguientes programas:

- **PHP** (recomendado PHP 8.0 o superior)
- **Composer** (para gestionar las dependencias de PHP)
- **MySQL** (como base de datos)
- **Node.js** (si trabajas con frontend o necesitas ejecutar tareas de compilación)
- **Git** (para control de versiones)

## Instalación

### 1. Clonar el repositorio

Primero, clona el repositorio en tu máquina local:

```bash
git clone https://github.com/MarAlfaro/prueba_tecnica.git
cd prueba_tecnica
```

### 2. Instalar las dependencias

Usa Composer para instalar las dependencias del proyecto:

```bash
composer install
```

### 3. Configurar el archivo `.env`

Copia el archivo `.env.example` y renómbralo a `.env`:

```bash
cp .env.example .env
```

Ahora, abre el archivo `.env` y configura los parámetros necesarios, como la conexión a la base de datos:

```ini
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=nombre_de_tu_base_de_datos
DB_USERNAME=tu_usuario
DB_PASSWORD=tu_contraseña
```

### 4. Generar la clave de la aplicación

Genera la clave de la aplicación Laravel:

```bash
php artisan key:generate
```

### 5. Ejecutar las migraciones

Para crear las tablas necesarias en la base de datos (como usuarios, tokens, etc.), ejecuta las migraciones:

```bash
php artisan migrate
```

### 6. Configurar Sanctum

Asegúrate de que el archivo `config/sanctum.php` esté correctamente configurado y habilitado el middleware en el archivo `app/Http/Kernel.php`. Si has seguido los pasos de configuración, ya debería estar listo.

### 7. Instalar las dependencias de frontend (si aplica)

Si el proyecto incluye un frontend, también puedes instalar las dependencias de JavaScript utilizando npm o yarn:

```bash
npm install
# o
yarn install
```

### 8. Iniciar el servidor de desarrollo

Para iniciar el servidor de desarrollo de Laravel, usa el siguiente comando:

```bash
php artisan serve
```

Esto iniciará la API en `http://localhost:8000` por defecto.

### 9. Enviar correos de confirmación (Opcional)

Si la aplicación está configurada para enviar correos (por ejemplo, para confirmar el registro de usuarios), asegúrate de configurar correctamente un servicio de correo en el archivo `.env`:

```ini
MAIL_MAILER=smtp
MAIL_HOST=smtp.mailtrap.io
MAIL_PORT=2525
MAIL_USERNAME=tu_usuario
MAIL_PASSWORD=tu_contraseña
MAIL_ENCRYPTION=tls
MAIL_FROM_ADDRESS=tu_correo@example.com
MAIL_FROM_NAME="${APP_NAME}"
```




