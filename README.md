🗓️ Gestor de Turnos – Proyecto Django

Este es un sistema de gestión de turnos (appointments) desarrollado con Django y Django REST Framework, pensado para administrar turnos de atención, profesionales y pacientes/usuarios de forma eficiente.
Este proyecto ofrece un backend API robusto para gestionar turnos y funciones relacionadas (usuarios, autenticación, filtros, etc.).

🚀 Tecnologías

El proyecto está basado en:
🐍 Python 3
🌐 Django 5.2
⚙️ Django REST Framework
🛠️ Bibliotecas adicionales como:
django-cors-headers para CORS
djangorestframework_simplejwt para JWT Auth
django-crispy-forms, crispy-bootstrap5 para formularios y UI
django-filter para filtros en APIs
y más según el requirements.txt

📦 Instalación (Entorno Local)

Clona el repositorio
  git <url del proyecto>
  cd gestor_turnos_proyecto

Crea y activa un entorno virtual
  python3 -m venv venv
  source venv/bin/activate   # macOS/Linux
  venv\Scripts\activate      # Windows

Instala las dependencias
  pip install -r requirements.txt

🛠️ Configuración
Variables de entorno
Crear un archivo .env en la raíz con:
  SECRET_KEY=key
  DEBUG=True
  ALLOWED_HOSTS=localhost,127.0.0.1
  DATABASE_URL=sqlite:///db.sqlite3

También podés configurar PostgreSQL u otra base de datos si lo necesitás.


🗄️ Migraciones y Base de Datos
Ejecutá las migraciones para generar las tablas:
  python manage.py migrate

👤 Creación de Superusuario
Para acceder al panel de administración Django:
  python manage.py createsuperuser

🚀 Levantar el Servidor
  python manage.py runserver


📡 Endpoints API (Ejemplos)
La API está estructurada bajo /api/ y utiliza DRF con JWT para autenticación.
| Método      | Endpoint                           | Descripción                           | Permisos |
| ----------- | ---------------------------------- | ------------------------------------- | -------- |
| GET         | `/api/medicos/`                    | Listar todos los médicos              | Admin    |
| POST        | `/api/medicos/`                    | Crear nuevo médico                    | Admin    |
| GET         | `/api/medicos/{matricula}/`        | Obtener detalle de un médico          | Admin    |
| PUT / PATCH | `/api/medicos/{matricula}/`        | Actualizar datos de un médico         | Admin    |
| DELETE      | `/api/medicos/{matricula}/`        | Eliminar un médico                    | Admin    |
| GET         | `/api/medicos/{matricula}/turnos/` | Obtener todos los turnos de un médico | Admin    |


🧪 Pruebas y Debug
Si usás Django Debug Toolbar podés activar opciones adicionales para debugging en local.

✨ ¿Querés contribuir?
Haz un fork del proyecto
Crea una rama (feature/mi-mejora)
Envía un Pull Request 🚀

Licencia
Este proyecto está bajo licencia MIT

Autor
Creado por Nicolás Dondero
