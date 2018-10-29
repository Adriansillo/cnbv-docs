# Consultar información de la solicitud de un reporte 

Consulta la información de la solicitud de un reporte con base al identificador

**URL** : `/solicitudReportes/{id}`

**Método** : `GET`

**Autenticación requerida** : Si

**Parámetros** Todos los parámetros deben ser enviados.

| Nombre|Tipo|Descripción|
| :--: |:--:| :--:|
| ```id ```| ```integer``` |Identificador de la solicitud del reporte|



## Respuesta exitosa

**Condición** : Si se obtuvo la información de la solicitud del reporte

**Código** : `200 Ok`

**Contenido de ejemplo**

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