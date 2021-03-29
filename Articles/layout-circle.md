`layout-circle` es un elemento primitivo que mueve un conjunto de agentes o una lista de tortugas a un círculo espaciado uniformemente de un radio determinado. La sintaxis es:

`layout-circle agentset radius`

A menudo se usa con modelos que usan enlaces porque facilita ver qué tortugas están conectadas a qué. Las tortugas crearán el círculo alrededor del centro del mundo y todas mirarán hacia afuera. `layout-circle` es un comando de observador (no llamado dentro de un `ask` ) porque actúa sobre todas las tortugas "a la vez", no solo una a la vez. Cuando se usa un conjunto de agentes, el orden de las tortugas es aleatorio, pero cuando se usa con una lista de tortugas, las tortugas se organizan en el sentido de las agujas del reloj en el orden dado comenzando en la parte superior del círculo.

El modelo siguiente muestra un uso típico de `layout-circle` en un diagrama de red.