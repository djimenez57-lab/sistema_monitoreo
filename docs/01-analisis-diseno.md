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
