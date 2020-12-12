## Gestionar la seguridad

Aplicación web .NET Core que muestra los libros más recomendados. Tiene una página de inicio de sesión y de registro, 
y la posibilidad de agregar libros a la biblioteca sólo para usuarios autorizados. La aplicación tiene configuración 
de identidad, variedad de ajustes para la autorización. 

También se realiza una demostración de un ataque de falsificación de cross-site request.

Objetivos de la aplicación

- Uso de identidad.
- Agregar autorización.
- Evitar el ataque de falsificación de cross-site request.


*1: Uso de identidad*

Primero se añadiremos un entity-framework-database context a la clase LibraryContext. A continuación, se habilitará el uso 
de la identidad en la clase de inicio. Después de eso, se agregará el inicio de sesión y registrará la lógica de usuario. 
Finalmente, se recuperará datos de la propiedad identity en la vista LendingBook.cshtml.

Las tareas son:

1. Añadir Entity Framework al contexto de la base de datos 
2. Habilitar el uso de la identidad
3. Añadir lógica de inicio de sesión
4. Añadir lógica de registro de usuarios
5. Recuperar datos de la propiedad Identity


*2: Añadir autorización*

Primero agregaremos AuthorizeAttribute a la clase LibraryController. A continuación, se configurará la autenticación de la 
política basada en roles y reclamaciones. Por último se añadirá el atributo correspondiente en las clases AccountController y LibrarianController.

Las tareas son:

1. Añadir AuthorizeAttribute a una acción
2. Añadir la autenticación de directivas basada en roles
3. Agregar la autenticación de directivas basada en notificación


*3: Evitar el ataque de falsificación de solicitudes entre sitios*

Lo primero que haremos es escribir el ataque de falsificación de solicitudes entre sitios en un proyecto independiente. A continuación, 
se ejecutará la aplicación y verá el posible ataque. Por último, se evitará el ataque de falsificación de solicitudes entre sitios 
agregando el atributo ValidateAntiForgeryToken en la clase AccountController.

Las tareas son:

1. Escribir el ataque de falsificación de solicitudes entre sitios
2. Ejecute la aplicación y comprobar que el ataque es posible 
3. Evite el ataque de falsificación de solicitudes entre sitios
4. Ejecute la aplicación y comprobar que el ataque no es posible
