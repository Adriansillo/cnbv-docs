# Consultar reporte

.. Advertencia::

    Esta versión del API es **obsoleto**.
    Por favor, consultar el siguiente enlace :doc:``.
	
**URL** : `/api/solicitudReportes/{id}/datos`

**Método** : `GET`

**Autenticación requerida** : Si

**Parámetros de URL** Todos los parámetros deben ser enviados.

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
{
	"cveMoneda": 0,
	"id": "id",
	"cveConcepto": "cveConcepto",
	"datoImporte": "datoImporte",
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