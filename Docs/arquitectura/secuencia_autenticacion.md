# Especificacion de Secuencia: Autenticacion de Usuario

## 1. Contexto del Flujo

Se describe la interaccion temporal entre la interfaz movil, la API backend y la base de datos para la validacion de credenciales.

## 2. Diagrama UML de Secuencia

![Diagrama de Secuencia Autenticacion](../assets/secuencia_autenticacion.png)

## 3. Detalle de los Pasos

1. El usuario ingresa sus credenciales en la aplicacion.
2. La aplicacion envia una solicitud HTTP POST al servidor.
3. El servidor valida la informacion contra la base de datos.
4. La base de datos responde con los datos del usuario.
5. El servidor genera y retorna un token de sesion `200 OK`.
6. La aplicacion muestra la pantalla principal.