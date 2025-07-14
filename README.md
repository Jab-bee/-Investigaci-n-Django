# 📚 Sistema de Gestión de Libros (Django)

Este es un proyecto creado con Django que permite realizar operaciones CRUD (Crear, Leer, Actualizar, Eliminar) sobre un catálogo de libros.

---

## 🚀 Funcionalidades

- Agregar nuevos libros con título, autor, ISBN y descripción.
- Listar todos los libros registrados.
- Editar la información de un libro.
- Eliminar libros del sistema.
- Panel administrativo con autenticación integrada de Django.

---

## 🛠 Tecnologías utilizadas

- Python 3.13
- Django 4.x
- SQLite (base de datos por defecto)
- HTML + Bootstrap (para los templates)

---

## 🧪 Instalación local

1. Clona el repositorio:

```bash
git clone https://github.com/Jab-bee/-Investigaci-n-Django.git
cd -Investigaci-n-Django




Por Jabeich Andres Benavides: 

1. ¿Qué es CRUD y cuál es su propósito en el desarrollo de aplicaciones web?

CRUD es un acrónimo que representa las cuatro operaciones básicas de almacenamiento persistente en una base de datos: Crear, Leer, Actualizar y Eliminar. Su propósito principal es permitir a los usuarios interactuar con los datos de una aplicación de forma integral y controlada. Casi cualquier aplicación web que gestione información (como usuarios, productos o tareas) requiere la implementación de estas operaciones para funcionar eficazmente. Por ejemplo, en una aplicación de gestión de tareas (lista de tareas pendientes), CRUD permite a los usuarios crear nuevas tareas, ver la lista existente, editar las tareas guardadas y eliminar las que ya no son necesarias.

2. ¿Cuáles son los patrones arquitectónicos en el desarrollo de software?
Los patrones arquitectónicos son estructuras de diseño que organizan el código de una aplicación para mejorar su mantenibilidad, escalabilidad y reutilización. Estos patrones separan las responsabilidades entre los diferentes componentes del sistema, evitando que una sola parte gestione múltiples tareas.

Patrón MVC (Modelo-Vista-Controlador):

Modelo: Gestiona la lógica de los datos y las reglas de negocio (p. ej., la conexión a la base de datos).

Vista: Gestiona la interfaz de usuario (presentación de datos).

Controlador: Interpreta las acciones del usuario (p. ej., clics o envíos de formularios) y actualiza el modelo o la vista en consecuencia.

Patrón MVT (Modelo-Vista-Plantilla):

Modelo: Define la estructura de la base de datos y la lógica de negocio (similar a MVC).

Vista: Contiene la lógica que procesa las solicitudes HTTP y devuelve las respuestas (actuando como controlador).

Plantilla: Archivos HTML que representan la presentación de los datos (equivalente a la "Vista" en MVC).

Diferencias clave entre MVC y MVT:
En MVC, la Vista es la capa de presentación y el Controlador gestiona el flujo de datos. En MVT (usado por Django), la Vista funciona como controlador, mientras que la Plantilla asume la función de presentación visual. Django utiliza oficialmente el patrón MVT.


3. ¿Cómo se estructura un proyecto de Django?
Un proyecto de Django se organiza en cuatro componentes principales:

Modelos (models.py): Definen tablas y campos de la base de datos mediante clases de Python.

Vistas (views.py): Procesan solicitudes HTTP, acceden a los modelos y devuelven respuestas (p. ej., renderizan plantillas).

Plantillas: Archivos HTML (ubicados en la carpeta templates/) que muestran información dinámica al usuario.

URL (urls.py): Asignan rutas de aplicación (p. ej., /tasks/) a vistas específicas.

Uso de {% %} en plantillas:

Estos delimitadores ejecutan la lógica de las plantillas de Django, como bucles o condicionales. Por ejemplo:

{% for task in tasks %}
  <li>{{ task.title }}</li>
{% endfor %}

4. ¿Cuál es el flujo de datos entre un formulario HTML y la base de datos en Django?

El flujo sigue estos pasos:

Un usuario envía un formulario HTML (vía POST).

La vista de Django recibe la solicitud y los datos del formulario.

La información se valida mediante un formulario o un ModelForm.

Si los datos son válidos:

Se guardan en el modelo asociado.

El modelo persiste los datos en la base de datos.

La vista redirige a una página de confirmación o muestra errores si la validación falla.


5. ¿Qué herramientas o comandos ofrece Django para facilitar el desarrollo CRUD?
Django incluye comandos y utilidades clave:

startproject: Crea un nuevo proyecto.

startapp: Genera una aplicación dentro del proyecto.

makemigrations: Prepara los cambios del modelo para la base de datos.

migrate: Aplica las migraciones pendientes.

runserver: Inicia un servidor de desarrollo local.

ModelForm: Genera formularios automáticamente a partir de los modelos.

admin: Interfaz administrativa predefinida.

createsuperuser: Crea un usuario con acceso al panel de administración.

6. ¿Cómo funciona Django Admin?

Django Admin es una interfaz web automatizada para la gestión de modelos. Permite realizar operaciones CRUD sobre los datos sin crear vistas manuales. Para usarlo:

Registre los modelos en admin.py mediante admin.site.register(Model).

Cree un superusuario con python manage.py createsuperuser.

Al acceder a /admin/, el superusuario puede:

Crear, leer, actualizar o eliminar registros;

Administrar los permisos de usuario;

Filtrar y buscar datos.
Esta herramienta es ideal para la creación rápida de prototipos y la administración interna
