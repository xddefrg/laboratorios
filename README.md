#Lab 9 - classroomhub
Sitio web educativo desarrollado con Django y respaldado por una base de datos MySQL/MariaDB. Cuenta con un catálogo público de recursos educativos, registro de usuarios, inicio y cierre de sesión, un panel privado y una página de revisión del catálogo restringida a un grupo mediante permisos.

Versiones
Python 3.15 (probado en Windows).

Django 6.1.3.

MariaDB (probado con las versiones 13.0.2 y 13.1.1). Django 6.1 requiere MariaDB 10.11 o superior, o MySQL 8.4 o superior.

Configuración inicial
Crea y activa un entorno virtual. Luego, instala las dependencias:


bash
py -m venv .venv
.venv\Scripts\activate
py -m pip install -r requirements.txt
Crea la base de datos y una cuenta SQL (reemplaza CHANGE_ME por tu contraseña):


sql
CREATE DATABASE classroom_hub CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
CREATE USER 'classroomhub_user'@'localhost' IDENTIFIED BY 'CHANGE_ME';
CREATE USER 'classroomhub_user'@'127.0.0.1' IDENTIFIED BY 'CHANGE_ME';
GRANT ALL PRIVILEGES ON classroom_hub.* TO 'classroomhub_user'@'localhost';
GRANT ALL PRIVILEGES ON classroom_hub.* TO 'classroomhub_user'@'127.0.0.1';
GRANT ALL PRIVILEGES ON test_classroom_hub.* TO 'classroomhub_user'@'localhost';
GRANT ALL PRIVILEGES ON test_classroom_hub.* TO 'classroomhub_user'@'127.0.0.1';
Copia el archivo .env.example y renómbralo como .env. Configura en él la misma contraseña. Nunca subas el archivo .env al repositorio.

Ejecuta las migraciones y crea un usuario administrador:


bash
python manage.py migrate
python manage.py createsuperuser
Ejecución del proyecto

bash
python manage.py check
python manage.py runserver
Rutas del sitio
Ruta

Acceso

/

Página de inicio pública

/resources/

Catálogo público

/about/

Página pública

/accounts/signup/

Registro público (solo cuentas de usuario normales)

/accounts/login/

Inicio de sesión público

/accounts/logout/

Solo permite solicitudes POST; las solicitudes GET devuelven el código 405

/dashboard/

Requiere iniciar sesión

/resources/review/

Requiere iniciar sesión y tener el permiso pages.view_resource (de lo contrario, devuelve un error 403)

/admin/

Acceso exclusivo para personal autorizado

Grupo de revisores
En el panel de administración de Django (Django Admin), abre la sección Groups (Grupos) y crea un grupo llamado Catalog reviewers con el siguiente permiso:

pages | resource | Can view resource

Después, abre el perfil de un usuario y agrégalo a ese grupo.

Los usuarios que pertenezcan al grupo de revisores no obtendrán permisos de personal administrativo (staff) automáticamente.

Pruebas

bash
python manage.py test pages
Las pruebas se ejecutan utilizando una base de datos independiente llamada test_classroom_hub. Por lo tanto, la cuenta SQL necesita tener permisos sobre ella.

Funcionalidades no incluidas
Creación, edición y eliminación públicas de recursos.

Recuperación de contraseñas mediante correo electrónico, autenticación OAuth y autenticación multifactor (MFA).

Configuraciones para entornos de producción.
