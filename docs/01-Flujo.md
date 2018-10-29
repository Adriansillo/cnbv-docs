# Flujo de una solicitud

## Flujo 1 "Consulta":  La CNBV consulta los datos del reporte expuestos en el servidor de la ITF

### Flujo Ideal

* **1.-** La CNBV crea una "SolicituReporte" en el servidor de la ITF ([POST /api/solicitudReportes](Ejemplos/API ITF/solicitudReporte.md)) 
* **2.-** La ITF actualiza el "EstadoReporte" a "ListoParaConsultarReporte" en el servidor de la CNBV ([PUT /api/solicitudReportes/{id}/estadoReporte](Ejemplos/API CNBV/notificarEstadoCNBV.md))
* **3.-** La CNBV consulta un arreglo de "Dato" de la "SolicitudReporte" en el servidor de la ITF ([GET /api/solicitudReportes/{id}/datos](Ejemplos/API ITF/consultarReporte.md))
* **4.-** La CNBV actualiza el "EstadoReporte" a "ReporteConsultado" en el servidor de la ITF ([PUT /api/solicitudReportes/{id}/estadoReporte](Ejemplos/API ITF/notificarEstado.md))
* **5a.-** Si el reporte tiene errores: La CNBV actualiza el "EstadoReporte" a "ValidadoConErrores" en el servidor de la ITF ([PUT /api/solicitudReportes/{id}/estadoReporte](Ejemplos/API ITF/notificarEstado.md)). La ITF después de corregir el reporte volverá a ejecutar el punto 2 del proceso 
* **5b.-** Si el reporte es aceptado: La CNBV actualiza el "EstadoReporte" a "ReporteAceptado" en el servidor de la ITF ([PUT /api/solicitudReportes/{id}/estadoReporte](Ejemplos/API ITF/notificarEstado.md))


### Flujo Alterno

En caso de que la ITF no ejecute el paso 2 del **Flujo Ideal** en el tiempo que la CNBV determine se seguirá con este flujo alterno

* **2.-** La CNBV actualiza el "TipoFlujo" a "ENVIO" en el servidor de la ITF ([PUT /api/solicitudReportes/{id}/tipoFlujo](Ejemplos/API ITF/notificarTipoFlujo.md))

Una vez actualizado el "TipoFlujo" se deberá continuar con el **Flujo 2 "Envio"**


## Flujo 2 "Envio":  La ITF envía los datos del reporte al servidor de la CNBV

* **1.-** La CNBV crea una "SolicituReporte" en el servidor de la ITF ([POST /api/solicitudReportes](Ejemplos/API ITF/solicitudReporte.md)) 
* **2.-** La ITF envía un arreglo de "Dato" de la "SolicitudReporte" al servidor de la ITF (PUT /api/solicitudReportes/{id}/datos[PUT /api/solicitudReportes/{id}/datos](Ejemplos/API CNBV/recibirReporteCNBV.md))
* **3a.-** Si el reporte tiene errores: La CNBV actualiza el "EstadoReporte" a "ValidadoConErrores" en el servidor de la ITF ([PUT /api/solicitudReportes/{id}/estadoReporte](Ejemplos/API ITF/notificarEstado.md)). La ITF después de corregir el reporte volverá a ejecutar el punto 2 del proceso 
* **3b.-** Si el reporte es aceptado: La CNBV actualiza el "EstadoReporte" a "ReporteAceptado" en el servidor de la ITF ([PUT /api/solicitudReportes/{id}/estadoReporte](Ejemplos/API ITF/notificarEstado.md))