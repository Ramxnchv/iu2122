# iu2122

Servidor y código de plantilla para una interfaz de gestión de valoraciones de películas, a usar para las prácticas de la asignatura *Interfaces de Usuario* de los grados de Informática de la Universidad Complutense, en su edición 2021-22.

## Participantes

- Ramón Rosa
- Pedro Martínez
- Sergio Lorente
- Beatriz Ortega
- Julio Martínez

## Cambios realizados por nosotros

### index.html

Esta es la página web principal. En ella se hace un breve resumen sobre la utilidad de la aplicación. Se ha creado un timer para que cuando pase un tiempo, se muestre automáticamente el modal del login.

### Header

Hemos modificado el header, en concreto los dropdowns que se muestran en cada uno de los apartados.
Anteriormente se mostraban de la siguiente forma:
- Películas
  - Añadir película
  - Borrar película
  - Modificar película
  - Ver catálogo
  - Buscar película por
- Grupos

Hemos eliminado varios submenús y añadidos otros ahora se muestran de la siguiente forma:

- Ver todas las películas
- Añadir películas
- Ver grupos
- Crear grupo

Esto lo hemos hecho debido a que el resto de campos no eran necesarios, ya que se puede acceder a ellos de forma más intuitiva, por ejemplo al estar viendo una película en concreto. 

### Login

Añadido botón para hacer login, mostrando un formulario en el que introducir usuario y contraseña. Si ya has iniciado sesión te muestra `Holi ${nombre}`.

### Añadir película

Ahora las películas se añaden a través de un modal, es decir, no hay una página en concreto para añairla. Al modal se puede acceder a través del header. Se ha de estar logueado y ser ADMIN para poder crear una película.

### Crear grupo

Ahora los grupos se crean a través de un modal, es decir, no hay una página en concreto para crearlos. Al modal se puede acceder a través del header. Se ha de estar logueado en la página para poder crear un grupo.

### Crear usuario

Ahora los usuarios se crean a través de un modal, es decir, no hay una página en concreto para crearlos. Al modal se puede acceder a través del header. Se puede crear un usuario sin estar logueado en la página.

### Ver películas

Hemos cambiado la forma en la que se muestran las películas. Ahora se muestran mediante tarjetas. Esto favorece que el usuario vea la información más claramente.

### Ver grupos

Página donde aparecen listados los grupos, junto con sus usuarios, y cantidad de requests.

### Ver película

Al hacer clic sobre una película, abre un modal con la información de la misma.

### Ver usuarios

Página donde aparecen listados todos los usuarios.

## Práctica

Implementa la interfaz que propusiste en tu Práctica 5 (Diseño de una GUI) usando Boostrap 5, *sin* JQuery. Tendrás que usar
- HTML
- JavaScript
- CSS

Para ello, haz un "fork" de este proyecto, y toca únicamente los siguientes ficheros y directorios (todos ellos bajo [main/src/main/resources/static](https://github.com/manuel-freire/iu2122/blob/main/src/main/resources/static/)):
- [index.html](https://github.com/manuel-freire/iu2122/blob/main/src/main/resources/static/index.html), donde escribirás todo el HTML estático (es decir, el que existe al cargar la página, en lugar de generarse dinámicamente vía `pmgr.js`)
- [js/pmgr.js](https://github.com/manuel-freire/iu2122/blob/main/src/main/resources/static/js/pmgr.js), donde escribirás todo el JS que genera HTML y realiza peticiones a la [API](https://github.com/manuel-freire/iu2122/blob/main/src/main/resources/static/js/pmgrapi.js) para interactuar con el servidor. *Por favor, no modifiques la API en sí*.
- [css/custom.css](https://github.com/manuel-freire/iu2122/blob/main/src/main/resources/static/css/custom.js), donde escribirás reglas CSS para estilar tu página tal y como quieres, modificando los estilos por defecto de Bootstrap 5.
- Puedes incorporar css/scripts/imágenes en sus respectivas carpetas (`css`, `js`, `img`). **Evita** introducir dependencias a código externo, entendido como código que cargas de fuera de tu aplicación. Sí puedes (si su licencia lo permite) introducir dependencias copiándolas a las respectivas carpetas, previa consulta al profesor.

### Entorno de desarrollo

Necesitarás un servidor local para lanzar tu página. Hay muchos disponibles:
- si tienes PHP instalado, puedes, desde la carpeta `static`, lanzar `php -S localhost:8000` (y luego abres un navegador apuntando a localhost:8000`)
- si tienes Python3 instalado, puedes usar, desde la carpeta `static`, `python -m http.server 8000` (y luego abres un navegador apuntando a localhost:8000`)
- (recomendado) si usas VS Code, puedes instalar la extensión "Live Server", y lanzar el servidor vía click derecho desde `index.html` + `Open with Live Server`.

## Resto del código

La aplicación de servidor funciona con Spring Boot, y puedes lanzarla en local y/o jugar con ella libremente. Para lanzarla, necesitarás tener `maven` y una JDK >= 8.0 instaladas. Basta con ejecutar `mvn spring-boot:run` para lanzar todo en local. Archivos importantes:
- Configuración de la aplicación: [application.properties](https://github.com/manuel-freire/iu2122/blob/main/src/main/resources/application.properties)
- Contraseñas y contenido inicial de la BD: [import.sql](https://github.com/manuel-freire/iu2122/blob/main/src/main/resources/import.sql)

*El profesor proporcionará un servidor (con configuración cambiada con respecto a la anterior) que permanecerá encendido hasta el fin de las prácticas de la asignatura. Lanzar o no otro servidor en local, o jugar con el codigo, es completamente opcional. Ver [licencia](https://github.com/manuel-freire/iu2122/blob/main/LICENSE)*



