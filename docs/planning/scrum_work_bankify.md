| Nivel | Nombre | ID en Jira | Descripción |
|-------|--------|------------|-------------|
| **Épica** | Gestión de Transferencias Bancarias — Bankify | **DOSW-1** | Permitir a los usuarios realizar transferencias de dinero de forma segura, tanto entre cuentas propias como hacia terceros, ofreciendo seguimiento y mecanismos de protección contra fraudes. |
| **Historia de usuario 1** | Transferencia entre cuentas propias | **DOSW-2** | Como usuario de Bankify, quiero transferir dinero entre mis propias cuentas para gestionar mis fondos sin ir a una sucursal. <br> **Criterios de aceptación:** <br> Ver todas mis cuentas con saldo disponible <br> Confirmar la transferencia con PIN o biometría <br> Recibir notificación de éxito o error |
| **Historia de usuario 2** | Transferencia a terceros | **DOSW-3** | Como usuario de Bankify, quiero enviar dinero a otros bancos para pagar a personas fuera de mi red. <br> **Criterios de aceptación:** <br> Ingresar número de cuenta, banco y titular <br> Validar datos antes de ejecutar. <br> Guardar destinatarios frecuentes. |
| **Historia de usuario 3** | Historial de transferencias | **DOSW-4** | Como usuario de Bankify, quiero ver el historial de mis movimientos para controlar mis finanzas personales. <br> **Criterios de aceptación:** <br> Filtrar por fecha, monto o tipo <br> Descargar comprobante en PDF <br> Ver estado de cada transacción (pendiente, completada, fallida) |
| **Historia de usuario 4** | Límites y seguridad de transferencias | **DOSW-5** | Como usuario de Bankify, quiero configurar límites diarios de transferencia para proteger mi dinero ante fraudes. <br> **Criterios de aceptación:** <br> Establecer monto máximo diario <br> Recibir alerta si se supera el límite <br> Solicitar desbloqueo temporal con verificación adicional |
| **Tarea 1.1** | Diseñar pantalla de selección de cuenta origen/destino | **DOSW-6** | Diseñar la interfaz gráfica que permita al usuario visualizar y seleccionar las cuentas de origen y destino disponibles para realizar una transferencia interna, garantizando una experiencia intuitiva y fácil de usar. |
| **Tarea 1.2** | Desarrollar endpoint REST para transferencia interna | **DOSW-7** | Implementar un servicio REST encargado de procesar las transferencias entre cuentas propias, validando la existencia de las cuentas y actualizando los saldos correspondientes de manera segura. |
| **Tarea 1.3** | Implementar notificación push de confirmación | **DOSW-8** | Desarrollar el mecanismo de notificaciones que informe al usuario sobre el resultado de la transferencia realizada, indicando si la operación fue exitosa o si ocurrió algún error. |
| **Tarea 2.1** | Crear formulario de destinatario con validación en tiempo real | **DOSW-9** | Diseñar e implementar un formulario que permita ingresar la información del destinatario, validando en tiempo real el número de cuenta, el banco asociado y los datos requeridos antes de ejecutar la transferencia. |
| **Tarea 2.2** | Integrar API interbancaria (ACH/SPEI según país) | **DOSW-10** | Implementar la comunicación con la API interbancaria para permitir el envío de dinero a cuentas pertenecientes a otras entidades financieras, garantizando la integridad y seguridad de las transacciones. |
| **Tarea 2.3** | Desarrollar módulo de agenda de contactos frecuentes | **DOSW-11** | Crear una funcionalidad que permita almacenar y administrar destinatarios frecuentes, facilitando futuras transferencias y reduciendo el tiempo de ingreso de información. |
| **Tarea 3.1** | Diseñar pantalla de historial con filtros dinámicos | **DOSW-12** | Diseñar la interfaz de consulta del historial de transferencias, permitiendo al usuario filtrar los movimientos por fecha, monto y tipo de operación. |
| **Tarea 3.2** | Crear query paginado en base de datos para movimientos | **DOSW-13** | Implementar las consultas necesarias para recuperar los movimientos registrados en la base de datos utilizando paginación, optimizando el rendimiento y el tiempo de respuesta del sistema. |
| **Tarea 3.3** | Generar y exportar comprobante en formato PDF | **DOSW-14** | Desarrollar la funcionalidad que permita generar y descargar comprobantes de las transferencias realizadas en formato PDF, incluyendo la información relevante de cada operación. |
| **Tarea 4.1** | Desarrollar pantalla de configuración de límites en perfil | **DOSW-15** | Diseñar e implementar una interfaz dentro del perfil del usuario que permita establecer y modificar límites diarios para las transferencias realizadas. |
| **Tarea 4.2** | Implementar lógica de validación de límite antes de cada transacción | **DOSW-16** | Desarrollar las reglas de negocio encargadas de verificar que el monto acumulado de las transferencias no supere el límite diario configurado por el usuario. |
| **Tarea 4.3** | Crear flujo de desbloqueo temporal con autenticación de dos factores (2FA) | **DOSW-17** | Implementar un proceso de autenticación adicional mediante doble factor de verificación que permita al usuario solicitar un desbloqueo temporal en caso de exceder los límites establecidos. |

---

## Prioridades

### Prioridad alta

- **HU-1** Transferencia entre cuentas propias (**DOSW-2**).
- **HU-2** Transferencia a terceros (**DOSW-3**).
- **HU-4** Límites y seguridad (**DOSW-5**).

### Prioridad media

- **HU-3** Historial de transferencias (**DOSW-4**).

---

**Alta:** Tareas críticas para el funcionamiento principal del sistema. Deben desarrollarse con prioridad porque son indispensables para que la funcionalidad esté operativa.

**Media:** Tareas importantes que complementan la funcionalidad principal y mejoran la experiencia del usuario, pero cuya ausencia no impide el funcionamiento básico del sistema.

**Baja:** Tareas de apoyo o mejoras adicionales que pueden implementarse en etapas posteriores sin afectar significativamente la operación principal del sistema.