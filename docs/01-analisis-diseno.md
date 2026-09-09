1. Descripción del problema. 

El sistema que se pretende representar es una pequeña instalación de tanques de agua.
Para ello, es necesario conocer de qué tanque se trata (identificación), su capacidad máxima, su nivel actual en litros y su estado de operación, el cual variará en 3: 
- Detenido. 
- Llenando. 
- Vaciando.

Las operaciones a realizar serán realizar el llenado y vaciado de un tanque, detener su operación, consultar su nivel, su porcentaje de llenado, su estado, la consulta de información de un tanque, y obtener una lectura mediante un sensor de nivel.

Las restricciones a respetar serán: 

- nivelActual >= 0
- nivelActual <= capacidadMaxima

Esto quiere decir que el nivel del agau que detectemos en el tanque debe ser siempre mayor a cero y menor que la capacidad máxima del tanque.

2. Identificación de objetos

En esta problemática se detectan dos objetos: El tanque y el sensor.

- Tanque: Representa justamente el tanque, con su identificación, su capacidad máxima, su nivel actual en litros y su estado de operación. Consideramos que debe existir porque la problemática misma lo requiere para saber de qué tanque dentro de la pequeña instalación estamos hablando.
- Sensor: Representa el monitoreo de cada tanque y, dependiendo de lo que detecte, realizará el llenado, vaciado o detención del tanque, al igual que mostrar su porcentaje de llenado y su estado; en pocas palabras, será el encargado de mandar información cada que el cliente requiera una consulta acerca del tanque.

3. Estado y comportamiento

| **Objeto propuesto** | **Responsabilidad**                             | **Información que debe conservar**                                                                              |**Comportamiento que debe realizar**|
|----------------------|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|-|
| Tanque               | Representar un tanque dentro de la instalación. | Contendrá el identificador del tanque, su capacidad máxima, su nivel actual en litros y su estado de operación. |Representar a uno de los tanques dentro de la instalación.|
| Sensor               | Recopilar información acerca del tanque.        | Nivel de llenado del tanque                                                                                     |Llenado, vaciado y detención del tanque, mostrar al usuario su porcentaje de llenado y el estado en el que se encuentra.