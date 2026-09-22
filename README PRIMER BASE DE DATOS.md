# Tarea: Instalación de PostgreSQL con Docker, Configuración de DataGrip y Creación de Base de Datos

Este repositorio contiene la documentación y guía paso a paso para desplegar un contenedor de PostgreSQL utilizando Docker, configurarlo como gestor de base de datos en DataGrip (JetBrains) y crear la primera base de datos.


## 🚀 Guía Paso a Paso

### Paso 1: Instalar Docker

1. Se descarga e instala [Docker Desktop]
2. Se inicia Docker Desktop y se verifica que el motor de contenedores esté en ejecución.

### Paso 2: Descargar e iniciar PostgreSQL en Docker

1. Se abre una terminal (PowerShell, Command Prompt o Bash) y ejecuta el siguiente comando:

```
docker run --name postgres-db -e POSTGRES_PASSWORD=yourpassword -p 5432:5432 -d postgres
```

2. Se verifica que el contenedor esté activo ejecutando:

```
docker ps
```

### Paso 3: Instalar DataGrip

1. Se descarga e instala DataGrip desde el sitio oficial de [JetBrains DataGrip]
2. Se registra e inicia sesión con tu licencia estudiante/gratuita utilizando tu correo institucional de la UMG.

### Paso 4: Configuración de Conexión en DataGrip

1. Se abre DataGrip y nos dirigimos a: `File` > `Data Sources and Drivers`
2. Hacemos clic en el botón de `+` (Añadir) y seleccionamos PostgreSQL.
3. Configuramos los parámetros de conexión:
   * Host: `localhost`
   * Port: `5432`
   * User: `postgres`
   * Password: `yourpassword`
   * Database: `postgres`
4. Hacemos clic en Test Connection para validar el acceso. Si falta algún controlador, hacemos clic en Download Driver.

### Paso 5: Crear tu primera Base de Datos

1. Abrimos una nueva consola SQL en DataGrip haciendo clic derecho en la conexión > `New` > `Console`.
2. Escribimos y ejecutamos la siguiente sentencia SQL:

```sql
CREATE DATABASE my_first_database WITH TEMPLATE template0;
```
