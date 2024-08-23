# Aplicación de Datos de Vacunación con Flask, Gunicorn y Nginx

## Descripción del Proyecto
Esta aplicación web proporciona acceso a datos históricos sobre la vacunación contra el sarampión en Panamá, destinada a niños entre 12-23 meses. Utiliza Flask como framework web, Gunicorn como servidor WSGI y Nginx como servidor web frontal para manejar solicitudes y servir contenido estático.

## Características Principales
- **Interfaz Web**: Interactúa con los datos a través de una interfaz web intuitiva.
- **Consulta de Datos**: Visualiza y filtra los datos de vacunación por año.
- **Despliegue Seguro y Escalable**: Utiliza Gunicorn y Nginx para un despliegue robusto y escalable.

## Tecnologías Utilizadas
- **Flask**: Framework web para construir la aplicación.
- **Jinja2**: Motor de plantillas para renderizar vistas HTML.
- **Gunicorn**: Servidor WSGI para manejar solicitudes HTTP.
- **Nginx**: Servidor web para servir contenido estático y actuar como proxy inverso.
- **Redis**: Base de datos en memoria para almacenar y recuperar datos rápidamente.

## Estructura del Proyecto
yourapp/ ├── app/ │ ├── init.py # Configuración inicial de Flask │ ├── routes.py # Rutas de la aplicación │ ├── templates/ # Plantillas Jinja2 para la interfaz de usuario │ └── static/ # Archivos estáticos (CSS, JS) ├── config/ │ ├── nginx/ # Configuración de Nginx │ └── systemd/ # Configuración del servicio systemd para Gunicorn ├── tests/ # Pruebas unitarias ├── requirements.txt # Dependencias ├── .gitignore # Archivos excluidos de Git └── README.md # Documentación del proyecto


## Instalación y Configuración

### Requisitos Previos
- Python 3.8+
- Redis
- Nginx
- Gunicorn

### Pasos de Instalación
1. **Clonar el Repositorio**:
   ```bash
   git clone https://github.com/tu_usuario/tu_repositorio.git
   cd yourapp


## Configurar el Entorno Virtual:
- python3 -m venv venv
- source venv/bin/activate

## Ejecución de la Aplicación
- Iniciar Redis (asegúrate de que Redis esté corriendo en tu sistema).
- Ejecutar Gunicorn:
- bash
- Copy code
- gunicorn --bind 0.0.0.0:8000 app:app
