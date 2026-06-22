| FUNCIONALES (mínimo 5)                                                                                                                                                                                                                                                                                                                           | NO FUNCIONALES (mínimo 5)                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RF:  Autenticar usuarios con usuario y contraseña <br> RF:  Registrar y validar cuentas bancarias (10 dígitos,banco registrado) <br> RF:  Consultar el saldo de una cuenta por el cliente <br> RF:  Realizar depósitos a una cuenta  <br> RF:  Generar reporte tributario en PDF para el cliente <br> RF:  Enviar reporte a la DIAN en formato JSON |RNF: Seguridad: autenticación con tokens JWT <br> RNF: Disponibilidad: 99.5% uptime mensual <br> RNF: Rendimiento: respuesta < 2 segundos por operación <br> RNF: Escalabilidad: soportar 10.000 usuarios concurrentes <br> RNF: Auditabilidad: log de todas las transacciones 
| RF: crear clientes| RNF: El servicio debe estar operativo las 24 horas del día, los 7 días de la semana, salvo mantenimientos programados.
|RF: activar clientes | RNF: la aplicación debe cumplir con estándares de accesibilidad para que pueda ser utilizada por personas con discapacidades visuales o motoras.
|RF: Consultar Movimientos  | RNF: Ser compatible con diferentes sietemas operativos y navegadores web modernos.
|RF: Recibir notificaciones | RNF: RNF: El sistema debe poder restaurar la información y continuar operando después de una falla crítica.         
| RF: Realizar pagos de servicios  | RNF: las actualizaciones del sistema no deben afectar el funcionamiento de las funciones existentes.


## PREGUNTA DE ANÁLISIS
a. ¿Identifica algún requerimiento que deba detallarse más? ¿Cuál(es)? ¿Por qué?

Sí. Algunos requerimientos necesitan más detalle para evitar ambigüedades:

- RF: Recibir notificaciones, porque no especifica si serán por correo electrónico, SMS o notificaciones dentro de la aplicación.

- RF: Consultar movimientos, porque no indica si existe un límite de fechas, filtros o cantidad máxima de registros.

- RNF: Recuperar la información después de una falla crítica, porque no define el tiempo máximo permitido para la recuperación ni la cantidad de datos que podrían perderse.

b. ¿Existen requerimientos que se contradigan entre sí? ¿Cuáles?

No se observan contradicciones directas entre los requerimientos. Sin embargo, existe una posible redundancia entre:

- RNF: Disponibilidad del 99.5% de uptime mensual.
- RNF: El servicio debe estar operativo las 24 horas del día, los 7 días de la semana, salvo mantenimientos programados.

Ambos hacen referencia a la disponibilidad del sistema y podrían unificarse en un solo requerimiento para evitar duplicidad.

c. Si tuviera que dar prioridad, ¿cuáles serían los 2 más importantes para una primera iteración? Justifique.
- RF: Autenticar usuarios con usuario y contraseña.

Es fundamental para garantizar que solo los clientes autorizados puedan acceder a sus cuentas y realizar operaciones.
- RF: Consultar el saldo de una cuenta por el cliente.

Es una de las funciones principales que esperan los usuarios de una aplicación bancaria y aporta valor desde las primeras versiones del sistema.

d. ¿Existe algún requerimiento que NO debería realizarse en el MVP? ¿Por qué?

Sí. RF: Generar reporte tributario en PDF para el cliente y RF: Enviar reporte a la DIAN en formato JSON podrían dejarse para una fase posterior. Estas funcionalidades son especializadas y no son esenciales para que el usuario pueda utilizar las funciones básicas del banco, como iniciar sesión, consultar su saldo o realizar transacciones. Implementarlas después permitiría lanzar un MVP más rápido y enfocado en las necesidades principales.
