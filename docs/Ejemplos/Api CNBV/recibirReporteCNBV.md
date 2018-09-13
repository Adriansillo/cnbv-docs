# Recibir reporte

**URL** : `/api/solicitudReportes/{id}/datos`

**Método** : `PUT`

**Autenticación requerida** : Si

**Parámetros de URL** Todos los parámetros deben ser enviados.

| Nombre|Tipo|Descripción|
| :--: |:--:| :--:|
| ```id ```| ```integer``` |Identificador de la solicitud del reporte|

**Parámetros Header** Todos los parámetros deben ser enviados.

| Nombre|Tipo|Descripción|
| :--: |:--:| :--:|
| ```reporteCompletado```| ```boolean``` |Especifica si el paquete de datos es el ultimo y por tanto la transferencia del reporte se ha completado|

**Datos de ejemplo** Todos los campos deben ser enviados.

```json
{
	"id": "string",
	"cveConcepto": "string",
	"cveMoneda": 0,
	"datoImporte": "string",
	"solicitudReporte": {
		"id": "string",
		"estadoReporte": {
			"id": "string",
			"descripcion": "string",
			"nombre": "string"
		},
		"fechaRecepcion": "string",
		"numeroEnvios": 0,
		"reporte": {
			"id": "string",
			"fechaLimiteRecepcion": "string",
			"fechaSolicitud": "string",
			"periodo": {
				"id": "string",
				"fechaFin": "string",
				"fechaInicio": "string"
			},
			"tipoFlujo": {
				"id": "string",
				"descripcion": "string",
				"nombre": "string"
			},
			"tipoReporte": {
				"id": "string",
				"descripcion": "string",
				"nombre": "string"
			},
			"templateReporteCatalogoConceptos": {
				"id": "string",
				"periodicidad": "string",
				"vigenciaInicio": "string",
				"vigenciaFin": "string",
				"TemplateReporte": {
					"id": "string",
					"version": 0,
					"descripcion": "string",
					"descripcionCorta": "string",
					"elementosPorPagina": 0,
					"maxErrores": 0,
					"columnas": [
						{
							"id": "string",
							"nombre": "string",
							"min": "string",
							"max": "string",
							"requerida": true,
							"formato": "string",
							"catalogoRelacionado": "string"
						}
					]
				},
				"catalogoConceptos": {
					"id": "string",
					"version": 0,
					"conceptos": [
						{
							"id": "string",
							"concepto": "string",
							"ordenPresentacion": 0,
							"conceptoPadreId": "string"
						}
					]
				}
			}
		},
		"tipoFlujo": {
			"id": "string",
			"descripcion": "string",
			"nombre": "string"
		}
	}
}
```
## Respuesta exitosa

**Condición** : Si se registró la información recibida del reporte

**Código** : `200 Ok`

**Contenido de ejemplo**

```json
{
  "id": "string",
  "cadenaOriginal": "string",
  "fechaAcuse": "string",
  "selloDigital": "string",
  "solicitudReporte": {
    "id": "string",
    "estadoReporte": {
      "id": "string",
      "descripcion": "string",
      "nombre": "string"
    },
    "fechaRecepcion": "string",
    "numeroEnvios": 0,
    "reporte": {
      "id": "string",
      "fechaLimiteRecepcion": "string",
      "fechaSolicitud": "string",
      "periodo": {
        "id": "string",
        "fechaFin": "string",
        "fechaInicio": "string"
      },
      "tipoFlujo": {
        "id": "string",
        "descripcion": "string",
        "nombre": "string"
      },
      "tipoReporte": {
        "id": "string",
        "descripcion": "string",
        "nombre": "string"
      },
      "templateReporteCatalogoConceptos": {
        "id": "string",
        "periodicidad": "string",
        "vigenciaInicio": "string",
        "vigenciaFin": "string",
        "TemplateReporte": {
          "id": "string",
          "version": 0,
          "descripcion": "string",
          "descripcionCorta": "string",
          "elementosPorPagina": 0,
          "maxErrores": 0,
          "columnas": [
            {
              "id": "string",
              "nombre": "string",
              "min": "string",
              "max": "string",
              "requerida": true,
              "formato": "string",
              "catalogoRelacionado": "string"
            }
          ]
        },
        "catalogoConceptos": {
          "id": "string",
          "version": 0,
          "conceptos": [
            {
              "id": "string",
              "concepto": "string",
              "ordenPresentacion": 0,
              "conceptoPadreId": "string"
            }
          ]
        }
      }
    },
    "tipoFlujo": {
      "id": "string",
      "descripcion": "string",
      "nombre": "string"
    }
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