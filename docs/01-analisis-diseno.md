### Información de la Práctica

| Rol | Nombre del Integrante |
| :--- | :--- |
| **Estudiante A** | Daniela Jimenez Herrera |
| **Estudiante B** | Arath Yahir Albino Caballero |

**Fecha de inicio:** 02 de septiembre de 2026

---


1. **Descripción del problema** 

Se pretende crear un código para la representación de una pequeña planta de tanques de agua, donde el principal objetivo es su monitoreo.
Para ello, es necesario conocer de qué tanque se trata (identificación), su capacidad máxima, su nivel actual en litros y su estado de operación, el cual variará en 3: 
- Detenido. 
- Llenando. 
- Vaciando.

Las operaciones a realizar serán realizar el llenado y vaciado de un tanque, detener su operación, consultar su nivel, su porcentaje de llenado, su estado, la consulta de información de un tanque, y obtener una lectura mediante un sensor de nivel.

Las restricciones a respetar serán: 

- nivelActual >= 0
- nivelActual <= capacidadMaxima

Esto quiere decir que el nivel del agau que detectemos en el tanque debe ser siempre mayor a cero y menor que la capacidad máxima del tanque.

2. **Identificación de objetos**

En esta problemática se detectan dos objetos: El tanque y el sensor.

- Tanque: Representa justamente el tanque, con su identificación, su capacidad máxima, su nivel actual en litros y su estado de operación. Consideramos que debe existir porque la problemática misma lo requiere para saber de qué tanque dentro de la pequeña instalación estamos hablando.
- Sensor: Representa el monitoreo de cada tanque y, dependiendo de lo que detecte, realizará el llenado, vaciado o detención del tanque, al igual que mostrar su porcentaje de llenado y su estado; en pocas palabras, será el encargado de mandar información cada que el cliente requiera una consulta acerca del tanque.

3. **Estado y comportamiento**

| **Objeto propuesto** | **Responsabilidad**                             | **Información que debe conservar**                                                                              | **Comportamiento que debe realizar**                                                                                     |
|----------------------|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Tanque               | Representar un tanque dentro de la instalación. | Contendrá el identificador del tanque, su capacidad máxima, su nivel actual en litros y su estado de operación. | Representar a uno de los tanques dentro de la instalación.                                                               |
| Sensor               | Recopilar información acerca del tanque.        | Nivel de llenado del tanque                                                                                     | Llenado, vaciado y detención del tanque, mostrar al usuario su porcentaje de llenado y el estado en el que se encuentra. | 

4. **Relaciones entre los objetos**

Consideramos que ambos objetos necesitan colaborar entre sí, ya que el objeto "tanque" nos dirá de qué tanque se trata y el objeto "sensor" mandará la información de dicho tanque al usuario.


Para esto, el objeto "sensor" requiere del objeto "tanque" la identificación del tanque para saber de qué tanque se trata, su capacidad máxima para saber hasta que punto llenar, su nivel actual en litros para determinar si se llenará, vaciará o detendrá el tanque y el estado en el que se encuentra.

Esta relación es necesaria debido a que sin el objeto "tanque", el objeto "sensor" no sabrá de qué tanque requiere la información el usuario. Se podría mandar la información de un tanque determinado, por ejemplo el 1, pero no se podría acceder a los demás.

Consideramos que una de las responsabilidades que comparten ambos objetos es el estado del tanque, pero con una ligera diferencia: el objeto "tanque" muestra en qué estado está, mientras que el objeto "sensor" determina o modifica su estado actual. No se repiten como tal, pero se debe de tener cuidado para no confundirse.

