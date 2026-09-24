# Politicas y Protocolos de Seguridad del Sistema

## 1. Control de Accesos y Roles (RBAC)

El sistema aplica un esquema de Control de Acceso Basado en Roles para restringir operaciones sensibles:
* **Rol Cliente:** Acceso unicamente a lectura de productos y gestion de su propio carrito.
* **Rol Pasarela de Pagos:** Integracion via tokens cifrados para procesamiento de cobros.
* **Rol Administrador:** Acceso total a reportes, facturacion y modificacion de inventario.

## 2. Encriptacion de Datos Sensibles

* Todas las contraseñas de los usuarios se almacenan encriptadas con el algoritmo **Bcrypt** (factor de costo 10).
* Todas las transmisiones web se ejecutan obligatoriamente sobre el protocolo **HTTPS (TLS 1.3)**.

## 3. Autenticacion mediante Tokens

* La API emite firma digital mediante **JWT (JSON Web Tokens)** con tiempo de vida util de 8 horas.