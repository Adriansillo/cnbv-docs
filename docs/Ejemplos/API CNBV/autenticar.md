# Autenticación

Se utiliza para autenticarse en el sistema y tener acceso a los recursos del API
	
**URL** : `/authenticate`

**Método** : `POST`

**Datos de ejemplo** Todos los campos deben ser enviados.

```json
{
	"username" : "string",
	"password" : "string"
}
```
## Respuesta exitosa

**Condición** : Se validaron los datos enviados para autenticarse

**Código** : `200 Ok`

**Contenido de ejemplo**

```json
{
	"id_token": "string"
}
```

## Respuesta de error

**Condición** : Si

**Código** : `401 Unauthorized`

**Headers** : `{}`

**Content** : `{}`

### O

**Condición** : Si

**Código** : `403 Forbidden`

**Headers** : `{}`

**Content** : `{}`

### O

**Condición** : Si

**Código** : `404 Not Found`

**Headers** : `{}`

**Content** : `{}`