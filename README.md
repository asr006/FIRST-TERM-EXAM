# CRUD de Usuarios + Prueba de Fuerza Bruta

Este proyecto consiste en el desarrollo de una API REST utilizando FastAPI que permite realizar operaciones CRUD sobre usuarios.
Además, se realiza una prueba controlada de fuerza bruta sobre el endpoint de login para demostrar cómo las contraseñas débiles pueden ser vulnerables.

## Modelo de Usuario

El modelo User contiene los siguientes campos:

* id
* username
* password
* email (opcional)
* is_active (booleano)


## Endpoints

* **POST /users** → Crear usuario
* **GET /users** → Listar usuarios
* **GET /users/{id}** → Obtener usuario
* **PUT /users/{id}** → Actualizar usuario (sin cambiar password)
* **DELETE /users/{id}** → Eliminar usuario
* **POST /login** → Autenticación



## Cómo ejecutar la API

1. Instalar dependencias:

pip install fastapi uvicorn sqlmodel requests

2. Ejecutar el servidor:

uvicorn main:app --reload

3. Abrir en el navegador:


http://127.0.0.1:8000/docs



El archivo bruteForce.py realiza múltiples intentos de login probando diferentes contraseñas automáticamente.

Para ejecutarlo:

python bruteForce.py

El programa intentará varias combinaciones hasta encontrar la contraseña correcta.


## Resultados

Se pudo observar que el sistema permite múltiples intentos de login sin restricciones, lo que facilita que un ataque de fuerza bruta logre encontrar la contraseña.

Se registraron:

* Número de intentos
* Tiempo de ejecución
* Contraseña encontrada






