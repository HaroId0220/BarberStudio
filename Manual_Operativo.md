# Manual Operativo de Procesos del Proyecto
 
## BarberStudio

Este manual consolida los requerimientos y acuerdos de diseño establecidos por el equipo de **BarberStudio** para la construcción técnica y validación del sistema de gestión.

---

# 1. Flujo del Proceso Base: Gestión de Citas y Anticipos

```text
[ Cliente solicita cita ]
            │
            ▼
[ Verificar historial del cliente ]
            │
            ▼
[ Registrar cita (Pendiente) ]
            │
            ▼
[ Registrar anticipo ]
            │
            ▼
[ Marcar cita confirmada ]
            │
            ▼
[ Enviar recordatorio ]
```

### Paso 1: Consulta de Historial

Antes de registrar una cita, el sistema deberá permitir la búsqueda de clientes para consultar historial de servicios, citas previas y cancelaciones.

### Paso 2: Registro de Cita

Se registra la cita asociando:

* Cliente.
* Fecha.
* Hora.
* Servicio solicitado.
* Barbero asignado.

### Paso 3: Registro de Anticipo

El sistema deberá registrar:

* Monto recibido.
* Método de pago.
* Usuario que recibió el pago.
* Fecha de registro.

### Paso 4: Confirmación Visual

Las citas con anticipo registrado deberán mostrarse con una identificación visual diferente dentro de la agenda.

### Paso 5: Recordatorio

El sistema deberá generar recordatorios para las citas próximas.

---

# 2. Estructura de Módulos y Requerimientos

| Módulo              | Función                         | Estatus   |
| ------------------- | ------------------------------- | --------- |
| Gestión de Citas    | Registrar citas                 | Propuesto |
| Gestión de Citas    | Registrar anticipos             | Propuesto |
| Gestión de Citas    | Modificar y cancelar citas      | Propuesto |
| Gestión de Clientes | Consultar historial de clientes | Propuesto |
| Gestión de Barberos | Catálogo y disponibilidad       | Propuesto |
| Reportes            | Reportes de citas e ingresos    | Propuesto |

---

# 3. Matriz de Roles y Responsabilidades

### Scrum Master

**Harold Alonso Herrera Beltrán**

Responsable de:

* Seguimiento del proyecto.
* Comunicación con el cliente.
* Gestión documental.
* Administración del repositorio GitHub.

### Frontend / Backend

**Erika Daniela Verdugo Rodríguez**

Responsable de:

* Diseño de interfaces.
* Desarrollo frontend.
* Desarrollo backend.
* Integración de funcionalidades.

### Dueño del Producto

**Arturo Beltrán**

Responsable de:

* Validación de requerimientos.
* Aprobación de entregables.
* Retroalimentación del sistema.

---

# 4. Directrices Técnicas

## Arquitectura

El sistema será desarrollado como una aplicación web responsive orientada principalmente a dispositivos móviles.

Tecnologías:

* Angular
* Node.js
* PostgreSQL
* GitHub

---

## Diseño Mobile First

Todas las pantallas deberán diseñarse priorizando teléfonos móviles, ya que constituyen el principal medio de acceso al sistema.

---

## Seguridad

El sistema deberá implementar:

* Inicio de sesión.
* Control de acceso por roles.
* Protección de información de clientes.

---

## Respaldo de Información

La información deberá almacenarse en la base de datos y mantenerse respaldada mediante mecanismos de control de versiones y copias de seguridad periódicas.

---

# 5. Riesgos Identificados

* Cambios de requerimientos durante el desarrollo.
* Dependencia de internet.
* Retrasos en validaciones por parte del cliente.
* Errores detectados durante pruebas.

---

# 6. Criterios de Aceptación

El sistema será aceptado cuando:

* Las funcionalidades acordadas estén implementadas.
* Las pruebas funcionales sean aprobadas.
* El cliente valide los resultados.

