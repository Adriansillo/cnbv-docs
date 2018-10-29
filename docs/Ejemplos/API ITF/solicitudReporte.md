# Crear solicitud reporte

Se crea la solicitud del reporte en el servidor de la ITF

**URL** : `/solicitudReportes`

**Método** : `POST`

**Autenticación requerida** : Si

**Datos de ejemplo** Todos los campos deben ser enviados.

```json
{
  "id": "string",
  "nombre": "string",
  "periodo": {
    "fechaFin": "string",
    "fechaInicio": "string"
  },
  "estadoReporte": "string",
  "fechaSolicitud": "string",
  "fechaLimiteRecepcion": "string",
  "fechaCambioFlujoEnvio": "string",
  "tipoReporte": "string",
  "tipoFlujo": "string",
  "TemplateReporte": {
    "clavetemplate": "string",
    "descripcionCorta": "string",
    "elementosPorPagina": 0,
    "columnas": [
      {
        "nombre": "string",
        "tipodato": "string",
        "orden": 0,
        "requerida": true,
        "formato": "string",
        "min": "string",
        "max": "string",
        "catalogoRelacionado": "string"
      }
    ]
  },
  "CatalogoConceptos": {
    "claveCatalogoConceptos": "string",
    "descripcionCorta": "string",
    "conceptos": [
      {
        "claveConcepto": "string",
        "conceptoNombre": "string",
        "ordenPresentacion": 0,
        "conceptoPadreId": "string"
      }
    ]
  }
}
```

## Respuesta exitosa

**Condición** : Si todo está bien y se registró la solicitud en el servidor de la ITF.

**Código** : `201 Created`

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