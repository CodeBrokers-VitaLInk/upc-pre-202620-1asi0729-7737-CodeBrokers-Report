## 4.2. Information Architecture

Esta sección define cómo se organiza, se nombra, se busca y se recorre el contenido en los dos productos digitales de VitaLink: el Landing Page (sitio web estático) y las Web Applications. Las decisiones buscan que visitantes y usuarios se adapten con facilidad a cada producto y encuentren lo que necesitan sin esfuerzo, y son coherentes con los tokens y componentes definidos en 4.1.

### 4.2.1. Organization Systems

VitaLink combina sistemas de organización visual y esquemas de categorización seleccionados según el tipo de contenido de cada bloque.

#### Organización jerárquica (visual hierarchy)

Se aplica en toda la estructura del Landing Page para establecer niveles de importancia y guiar la atención:

- **Nivel 1:** header y navegación principal, con el logotipo, las secciones y la acción principal.
- **Nivel 2:** títulos y mensajes principales de cada sección, como "Flujo clínico integrado", "Protocolo de alerta inteligente" y "Seguridad de grado médico".
- **Nivel 3:** descripciones, características, beneficios y elementos secundarios que complementan la información principal.

La jerarquía se refuerza con tamaño tipográfico, peso, color, contraste, espaciado y posición, según la escala definida en 4.1.1. Los elementos de mayor importancia se ubican arriba y hacia el inicio de la línea de lectura, que es el orden en que se recorre la página.

#### Organización secuencial (step-by-step)

Se utiliza en la sección "Flujo clínico integrado", donde el funcionamiento se presenta como una progresión de tres etapas:

- **Captura continua:** recopilación de información desde el sensor o la aplicación del adulto mayor.
- **Análisis algorítmico:** procesamiento de los datos y detección de valores fuera de rango.
- **Alertas integradas:** comunicación priorizada de la situación al familiar y al profesional de salud.

Las tres etapas se presentan consecutivas y conectadas visualmente. Cada etapa tiene su propio ícono, distinto de los demás, y su propio título: el orden y la diferenciación son justamente lo que comunica que se trata de un proceso y no de tres características sueltas.

#### Organización por secciones

El Landing Page divide la información en bloques diferenciados, presentados en este orden:

| Orden | Sección | Propósito |
|---|---|---|
| 1 | Hero | Propuesta de valor principal y acciones principales |
| 2 | Flujo clínico integrado | Explicar cómo funciona el sistema |
| 3 | Protocolo de alerta inteligente | Comunicar el comportamiento de las alertas |
| 4 | Planes | Presentar los niveles de servicio y su precio |
| 5 | Seguridad de grado médico | Cumplimiento normativo y protección de datos |
| 6 | Llamada a la acción final | Conversión hacia registro o solicitud de información |
| 7 | Footer | Información institucional, legal, contacto y enlaces |

#### Categorización por tópicos

La información se agrupa según temas: beneficios y propuesta de valor, funcionamiento, seguridad, servicios para profesionales e información complementaria. Esta categorización permite identificar rápidamente el tema de cada sección.

#### Categorización por audiencia

El Landing Page atiende a dos segmentos mediante un selector de perfil en el header, que conmuta entre la vista **Profesional de salud** y la vista **Familiar**. Ambas vistas conservan el mismo orden de secciones y el mismo sistema de componentes; cambian el contenido, las imágenes y las llamadas a la acción. Mantener la estructura estable entre vistas evita que la persona tenga que reorientarse al cambiar de perfil.

### 4.2.2. Labeling Systems

El sistema de etiquetado comunica la propuesta de valor de forma clara y directa, con un número reducido de palabras y términos reconocibles del ámbito de la salud, para facilitar el escaneo visual y reducir la carga cognitiva.

#### Principios de etiquetado

- **Concisión:** etiquetas de una a tres palabras.
- **Consistencia:** un concepto se nombra siempre igual, en las dos vistas y en los dos productos. Una etiqueta que cambia de nombre entre pantallas obliga a reaprender la interfaz.
- **Familiaridad:** términos reconocibles para cada segmento; el vocabulario clínico se reserva para la vista Profesional.
- **Claridad:** la etiqueta describe el contenido o la acción, sin recurrir a nombres creativos que no se entiendan fuera del equipo.
- **Sentence case:** todas las etiquetas de interfaz se escriben en sentence case, sin mayúsculas sostenidas.

#### Etiquetas de navegación

El menú principal utiliza cuatro etiquetas por vista, tres de ellas compartidas, con anclas estables:

| Vista Profesional | Vista Familiar | Ancla |
|---|---|---|
| Cómo funciona | Cómo funciona | `#como-funciona` |
| Alertas | Alertas | `#alertas` |
| Planes | Planes | `#planes` |
| Seguridad | Familias | `#seguridad` / `#familias` |

Estas etiquetas son las que se implementan en el header, en las anclas internas y en los diseños de la sección 4.3, de modo que la documentación, el prototipo y la implementación nombren las mismas cosas del mismo modo.

#### Etiquetas de identificación de audiencia

El selector de perfil utiliza "Profesionales de salud" y "Familias". Ambas opciones se anuncian con `aria-selected` además de diferenciarse por color, para que el estado activo no dependa únicamente de la apariencia.

#### Etiquetas de secciones informativas

"Flujo clínico integrado", "Protocolo de alerta inteligente", "Seguridad de grado médico" y "Cumplimiento normativo". Funcionan como encabezados de bloque y permiten identificar el propósito de cada sección.

#### Etiquetas de características y beneficios

"Captura continua", "Análisis algorítmico", "Alertas integradas", "Priorización por gravedad", "Escalamiento multicanal", "Contexto histórico", "Cifrado de extremo a extremo", "HIPAA y GDPR" y "Control de acceso por roles".

Las etiquetas no prometen resultados que el producto no puede garantizar. En particular, no se utilizan formulaciones como "cero falsos positivos": en un producto de salud, una promesa absoluta sobre la detección compromete la credibilidad de toda la propuesta y no puede sustentarse ante una audiencia clínica.

#### Etiquetas de acción

"Unirme como proveedor", "Solicitar información", "Crear cuenta" y "Conocer cómo funciona". Cada una empieza con un verbo y describe el resultado de la acción.

#### Etiquetas institucionales

En el footer: "Legal", "Contacto", "Privacidad" y "Términos del servicio". El enlace a términos y condiciones y a la política de privacidad está presente en el footer del Landing Page y en el de las aplicaciones.

#### Asociaciones entre etiquetas

Las etiquetas se relacionan mediante jerarquía tipográfica, agrupación visual dentro de una misma tarjeta o sección, iconografía complementaria, color de acento y espaciado consistente. El color acompaña la asociación, pero nunca es el único recurso que la comunica.

### 4.2.3. SEO Tags and Meta Tags

Los valores se definen según el propósito de cada experiencia: el Landing Page busca posicionamiento y captación; la Web Application, identificación de vistas para usuarios autenticados.

#### Landing Page

```html
<title>VitaLink | Preventive Monitoring for Health Professionals and Families</title>

<meta name="description" content="VitaLink connects older adults, their families and health professionals through continuous vital-sign monitoring and prioritized alerts.">

<meta name="keywords" content="VitaLink, preventive monitoring, patient monitoring, health alerts, older adult care, health professionals">

<meta name="author" content="CodeBrokers">

<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

El idioma por defecto de los metadatos es inglés, en coherencia con la decisión de i18n de la sección 4.1. La versión en español se sirve mediante `hreflang`:

```html
<link rel="alternate" hreflang="en-US" href="https://vitalink.app/">
<link rel="alternate" hreflang="es-419" href="https://vitalink.app/es/">
```

#### Open Graph y redes sociales

```html
<meta property="og:title" content="VitaLink | Preventive Monitoring for Health Professionals and Families">
<meta property="og:description" content="Continuous monitoring and prioritized alerts that keep families and clinicians informed.">
<meta property="og:image" content="[URL de la imagen oficial de VitaLink]">
<meta property="og:url" content="[URL oficial de VitaLink]">
<meta property="og:type" content="website">
<meta name="twitter:card" content="summary_large_image">
```

#### Estructura semántica del Landing Page

- **Jerarquía de encabezados:** un único `h1` para la propuesta de valor y encabezados `h2` y `h3` para secciones y tarjetas, sin saltos de nivel.
- **Identificadores de sección:** `#como-funciona`, `#alertas`, `#planes`, `#seguridad` y `#familias`, coincidentes con las etiquetas de navegación de 4.2.2.
- **Atributos `alt` descriptivos:** por ejemplo, `<img alt="Panel clínico de VitaLink con alertas priorizadas por gravedad">`.
- **Regiones semánticas:** `header`, `nav`, `main`, `section` y `footer`, que además permiten la navegación por lectores de pantalla.
- **Datos estructurados:** se podrá incorporar Schema.org para representar la organización y el producto cuando la información publicada sea definitiva.

#### Web Application

```html
<title>VitaLink | Health Monitoring Platform</title>

<meta name="description" content="VitaLink platform for preventive patient follow-up, health data visualization and alert management.">

<meta name="author" content="CodeBrokers">

<meta name="robots" content="noindex, nofollow">
```

Las vistas autenticadas se excluyen de la indexación, ya que su contenido no es público y no aporta valor de posicionamiento. Cada vista define su propio título manteniendo la identidad del producto: `Dashboard | VitaLink`, `Patients | VitaLink`, `Alerts | VitaLink`, `Profile | VitaLink`.

### 4.2.4. Searching Systems

#### Landing Page

El Landing Page no incorpora un buscador. Su contenido cabe en una sola página, está dividido en seis secciones y la navegación por anclas del header permite alcanzar cualquiera de ellas en un clic. Introducir un buscador en un volumen de contenido tan reducido agrega un control que compite con las llamadas a la acción sin resolver ninguna necesidad real.

#### Web Application — vista Profesional

Es la experiencia donde el volumen de información sí justifica un sistema de búsqueda, ya que un profesional puede tener decenas de pacientes bajo seguimiento.

- **Búsqueda global** en la barra superior, disponible desde cualquier vista, que consulta pacientes por nombre y por documento de identidad. Devuelve resultados mientras se escribe, a partir del tercer carácter, agrupados por tipo (pacientes y alertas).
- **Búsqueda dentro de la lista de pacientes**, combinada con filtros:

| Filtro | Valores | Comportamiento por defecto |
|---|---|---|
| Estado de la alerta | Pendiente, en revisión, atendida, cerrada | Pendiente y en revisión |
| Nivel de gravedad | Alta, media, baja | Todos |
| Rango de fechas | Hoy, últimos 7 días, últimos 30 días, personalizado | Últimos 7 días |
| Proveedor asignado | Lista de profesionales del centro | Todos |

- **Presentación de los resultados:** tabla con paginación, ordenable por gravedad y por fecha del último registro. Cada fila muestra el nombre del paciente, el nivel de gravedad como etiqueta con ícono y texto, la fecha del último registro y el estado de la alerta. Los filtros activos se muestran como etiquetas removibles sobre la tabla, de modo que siempre sea evidente por qué el listado está recortado.
- **Estado vacío:** cuando una búsqueda no arroja resultados se explica el motivo y se ofrece una salida —quitar filtros o ampliar el rango de fechas—, en lugar de mostrar una tabla en blanco.

#### Web Application — vista Familiar

El volumen de información es mucho menor, ya que una familia sigue a uno o pocos adultos mayores. En lugar de un buscador se ofrece un filtro por tipo de evento y por rango de fechas dentro del historial, con las mismas etiquetas de estado que la vista Profesional. Esta decisión responde al perfil del segmento: agregar controles de búsqueda a una experiencia que se usa en momentos de preocupación añade carga cognitiva sin beneficio.

### 4.2.5. Navigation Systems

#### Landing Page

Navegación lineal con un header fijo que contiene anclas a las secciones principales. El selector de perfil conmuta entre las vistas Profesional y Familiar conservando la posición de lectura, y las llamadas a la acción de cada vista dirigen a la Web Application correspondiente: la del segmento Profesional inicia el proceso para unirse como proveedor y la del segmento Familiar inicia la creación de cuenta. En móvil, la navegación colapsa en un menú desplegable, mientras el logotipo y la acción principal permanecen visibles.

Un selector de idioma en el footer permite alternar entre English y Español, según la decisión de i18n de 4.1.

#### Web Applications

| Recurso | Vista Profesional | Vista Familiar |
|---|---|---|
| Navegación principal | Barra lateral persistente con Panel, Pacientes, Alertas y Reportes | Barra inferior con Inicio, Alertas, Historial y Perfil |
| Navegación contextual | Ruta de navegación (breadcrumb) al entrar al detalle de un paciente | Botón de retorno explícito en cada vista de detalle |
| Navegación de emergencia | Acceso directo a alertas de gravedad alta desde cualquier vista | Botón de aviso rápido presente en la vista de inicio |

Decisiones asociadas:

- La barra lateral se eligió para la vista Profesional porque la persona alterna entre varias áreas durante una misma sesión de trabajo en pantalla amplia; la barra inferior se eligió para la vista Familiar porque concentra cuatro destinos y se usa mayoritariamente en móvil, con el pulgar.
- La sección activa se indica con color **y** con ícono relleno, además de `aria-current="page"`.
- Todos los destinos de navegación se alcanzan con teclado, en un orden de tabulación que sigue el orden visual, y con un enlace inicial para saltar directamente al contenido principal.
- Ninguna acción destructiva —cancelar un seguimiento, eliminar un contacto autorizado— se ejecuta directamente desde la navegación: siempre media una confirmación.
