# Notificar estado

Recibe la notificación del estado del reporte en el servidor de la ITF

**URL** : `/api/solicitudReportes/{id}/estadoReporte`

**Método** : `PUT`

**Autenticación requerida** : Si

**Parámetros de URL** Todos los parámetros deben ser enviados.

| Nombre|Tipo|Descripción|
| :--: |:--:| :--:|
| ```id ```| ```integer``` |Identificador de la solicitud del reporte|

**Datos de ejemplo** Todos los campos deben ser enviados.

```json
{
  "estadoReporte": "string"
}
```

## Respuesta exitosa

**Condición** : Si todo está bien y se actualizó la solicitud en el servidor de la CNBV.

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