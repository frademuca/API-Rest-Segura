# API-Rest-Segura
Proyecto final primer trimestre


## NOMBRE:
APP TAREAS DEL HOGAR


## IDEA:
API Rest para la gestión de tareas del hogar asociadas a un usuario en un domicilio. Se podrán consultar los datos de los usuarios, así como sus tareas del hogar y direcciones asociadas. Constará de 3 tablas; usuarios, tareas y direcciones.


## JUSTIFICACIÓN:
La aplicación permitirá la gestión de las tareas del hogar de distintos usuarios en uno o varios domicilios.


## TABLAS DEL PROYECTO:
### USUARIOS
- userName - String [Unique, Not null, Primary Key]
- nombre - String [Not null]
- apellidos - String [Not null]
- password - String [Not null, Longitud 8-20]
- email  - String [Not null, Unique, Formato (...@...)]
- roles - String [Not null, (User / Admin)]

### TAREAS
- idTarea  - Long [Autoincrement, Primary Key]
- userName - String [Unique, Not null, Foreign Key]
- nombre - String [Not null]
- descripcion- String [Not null]
- estado: Boolean [Por defecto false]
- fechaFinalizacion - Date [No antes de hoy]

### DIRECCIONES
- idDireccion  - Long [Autoincrement, Primary Key]
- userName - String [Unique, Not null, Foreign Key]
- calle - String [Not null]
- numero - String [Not null]
- codigoPostal - String [Not null]
- municipio -  String [Not null]
- provincia- String [Not null]


## ¿QUÉ DATOS NECESITAMOS PARA: ?
- Login: userName, password
- Registro usuario: nombre, apellido, email. password, repitePassword, userName
- Ver una tarea: nombre, descripción, fechaFinalizacion, estado
- Registrar una tarea: nombre, descripcion, fechaFinalizacion
- Borrar una tarea: idTarea
- Actualizar el estado de una tarea: idTarea, estado
- Registrar una tarea como ADMIN: idTarea, nombreUsuario
