# Notificar cambio de flujo

Recibe la notificación del cambio de flujo a seguir para el reporte solicitado

**URL** : `/solicitudReportes/{id}/flujoReporte`

**Método** : `PUT`

**Autenticación requerida** : Si

**Parámetros de URL** Todos los parámetros deben ser enviados.

| Nombre|Tipo|Descripción|
| :--: |:--:| :--:|
| ```id ```| ```integer``` |Identificador de la solicitud del reporte|

**Datos de ejemplo** Todos los campos deben ser enviados.

```json
{
  "flujoReporte": "string"
}
```

## Respuesta exitosa

**Condición** : Si todo está bien y se actualizó el tipo de flujo de la solicitud en el servidor de la ITF.

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