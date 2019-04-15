# TP ArquitecturaWeb


## Estacion meteorologica IoT


### Alumno: Pila Nahuel Martin


* * *

#### Introduccion

La finalidad de este trabajo es desarrollar una aplicacion que permita recopilar informacion de estaciones meteorologicas distribuidas y en base a la informacion recopilada generar graficos, alertas y enviar ordenes a dispositivos conectados para que realicen determinadas acciones.

* * *

#### Definicion de endpoints

|               | Funcion                                 | Metodo                        | Respuestas                          |
| ------------- | --------------------------------------- | ----------------------------- | ----------------------------------- |
| Estaciones		| alta (nombre,lugar,usuario,clave)				| POST /estaciones/ (body)			| 200, 201, 400, 403, 500	            |
|			| baja (id)							| DELETE /estaciones/id				| 200, 201, 403, 500	|
|			| modificacion (nombre,lugar,usuario,clave)			| PUT /estaciones/id (body)			| 200, 201, 400, 403, 500	|
| Datos meteorologicos	| alta (id_estacion,fecha,hora,temp,humedad,presion,uv,lluvia)	| POST /estaciones/datos_meteorologicos (body)	| 201, 400, 403, 500	|
| Obtener datos		| por zona							| GET /datos_meteorologicos/x			| 200, 400, 403, 404	|
|			| por fecha							| GET /datos_meteorologicos/x			| 200, 400, 403, 404	|
|			| por estacion especifica					| GET /datos_meteorologicos/x			| 200, 400, 403, 404	|
|			| por dato especifico						| GET /datos_meteorologicos/x			| 200, 400, 403, 404	|
|			| todas estaciones en un area					| GET /estaciones?campo=area			| 200, 400, 403, 404	|

* * *
