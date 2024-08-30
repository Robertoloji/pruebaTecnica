**Laravel Stripe Integration**

Este proyecto es una aplicación Laravel que integra el gateway de pago de Stripe para procesar pagos. Permite a los usuarios realizar pagos a través de una sesión de Stripe Checkout.

**Requisitos**

- PHP >= 8.0
- Composer
- MySQL
- XAMPP o un servidor web compatible

**Instalación**

1. **Clonar el Repositorio**

   Si aún no has clonado el repositorio, hazlo usando el siguiente comando:

   git clone <URL del repositorio>
   cd <nombre-del-repositorio>
 

2. **Instalar Dependencias**

   Asegúrate de estar en el directorio del proyecto y ejecuta:

   composer install


3. **Configurar el Entorno**

   Copia el archivo `.env.example` a `.env`:

   cp .env.example .env

   Luego, abre el archivo `.env` y configura los detalles de tu base de datos y Stripe:

   DB_CONNECTION=mysql
   DB_HOST=127.0.0.1
   DB_PORT=3306
   DB_DATABASE=laraveldb
   DB_USERNAME=root
   DB_PASSWORD=

   STRIPE_KEY=pk_test_xxxxxxxxxxxxxxxxxxx
   STRIPE_SECRET=sk_test_xxxxxxxxxxxxxx
 

4. **Generar la Clave de Aplicación**

   Ejecuta el siguiente comando para generar la clave de aplicación de Laravel:

   php artisan key:generate


5. **Ejecutar Migraciones**

   Ejecuta las migraciones para crear las tablas necesarias:

   php artisan migrate


6. **Instalar Stripe PHP SDK**

   Ejecuta el siguiente comando para instalar la biblioteca de Stripe:

   composer require stripe/stripe-php


7. **Iniciar el Servidor de Desarrollo**

   Inicia el servidor de desarrollo de Laravel:

   php artisan serve

   Accede a la aplicación en tu navegador a través de `http://127.0.0.1:8000/checkout`.

**Estructura del Proyecto**

- **Controllers**
  - `app/Http/Controllers/StripeController.php`: Controlador que maneja las sesiones de Stripe y las vistas.

- **Vistas**
  - `resources/views/checkout.blade.php`: Vista que muestra el formulario de pago.

- **Rutas**
  - `routes/web.php`: Rutas para las funcionalidades de Stripe.

- **Configuración de Stripe**
  - `config/stripe.php`: Configuración de las claves de Stripe.

**Uso**

1. **Acceder a la Página de Checkout**

   Abre `http://127.0.0.1:8000/checkout` en tu navegador para ver la página de checkout.

2. **Realizar un Pago**

   Completa el formulario y haz clic en "Checkout" para ser redirigido a Stripe Checkout.

3. **Ver Confirmación de Pago**

   Después de completar el pago, serás redirigido a la página de éxito con un mensaje de confirmación.

**Contribución**

Si deseas contribuir al proyecto, por favor, realiza un fork y envía un pull request con tus cambios. Asegúrate de seguir las mejores prácticas de desarrollo.

**Licencia**

Este proyecto está licenciado bajo la Licencia MIT. Consulta el archivo `LICENSE` para más detalles.
