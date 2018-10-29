# Recibir reporte

Recibe los datos de un reporte regulatorio según la especificación de la solicitud

**URL** : `/solicitudReportes/{id}/datos`

**Método** : `PUT`

**Autenticación requerida** : Si

**Parámetros de URL** Todos los parámetros deben ser enviados.

| Nombre|Tipo|Descripción|
| :--: |:--:| :--:|
| ```id ```| ```integer``` |Identificador de la solicitud del reporte|

**Parámetros Header** Todos los parámetros deben ser enviados.

| Nombre|Tipo|Descripción|
| :--: |:--:| :--:|
| ```reporteCompletado```| ```boolean``` |Especifica si el paquete de datos es el último y por tanto la transferencia del reporte se ha completado|

**Datos de ejemplo** Todos los campos deben ser enviados.

```json
[
  [
    "string",
    0,
    0
  ]
]
```
## Respuesta exitosa

**Condición** : Si se registró la información recibida del reporte

**Código** : `200 Ok`

**Contenido de ejemplo**

```json
{
  "idSolicitudReporte": "string",
  "cadenaOriginal": "string",
  "selloDigital": "string",
  "estadoReporte": "string",
  "fechaAcuse": "string"
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