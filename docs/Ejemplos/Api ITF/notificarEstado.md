# Notificar estado

.. Advertencia::

    Esta versión del API es **obsoleto**.
    Por favor, consultar el siguiente enlace :doc:``.
	
Recibe la notificación del estado del reporte en el servidor de la ITF

**URL** : `/api/solicitudReportes/{id}/estadoReporte`

**Método** : `PUT`

**Autenticación requerida** : Si

**Datos de ejemplo** Todos los campos deben ser enviados.

```json
{
  "id": "string",
  "descripcion": "string",
  "nombre": "string"
}
```

## Respuesta exitosa

**Condición** : Si todo está bien y se actualizó la solicitud en el servidor de la ITF.

**Código** : `200 Ok`

**Contenido de ejemplo**

```json
{
	"cadenaOriginal": "cadenaOriginal",
	"fechaAcuse": "2000-01-23",
	"id": "id",
	"selloDigital": "selloDigital",
	"solicitudReporte": {
		"numeroEnvios": 6,
		"estadoReporte": {
			"descripcion": "descripcion",
			"id": "id",
			"nombre": "nombre"
		},
		"id": "id",
		"tipoFlujo": {
			"descripcion": "descripcion",
			"id": "id",
			"nombre": "nombre"
		},
		"fechaRecepcion": "2000-01-23",
		"reporte": {
			"fechaSolicitud": "2000-01-23",
			"periodo": {
				"fechaInicio": "2000-01-23",
				"id": "id",
				"fechaFin": "2000-01-23"
			},
			"templateReporteCatalogoConceptos": {
				"periodicidad": "periodicidad",
				"vigenciaFin": "vigenciaFin",
				"TemplateReporte": {
					"descripcion": "descripcion",
					"elementosPorPagina": 6,
					"maxErrores": 1,
					"descripcionCorta": "descripcionCorta",
					"id": "id",
					"version": 0,
					"columnas": [
						{
							"min": "min",
							"max": "max",
							"formato": "formato",
							"requerida": true,
							"id": "id",
							"catalogoRelacionado": "catalogoRelacionado",
							"nombre": "nombre"
						},
						{
							"min": "min",
							"max": "max",
							"formato": "formato",
							"requerida": true,
							"id": "id",
							"catalogoRelacionado": "catalogoRelacionado",
							"nombre": "nombre"
						}
					]
				},
				"catalogoConceptos": {
					"conceptos": [
						{
							"concepto": "concepto",
							"ordenPresentacion": 5,
							"id": "id",
							"conceptoPadreId": "conceptoPadreId"
						},
						{
							"concepto": "concepto",
							"ordenPresentacion": 5,
							"id": "id",
							"conceptoPadreId": "conceptoPadreId"
						}
					],
					"id": "id",
					"version": 5
				},
				"vigenciaInicio": "vigenciaInicio",
				"id": "id"
			},
			"fechaLimiteRecepcion": "2000-01-23",
			"tipoReporte": {
				"descripcion": "descripcion",
				"id": "id",
				"nombre": "nombre"
			},
			"id": "id",
			"tipoFlujo": {
				"descripcion": "descripcion",
				"id": "id",
				"nombre": "nombre"
			}
		}
	}
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