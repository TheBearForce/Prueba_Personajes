# Prueba_Personajes
esta en dos partes la base de datos y en Visual estudio se dejara un readmy para la creacion de la base

Introducción
El presente informe documenta el desarrollo de una aplicación Web API utilizando el framework ASP.NET Core, junto con Entity Framework Core como tecnología de acceso a datos. El objetivo principal es gestionar una entidad llamada Personaje, la cual representa un personaje dentro de un sistema, permitiendo su almacenamiento, consulta e inserción en una base de datos SQL Server.
Herramientas y tecnologías
•	Visual Studio 2022
•	ASP.NET Core 6/7
•	Entity Framework Core
•	SQL Server (SQLEXPRESS)
•	Swagger para pruebas de endpoints
•	C# como lenguaje principal
Modelado de la Entidad 
Se modeló una clase llamada PersonajeModel con las siguientes propiedades:

![image](https://github.com/user-attachments/assets/0b8c6c97-f057-47f5-9468-1e6baf1dfb11)

 
Esta clase se encuentra dentro del namespace Personaje.Models y se mapea a una tabla de base de datos mediante Entity Framework.
Configuración de la base de datos
Se creó la base de datos y la tabla mediante el siguiente script SQL
También se insertaron datos de prueba:

![image](https://github.com/user-attachments/assets/07f788d9-f358-4167-b279-c21ee7c31637)

 
Configuración de la conexión a SQL Server
La cadena de conexión fue agregada en el archivo appsettings.json:

![image](https://github.com/user-attachments/assets/d168cead-576a-4ba8-bbc6-b9abe34c1c09)

 
Y registrada en Program.cs:

![image](https://github.com/user-attachments/assets/b3be8322-c2e4-4007-ba74-ef2a249b06f0)

 
Configuración del DbContext

![image](https://github.com/user-attachments/assets/39505e1a-0cb9-48e7-8c5e-4027b89ccf0f)

 
Este contexto se encarga de gestionar la comunicación con la base de datos.

![image](https://github.com/user-attachments/assets/9a362d77-1fe5-40fa-bffd-e65825689b9a)







Desarrollo del controlador API
Se implementó el controlador PersonajesController.cs con los métodos básicos GET y POST:
 

Pruebas con Swagger
Se utilizó la herramienta Swagger UI (habilitada por defecto en el proyecto) para probar la funcionalidad de la API:
•	GET /api/personajes muestra todos los personajes almacenados.
•	POST /api/personajes permite insertar un nuevo personaje.  
![image](https://github.com/user-attachments/assets/24e10293-85d9-4ad1-9745-bd11e931b4fe)


Conclusión
La implementación de esta API demostró el uso práctico de ASP.NET Core junto con Entity Framework para construir una aplicación robusta, modular y fácil de mantener. Se logró una correcta conexión a SQL Server, el modelado de datos, y la exposición de endpoints REST funcionales. Además, se probaron satisfactoriamente con datos reales usando Swagger.
Este proyecto sirve como base para aplicaciones más complejas que requieran persistencia de datos y una estructura sólida en capas.

