## 3.2. Impact Mapping

El Impact Mapping de VitaLink parte de los Business Goals del piloto (**WHY**), identifica a los User Personas que pueden ayudar a alcanzarlos (**WHO / Actors**), define el cambio de comportamiento esperado de cada uno (**Impact**), y lo conecta con los Deliverables del negocio digital y las User Stories que los producen. Los actores se construyen a partir del análisis de las 6 entrevistas ya registradas ([2.2.3. Análisis de entrevistas](../20-chapter-two/22-entrevistas.md)).

**Herramienta:** UXPressia
**URL pública del Impact Map:** `[completar]`

> **Nota de consistencia:** las tres fichas de User Persona descritas a continuación deben elaborarse primero en UXPressia (ver [2.3.1. User Personas](../20-chapter-two/23-needfinding.md)), antes de construir el Impact Map en la misma herramienta, según lo exige el statement.

### User Personas (Actors)

**Persona 1 — Dra. Jimena, Profesional de Salud**
* **Rol:** Médica tratante en centro de salud, con alta carga de pacientes.
* **Contexto actual:** Usa el sistema institucional y papeles dispersos; solo conoce el estado de un paciente en la consulta presencial.
* **Frustración clave:** *"No cuento con seguimiento remoto ni información en tiempo real; me entero de las complicaciones recién en la siguiente cita o ante una emergencia grave."*
* **Objetivo:** Visualizar de un vistazo qué casos son urgentes, sin que eso le tome tiempo adicional a su jornada.

**Persona 2 — Samir, Familiar Cuidador**
* **Rol:** Hijo y soporte principal del cuidado de su madre adulta mayor, coordina con hermanos.
* **Contexto actual:** Llama 2-3 veces al día para verificar que todo esté bien; se entera de los problemas por terceros o por su propia madre, cuando el problema ya ocurrió.
* **Frustración clave:** *"Priorizo que la plataforma garantice la privacidad y protección de los datos de mi madre"* — junto con la culpa y fatiga de coordinar todo manualmente con sus hermanos.
* **Objetivo:** Saber de inmediato si todo está en orden y registrar que ya atendió una situación con un solo botón.

**Persona 3 — Doña Rosa, Adulta Mayor**
* **Rol:** Adulta mayor monitoreada, con baja familiaridad tecnológica.
* **Contexto actual:** Su bienestar hoy se verifica solo mediante llamadas telefónicas esporádicas de su familia.
* **Frustración clave:** Necesita poder pedir ayuda en una urgencia sin depender de que alguien la llame primero, y le preocupa quién puede ver sus datos de salud.
* **Objetivo:** Mantener su independencia el mayor tiempo posible, con una forma simple de avisar cuando algo no está bien.

---

### Business Goal 1 (WHY): Validar la reducción del tiempo de respuesta familiar

> **SMART:** Lograr que el **70%** de los familiares que completen el registro en el piloto confirmen al menos una alerta dentro de las **2 semanas** posteriores a su registro, para validar que VitaLink reduce el tiempo de respuesta ante una situación de riesgo del adulto mayor frente al método actual (llamadas esporádicas).

| Actor/Persona | Impact (¿Cómo debe cambiar?) | Deliverables (¿Qué construimos?) | User Stories |
|---|---|---|---|
| Samir (Familiar Cuidador) | Deja de depender de llamadas esporádicas y entiende el beneficio de VitaLink desde la landing | Sección Hero de la landing orientada al monitoreo remoto | Como visitante del segmento familiares, quiero entender en segundos cómo la plataforma me informa del estado de mi padre/madre sin llamarlo constantemente, para decidir si me interesa registrarme. |
| Samir (Familiar Cuidador) | Revisa la app al recibir una notificación y confirma la atención en un solo paso | Estado general simple + notificación de alerta comprensible + confirmación de un solo botón | Como familiar y adulto mayor, quiero ver un estado general simple al abrir la aplicación, para saber de inmediato si debo actuar.<br>Como familiar y adulto mayor, quiero recibir una alerta que indique qué ocurrió, su gravedad y si ya está siendo atendida, para decidir si debo intervenir.<br>Como familiar y adulto mayor, quiero confirmar que ya atendí una situación, para que el resto de la familia sepa que el caso está cubierto. |
| Samir (Familiar Cuidador) | No duplica esfuerzos con sus hermanos al coordinar el cuidado | Indicador de quién atendió una alerta y cuándo | Como familiar y adulto mayor, quiero saber si otro familiar ya revisó o atendió una alerta, para no duplicar esfuerzos ni generar confusión. |
| Doña Rosa (Adulta Mayor) | Registra (o permite que su cuidador registre) sus datos de forma consistente | Modo de uso extremadamente simple + botón de ayuda rápida + registro en modo asistido | Como familiar y adulto mayor, quiero un modo de uso extremadamente simple (botones grandes, pocos pasos), para poder usarlo sin depender siempre de ayuda.<br>Como familiar y adulto mayor, quiero solicitar ayuda de forma inmediata sin explicaciones extensas, para pedir asistencia en momentos de urgencia.<br>Como Developer, quiero que el endpoint de eventos acepte un origen de captura distinto al del propio adulto mayor, para cubrir los casos donde un cuidador ingresa los datos en su nombre. |
| Sistema VitaLink | Detecta anomalías y notifica sin intervención manual | Endpoint de ingesta de telemetría con generación automática de alertas + listado de alertas priorizado + notificaciones diferenciadas por rol | Como Developer, quiero un endpoint que reciba Telemetría Biométrica y genere una alerta automáticamente cuando el valor se desvíe de su Línea Base de Signos Vitales, para iniciar el flujo de atención sin revisión manual.<br>Como Developer, quiero un endpoint que liste alertas filtrables por estado y prioridad, para alimentar el panel médico y familiar.<br>Como Developer, quiero un servicio que envíe notificaciones distintas según el rol del destinatario, para que cada uno reciba solo la información relevante. |

---

### Business Goal 2 (WHY): Validar el canal de afiliación de proveedores de salud

> **SMART:** Afiliar a **5 proveedores de salud** (clínicas o médicos independientes) a la red de VitaLink dentro de los primeros **3 meses** del piloto, para validar la viabilidad del canal de adquisición B2B (ver [2.1.2. Estrategia 3](../20-chapter-two/21-competidores.md)).

| Actor/Persona | Impact (¿Cómo debe cambiar?) | Deliverables (¿Qué construimos?) | User Stories |
|---|---|---|---|
| Dra. Jimena (Profesional de Salud) | Se registra como proveedor a través de la landing page | Botón y flujo de registro como proveedor de salud | Como visitante del segmento profesionales de salud, quiero iniciar mi registro como proveedor, para afiliarme a la red de VitaLink. |
| Dra. Jimena (Profesional de Salud) | Queda vinculada a los pacientes que la seleccionan como proveedor | Endpoint de asociación paciente-proveedor | Como Developer, quiero un endpoint que asocie un paciente a un proveedor de salud, para vincular la información clínica correspondiente. |

---

### Business Goal 3 (WHY): Validar la confianza en el manejo de datos de salud

> **SMART:** Lograr que el **90%** de los familiares encuestados califiquen con **4 o 5 (sobre 5)** su confianza en el manejo de los datos de salud de su adulto mayor durante el **primer mes** de uso del piloto, respondiendo directamente al hallazgo de entrevistas donde el 100% de los profesionales y el 66% de los familiares exigió transparencia sobre quién accede a la información (ver [2.2.3. Análisis de entrevistas](../20-chapter-two/22-entrevistas.md)).

| Actor/Persona | Impact (¿Cómo debe cambiar?) | Deliverables (¿Qué construimos?) | User Stories |
|---|---|---|---|
| Samir (Familiar Cuidador) | Revisa la sección de privacidad antes de registrar a su madre y entiende quién ve cada dato | Sección de privacidad/seguridad de datos en la landing | Como visitante del segmento familiares, quiero conocer quién puede ver los datos de salud de mi familiar, para confiar en registrar su información. |
| Dra. Jimena (Profesional de Salud) | Confía en registrar información de pacientes porque el acceso queda auditado por rol | Sección de privacidad/seguridad de datos en la landing (versión profesional de salud) | Como visitante del segmento profesionales de salud, quiero conocer las medidas de privacidad y seguridad de datos, para confiar en registrar información de mis pacientes. |
| Sistema VitaLink | Registra y expone el nivel de acceso (RBAC) de cada usuario a los datos de salud | Endpoint de control de acceso (RBAC) / access-log por paciente | Como Developer, quiero un endpoint que registre el nivel de acceso de cada usuario a los datos de salud de un paciente, para cumplir con las expectativas de privacidad expresadas por los entrevistados. |

---

### Trazabilidad Goals → Epics

| Business Goal | Epics relacionados (3.1) |
|---|---|
| G1. Reducción del tiempo de respuesta familiar | EP-01, EP-03, EP-04 |
| G2. Afiliación de proveedores de salud | EP-01, EP-02, EP-04 |
| G3. Confianza en el manejo de datos | EP-01, EP-02, EP-03, EP-04 |
