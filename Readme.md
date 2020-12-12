## Gestionar la seguridad

Aplicaci�n web .NET Core que muestra los libros m�s recomendados. Tiene una p�gina de inicio de sesi�n y de registro, 
y la posibilidad de agregar libros a la biblioteca s�lo para usuarios autorizados. La aplicaci�n tiene configuraci�n 
de identidad, variedad de ajustes para la autorizaci�n. 

Tambi�n se realiza una demostraci�n de un ataque de falsificaci�n de cross-site request.

Objetivos de la aplicaci�n

- Uso de identidad.
- Agregar autorizaci�n.
- Evitar el ataque de falsificaci�n de cross-site request.


*1: Uso de identidad*

Primero se a�adiremos un entity-framework-database context a la clase LibraryContext. A continuaci�n, se habilitar� el uso 
de la identidad en la clase de inicio. Despu�s de eso, se agregar� el inicio de sesi�n y registrar� la l�gica de usuario. 
Finalmente, se recuperar� datos de la propiedad identity en la vista LendingBook.cshtml.

Las tareas son:

1. A�adir Entity Framework al contexto de la base de datos 
2. Habilitar el uso de la identidad
3. A�adir l�gica de inicio de sesi�n
4. A�adir l�gica de registro de usuarios
5. Recuperar datos de la propiedad Identity


*2: A�adir autorizaci�n*

Primero agregaremos AuthorizeAttribute a la clase LibraryController. A continuaci�n, se configurar� la autenticaci�n de la 
pol�tica basada en roles y reclamaciones. Por �ltimo se a�adir� el atributo correspondiente en las clases AccountController y LibrarianController.

Las tareas son:

1. A�adir AuthorizeAttribute a una acci�n
2. A�adir la autenticaci�n de directivas basada en roles
3. Agregar la autenticaci�n de directivas basada en notificaci�n


*3: Evitar el ataque de falsificaci�n de solicitudes entre sitios*

Lo primero que haremos es escribir el ataque de falsificaci�n de solicitudes entre sitios en un proyecto independiente. A continuaci�n, 
se ejecutar� la aplicaci�n y ver� el posible ataque. Por �ltimo, se evitar� el ataque de falsificaci�n de solicitudes entre sitios 
agregando el atributo ValidateAntiForgeryToken en la clase AccountController.

Las tareas son:

1. Escribir el ataque de falsificaci�n de solicitudes entre sitios
2. Ejecute la aplicaci�n y comprobar que el ataque es posible 
3. Evite el ataque de falsificaci�n de solicitudes entre sitios
4. Ejecute la aplicaci�n y comprobar que el ataque no es posible
