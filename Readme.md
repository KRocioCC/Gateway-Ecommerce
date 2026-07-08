# API Gateway

## Seguridad con Keycloak

El API Gateway utiliza Keycloak para la autenticación mediante OAuth2 y JWT y  protege las rutas del sistema mediante autenticación con JWT.

Cuando un usuario inicia sesión, Keycloak genera un token. Ese token se envía en cada petición al Gateway usando el siguiente header:

```text
El Gateway valida el token antes de permitir el acceso a los microservicios.

Realm utilizado: 
ecommmerce-realm

Cliente utilizado:
api-gateway-client

Endpoint de configuración OpenID:
http://localhost:8080/realms/ecommmerce-realm/.well-known/openid-configuration

Este endpoint permite que Spring Security obtenga la configuración necesaria de Keycloak para validar tokens JWT.

Roles usados:

El sistema maneja dos roles principales:

USER: puede realizar compras y crear órdenes.
ADMIN: puede administrar productos, inventario e imágenes.
```
