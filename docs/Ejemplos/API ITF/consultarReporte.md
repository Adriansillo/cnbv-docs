# Consultar reporte

Obtiene la información disponible de un reporte en el servidor de la ITF

**URL** : `/solicitudReportes/{id}/datos`

**Método** : `GET`

**Autenticación requerida** : Si

**Parámetros** Todos los parámetros deben ser enviados.

| Nombre|Tipo|Descripción|
| :--: |:--:| :--:|
| ```id ```| ```integer``` |Identificador de la solicitud del reporte|
| ```page```| ```integer``` |Número de página solicitada|
| ```size```| ```integer``` |Número de registros de una página|


## Respuesta exitosa

**Condición** : Si se obtuvo la información solicitada del reporte

**Código** : `200 Ok`

**Parámetros Header** Todos los parámetros deben ser enviados.

| Nombre|Tipo|Descripción|
| :--: |:--:| :--:|
| ```links```| ```string``` |Links de navegación|

**Contenido de ejemplo**

```json
[
  [
    "string",
    0,
    0
  ]
]
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