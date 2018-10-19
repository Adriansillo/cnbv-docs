# Consultar información del reporte


.. Advertencia::

    Esta versión del API es **obsoleto**.
    Por favor, consultar el siguiente enlace :doc:``.
	

**URL** : `/api/reportes/{id}`

**Método** : `GET`

**Autenticación requerida** : Si

**Parámetros** Todos los parámetros deben ser enviados.

| Nombre|Tipo|Descripción|
| :--: |:--:| :--:|
| ```id ```| ```integer``` |Identificador de la solicitud del reporte|



## Respuesta exitosa

**Condición** : Si se obtuvo la información del reporte

**Código** : `200 Ok`

**Contenido de ejemplo**

```json
{
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