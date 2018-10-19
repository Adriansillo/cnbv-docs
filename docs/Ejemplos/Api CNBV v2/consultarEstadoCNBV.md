# Consultar estado

.. Advertencia::

    Esta versión del API es **obsoleto**.
    Por favor, consultar el siguiente enlace :doc:``.
	
**URL** : `/api/solicitudReportes/{id}/estadoReporte`

**Método** : `GET`

**Autenticación requerida** : Si

**Parámetros de URL** Todos los parámetros deben ser enviados.

| Nombre|Tipo|Descripción|
| :--: |:--:| :--:|
| ```id ```| ```integer``` |Identificador de la solicitud del reporte|

## Respuesta exitosa

**Condición** : Si se obtuvo el estado del reporte

**Código** : `200 Ok`

**Contenido de ejemplo**

```json
{
	"descripcion": "descripcion",
	"id": "id",
	"nombre": "nombre"
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