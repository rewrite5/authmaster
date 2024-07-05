# Restful Auth

API RESTful utilizando Django que permita la gestión de usuarios y la
autenticación mediante JSON Web Tokens (JWT).

### Estructura del proyecto

* api-restful
	+ authmaster
		- File.py
    + img
	+ users
		- File.py
    - README.md
    - requirements.txt
## Descripcion de directorios
- **authmaster/ ->** *incluye Archivos generales para el funcionamiento de Django.*

- **users/ ->** *desarrollo de puntos finales.*

# Configuración del proyecto API-Rest

- Paso 1: Descargar o Clonar el Proyecto

        Descargue o clone el proyecto en su máquina local.

- Paso 2: Navegar al Directorio del Proyecto

        Navegue hasta el directorio `/api-restful` del proyecto.

- Paso 3: Crear y Activar un Entorno Virtual

        Cree un entorno virtual para ejecutar e instalar dependencias.

#### Linux y macOS

* Crear entorno: `python -m venv venv`
* Activar entorno: `source venv/bin/activate`
* Instalar requisitos: `pip install -r requirements.txt`

#### Windows

* Crear entorno: `python -m venv venv`
* Activar entorno:
	+ Símbolo del sistema: `venv\Scripts\activate`
	+ PowerShell: `venv\Scriptsactivate.ps1`
* Instalar requisitos: `pip install -r requirements.txt`

para verificar que el entorno se ha iniciado correctamente se debe parecer a esto:
`(venv) nombre-usuario@dominio:~/Descargas/api-restful$ `

**Esta todo en orden para iniciar la aplicacion**
- Crear las migraciones correspondientes para inicializar la DATA BASE.
    * `python manage.py makemigrations`
    * `python manage.py migrate`

- Ejecutar el servidor
    `python manage.py runserver`

# Como utilizar  `http://127.0.0.1:8000`
 - Ruta inicial: GET - `http://127.0.0.1:8000/`

 Here are the examples in Markdown format:

### Registro de Usuario
#### `/register`
##### Método: `POST`

**Datos de entrada:**

* `username`: string (requerido)
* `password`: string (requerido)
* `email`: string (requerido)

### Login de Usuario
#### `/login`
##### Método: `POST`

**Datos de entrada:**

* `username`: string (requerido)
* `password`: string (requerido)

**Validaciones:**

Incluir en los **Headers** de la peticion.

Authorization: Token "token generado"

Ex:

Authorization: Token 53d671d12b221544ab148889747091cac654712b

### Obtener Información del Usuario
#### `/user`
##### Método: `GET`

**Autenticación**

Incluir en los **Headers** de la peticion.

Authorization: Token "token generado"

Ex:

Authorization: Token 53d671d12b221544ab148889747091cac654712b

**Respuesta:**

* Información del usuario autenticado.

### Actualizar Información del Usuario
#### `/user`
##### Método: `PUT`

**Datos de entrada:**

* `username`: string (opcional)
* `email`: string (opcional)


**Autenticación**

Incluir en los **Headers** de la peticion.

Authorization: Token "token generado"

Ex:

Authorization: Token 53d671d12b221544ab148889747091cac654712b

**Acciones:**

* Permitir actualizar el `username` y `email`.

### Eliminar Usuario
#### `/user`
##### Método: `DELETE`


**Autenticación**

Incluir en los **Headers** de la peticion.

Authorization: Token "token generado"

Ex:

Authorization: Token 53d671d12b221544ab148889747091cac654712b

**Acciones:**

* Eliminar la cuenta del usuario autenticado.
  

# Ejemplo Utilizando **Thunder Client**

![1](img/1.jpg)
<br>
<br>
<br>
![2](img/2.jpg)
<br>
<br>
<br>
![3](img/3.jpg)
<br>
<br>
<br>
![4](img/4.jpg)
<br>
<br>
<br>
![5](img/5.jpg)
<br>
<br>
<br>
![6](img/6.jpg)
<br>
<br>
<br>
![7](img/7.jpg)
<br>
<br>
<br>
![8](img/8.jpg)
<br>
<br>
<br>
![9](img/9.jpg)
