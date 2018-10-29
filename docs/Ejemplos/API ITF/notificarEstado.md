# Notificar estado

Recibe la notificación del estado del reporte que se encuentra en el servidor de la CNBV

**URL** : `/solicitudReportes/{id}/estadoReporte`

**Método** : `PUT`

**Autenticación requerida** : Si

**Datos de ejemplo** Todos los campos deben ser enviados.

```json
{
  "estadoReporte": "string"
}
```

## Respuesta exitosa

**Condición** : Si todo está bien y se actualizó la solicitud en el servidor de la ITF.

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

### Or

**Condición** : Si

**Código** : `403 Forbidden`

**Headers** : `{}`

**Content** : `{}`

### Or

**Condición** : Si

**Código** : `404 Not Found`

**Headers** : `{}`

**Content** : `{}`