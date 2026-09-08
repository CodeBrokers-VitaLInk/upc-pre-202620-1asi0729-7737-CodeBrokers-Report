# 4. Capítulo IV: Product Design

## 4.1. Style Guidelines

El diseño visual de VitaLink sigue una estética entre lo clínico y lo confiable, en línea con la identidad del startup CodeBrokers y con el compromiso de ofrecer soluciones de calidad para el sector salud, enfocadas en el cuidado y acompañamiento de adultos mayores.

Esta sección define el repositorio central de decisiones visuales y de interacción que todo el equipo aplica en el Landing Page y en las Web Applications: identidad, tipografía, color, espaciado, iconografía, tono de comunicación y criterios de accesibilidad. Cada decisión se acompaña del principio de diseño que la sustenta, de modo que las propuestas de las secciones 4.3 y 4.4 puedan verificarse contra este documento.

Las decisiones se expresan como **design tokens** (nombre, valor y uso). El nombre del token es el que se utiliza en el Landing Page (variables CSS), en las Web Applications (tema de Angular Material) y en el archivo de Figma, de manera que un cambio de valor se propague a los tres sin ambigüedad.

### 4.1.1. General Style Guidelines

#### Branding

El logo principal representa a VitaLink, una plataforma orientada al monitoreo y seguimiento de la salud de los adultos mayores. El nombre surge de la combinación de "Vital", relacionado con los signos vitales, la salud y el bienestar, y "Link", que representa la conexión constante entre el adulto mayor, sus familiares y los profesionales o centros de salud.

La identidad visual incorpora un ícono minimalista que combina elementos relacionados con la salud, el monitoreo y la conexión: una figura humana protegida dentro de una forma inspirada en un corazón, integrando una línea de pulso. Este recurso comunica de forma directa el propósito del producto: cuidar, monitorear y mantener conectadas a las personas involucradas en el bienestar del adulto mayor.

Reglas de uso de la marca:

- La grafía correcta es **VitaLink**, con V y L mayúsculas. No se utilizan las variantes "Vitalink", "Vita Link" ni "VITALINK" en interfaz ni en documentación.
- El logotipo mantiene un área de resguardo equivalente a la altura de la letra "V" en los cuatro lados; ningún elemento invade ese espacio.
- Tamaño mínimo de uso: 24 px de altura en pantalla. Por debajo de ese tamaño se utiliza únicamente el isotipo.
- El logotipo se coloca sobre superficies claras (`--color-surface` o `--color-background`). Sobre fondos de color se utiliza la versión monocromática blanca.
- El logotipo es un elemento de identidad, no un elemento decorativo: aparece una sola vez por vista, en el header, y actúa como enlace al inicio.

\includegraphics[width=0.7\linewidth]{assets/logo-vitalink.png}

#### Typography

La familia tipográfica del producto es **Inter**, en los pesos Regular (400), Medium (500), SemiBold (600) y Bold (700). Se eligió por su alta legibilidad en pantalla, su amplia gama de pesos y su altura de x generosa, característica que favorece la lectura de datos clínicos y de textos cortos por parte de adultos mayores.

La pila de fuentes declarada garantiza una degradación consistente si la fuente no llega a cargar:

```css
--font-family-base: "Inter", "Segoe UI", Roboto, system-ui, sans-serif;
```

Se utiliza una única familia tipográfica en todo el producto. Mezclar varias familias oscurece la jerarquía de información y hace que la interfaz se perciba inconsistente.

**Escala tipográfica**

| Token | Uso | Tamaño | Peso | Interlineado |
|---|---|---|---|---|
| `--text-display` | Título principal del Hero (un solo `h1` por vista) | 3rem (48 px) | 700 | 1.1 |
| `--text-h2` | Títulos de sección | 2rem (32 px) | 600 | 1.2 |
| `--text-h3` | Títulos de tarjeta y subsecciones | 1.5rem (24 px) | 600 | 1.3 |
| `--text-lead` | Texto destacado bajo un título | 1.125rem (18 px) | 400 | 1.5 |
| `--text-body` | Cuerpo de texto | 1rem (16 px) | 400 | 1.6 |
| `--text-caption` | Etiquetas, fechas e información auxiliar | 0.875rem (14 px) | 500 | 1.4 |

Reglas asociadas:

- Los tamaños se declaran en `rem`, nunca en `px` fijos, para que la interfaz responda cuando la persona modifica el tamaño de letra del navegador. **Principio de accesibilidad:** la interfaz debe permitir ampliar el texto hasta 200 % sin pérdida de contenido ni de funcionalidad.
- No se utilizan pesos Light ni Thin. Los pesos delgados reducen la legibilidad, en particular en tamaños pequeños y en pantallas de bajo contraste.
- El tamaño mínimo de texto en la interfaz es 14 px. Ningún dato clínico, etiqueta de estado o mensaje de error se muestra por debajo de ese tamaño.
- La longitud de línea del cuerpo de texto se limita a un máximo de 75 caracteres mediante el ancho del contenedor, para no dificultar el retorno de línea durante la lectura.
- La jerarquía se mantiene en todos los tamaños de pantalla: si el `--text-display` se reduce en móvil, los demás niveles se reducen proporcionalmente conservando la misma relación de importancia.

#### Color

La paleta se organiza por **rol semántico**, no por apariencia. Cada token indica para qué sirve el color; esto evita que un mismo color signifique cosas distintas en pantallas distintas, que es la causa más frecuente de confusión sobre qué elemento es interactivo.

**Colores de marca y acción**

| Token | Valor | Uso | Contraste sobre blanco |
|---|---|---|---|
| `--color-primary` | `#00694C` | Color de marca y de toda acción principal (botones primarios, enlaces activos, íconos de estado positivo) | 6.72:1 |
| `--color-primary-hover` | `#008560` | Estado hover y focus del color primario | 4.64:1 |
| `--color-on-primary` | `#FFFFFF` | Texto e íconos sobre superficies primarias | 6.72:1 sobre `--color-primary` |
| `--color-accent-family` | `#145DA3` | Acento de apoyo exclusivo de la vista Familiar: etiquetas de plan, ilustraciones y elementos informativos | 6.72:1 |

**Decisión sobre el uso del azul.** El producto tiene un único color de acción — el verde `--color-primary` — en las dos vistas del Landing Page. El azul `--color-accent-family` funciona como acento de apoyo en la vista Familiar, para diferenciar visualmente al segmento sin crear un segundo color de acción. **Principio de diseño:** evitar que un mismo color signifique cosas diferentes; si el verde indica que un elemento sin borde es interactivo, usar un segundo color con el mismo rol vuelve ambigua la interfaz. En consecuencia, todo botón primario, en ambas vistas, utiliza `--color-primary`.

**Superficies y texto**

| Token | Valor | Uso | Contraste |
|---|---|---|---|
| `--color-surface` | `#FFFFFF` | Tarjetas, header y superficies de contenido | — |
| `--color-background` | `#F8FAFB` | Fondo de página y de secciones alternas | — |
| `--color-surface-alt` | `#F2F4F5` | Bloques diferenciados dentro de una sección | — |
| `--color-surface-muted` | `#ECEEEF` | Controles inactivos y superficies deshabilitadas | — |
| `--color-border` | `#E1E3E4` | Bordes decorativos de tarjetas y separadores | 1.29:1 sobre blanco |
| `--color-border-strong` | `#5C6B65` | Bordes que comunican interactividad: campos de formulario y botones secundarios | 4.82:1 sobre blanco |
| `--color-text` | `#191C1D` | Títulos y texto principal | 17.14:1 sobre blanco |
| `--color-text-secondary` | `#3D4943` | Texto secundario, descripciones y enlaces de navegación | 9.41:1 sobre blanco |

**Colores de estado**

| Token | Valor | Uso | Contraste |
|---|---|---|---|
| `--color-danger` | `#BA1A1A` | Alertas críticas y errores de validación | 6.46:1 sobre blanco |
| `--color-danger-container` | `#FFDAD6` | Fondo de mensajes de alerta crítica | 5.00:1 con `--color-danger` |
| `--color-success` | `#00694C` | Confirmaciones y estados dentro de rango | 6.72:1 |
| `--color-warning` | `#8A5000` | Estados de atención que no requieren acción inmediata | 6.13:1 |

Reglas asociadas:

- **Ningún estado se comunica solo con color.** Toda alerta, etiqueta de urgencia o estado de un paciente combina color con un ícono y con una etiqueta de texto. Esto es indispensable para personas con discapacidad visual relacionada con el color, y en un producto de salud una alerta que solo se distingue por su tono es un riesgo real.
- Los bordes que comunican interactividad usan `--color-border-strong`. `--color-border` (1.29:1) se reserva para separaciones decorativas, ya que no alcanza el contraste necesario para transmitir el límite de un control.
- Los valores se declaran una sola vez como variables CSS y se consumen desde ahí; no se escriben hexadecimales sueltos en los componentes.

\includegraphics[width=0.7\linewidth]{assets/colors.png}

#### Spacing

El sistema de espaciado usa una unidad base de 8 px, que ordena la composición y evita separaciones arbitrarias.

| Token | Valor | Uso |
|---|---|---|
| `--space-1` | 0.25rem (4 px) | Separación entre un ícono y su etiqueta |
| `--space-2` | 0.5rem (8 px) | Separación entre elementos muy relacionados |
| `--space-3` | 1rem (16 px) | Separación entre elementos de una misma tarjeta |
| `--space-4` | 1.5rem (24 px) | Padding interno de tarjetas |
| `--space-5` | 2rem (32 px) | Separación entre bloques dentro de una sección |
| `--space-6` | 3rem (48 px) | Padding vertical de secciones en móvil |
| `--space-7` | 5rem (80 px) | Separación entre secciones en escritorio |

**Principio de diseño:** agrupar los elementos relacionados y darles suficiente espacio alrededor. Cuando controles no relacionados quedan demasiado juntos, o el contenido los aprieta, resulta difícil distinguirlos y entender qué hace cada uno.

#### Bordes, radios y elevación

| Token | Valor | Uso |
|---|---|---|
| `--radius-sm` | 8 px | Etiquetas y campos de formulario |
| `--radius-md` | 12 px | Botones |
| `--radius-lg` | 16 px | Tarjetas y contenedores de imagen |
| `--radius-full` | 999 px | Selectores de segmento y píldoras |
| `--shadow-sm` | `0 1px 2px rgba(25,28,29,.06)` | Tarjetas en reposo |
| `--shadow-md` | `0 4px 12px rgba(25,28,29,.10)` | Tarjetas destacadas y estado hover |

La elevación se usa para separar el contenido de los controles, no como recurso decorativo. Una tarjeta no lleva simultáneamente sombra pronunciada y borde marcado: se elige un solo recurso para delimitarla.

#### Iconografía

- **Sistema:** Material Symbols Rounded, en formato vectorial (SVG), coherente con Angular Material como biblioteca de componentes.
- **Tamaños:** 18 px en elementos pequeños, 24 px en línea con el texto, 40 px en elementos destacados.
- **Peso:** el trazo de los íconos acompaña el peso del texto adyacente, para que ambos tengan el mismo nivel de énfasis.
- **Un concepto, un ícono.** Cada idea del producto tiene su propio símbolo y ningún ícono se repite para representar conceptos distintos. Un ícono efectivo expresa un solo concepto de forma inmediatamente reconocible; repetir el mismo glifo en tarjetas que explican pasos diferentes anula esa función y obliga a leer todo el texto para distinguirlas.
- **Los íconos no sustituyen al texto:** acompañan siempre a una etiqueta, salvo en controles universalmente reconocidos, que en ese caso llevan `aria-label`.
- Los íconos decorativos se marcan con `aria-hidden="true"` para que los lectores de pantalla no los anuncien.

#### Tono de comunicación

La voz de VitaLink es profesional, confiable y empática. El tono se ajusta según el segmento y la situación, pero se mantiene dentro de las siguientes dimensiones:

| Dimensión | Posición de VitaLink | Sustento |
|---|---|---|
| Divertido ↔ **Serio** | Serio, sin llegar a solemne | El producto comunica información de salud; el humor restaría credibilidad a una alerta |
| **Formal** ↔ Casual | Formal en la vista Profesional, moderadamente casual en la vista Familiar | El profesional espera precisión clínica; el familiar necesita cercanía y lenguaje cotidiano |
| **Respetuoso** ↔ Irreverente | Respetuoso | El usuario final es un adulto mayor y el contexto puede ser una urgencia de salud |
| Entusiasta ↔ **Sereno** | Sereno | La serenidad transmite control; el entusiasmo frente a una alerta médica resulta inadecuado |

Reglas de redacción:

- Lenguaje sencillo y sin jerga innecesaria. En la vista Familiar no se usan términos clínicos como "HR basal" o "cama"; se dice "frecuencia cardíaca" y se describe la situación en palabras de todos los días.
- Las etiquetas de acción empiezan con un verbo y describen el resultado: "Crear cuenta", "Solicitar información". Se evitan fórmulas vagas como "Clic aquí".
- Se usa sentence case en botones, etiquetas y títulos de sección. No se emplean mayúsculas sostenidas en bloques de texto, porque reducen la velocidad de lectura.
- No se usa la primera persona del plural en mensajes de error: se prefiere "No se pudo cargar la información" antes que "Tuvimos un problema".

#### Accesibilidad e inclusión

Estas reglas son obligatorias y se verifican antes de dar por terminada cualquier vista:

- **Contraste:** 4.5:1 como mínimo para texto de hasta 17 pt; 3:1 para texto de 18 pt o mayor y para texto en negrita. Todos los tokens de esta sección incluyen su ratio medido.
- **Tamaño de los controles:** área interactiva de 44 × 44 px como mínimo en experiencias táctiles y de 24 × 24 px como mínimo con puntero. Los controles pequeños son difíciles de accionar para muchas personas, y el segmento de adultos mayores es especialmente sensible a esto.
- **Foco visible:** todo elemento interactivo muestra un anillo de foco de 2 px en `--color-primary` con 2 px de separación. Nunca se elimina el indicador de foco.
- **Estructura semántica:** un solo `h1` por vista y jerarquía de encabezados sin saltos de nivel; regiones marcadas con `header`, `nav`, `main` y `footer`.
- **ARIA:** el selector de segmento usa `role="tablist"` con `aria-selected`; las alertas dinámicas usan `role="alert"`; los íconos informativos llevan `aria-label` y los decorativos `aria-hidden`.
- **Imágenes:** todas llevan atributo `alt` descriptivo; las puramente decorativas llevan `alt=""`.
- **Movimiento:** las transiciones respetan `prefers-reduced-motion`; ninguna información depende de una animación para ser percibida.
- **Internacionalización (i18n):** el producto se construye con los idiomas English (`en_US`) y Latin American Spanish (`es_419`). El idioma por defecto de la interfaz y de la documentación es inglés. Ningún texto se escribe fijo en el código: todos los mensajes provienen de archivos de traducción, y los diseños contemplan un crecimiento de hasta 30 % en la longitud de las cadenas al traducirse. El atributo `lang` del documento cambia junto con el idioma seleccionado.

### 4.1.2. Web Style Guidelines

Esta sección define los estándares visuales y de interacción para las interfaces web responsive: el Landing Page y las Web Applications. Ambas vistas del Landing Page —Profesional de salud y Familiar— comparten estos lineamientos; lo que cambia entre ellas es el contenido y el acento de apoyo, nunca la estructura ni el sistema de componentes. Esa consistencia es la que permite que ambas se reconozcan como el mismo producto.

#### Grid y breakpoints

| Breakpoint | Ancho | Columnas | Margen lateral | Ancho del contenedor |
|---|---|---|---|---|
| Móvil | 360–767 px | 4 | 20 px | fluido |
| Tableta | 768–1023 px | 8 | 32 px | fluido |
| Escritorio | 1024 px en adelante | 12 | 40 px | 1200 px como máximo |

El contenido se ancla a un contenedor de 1200 px como máximo y se centra en pantallas mayores, para conservar una longitud de línea legible. El diseño se verifica en los dos extremos —360 px y 1440 px— antes de darse por terminado.

#### Botones

| Variante | Fondo | Texto | Borde | Uso |
|---|---|---|---|---|
| Primario | `--color-primary` | `--color-on-primary` | ninguno | Acción principal de la vista; una sola por sección |
| Secundario | `--color-surface` | `--color-text` | 1 px `--color-border-strong` | Acción alternativa |
| Terciario | transparente | `--color-primary` | ninguno | Acciones de baja jerarquía |

- Altura mínima de 44 px, padding horizontal de `--space-4`, radio `--radius-md`, tipografía `--text-body` en peso 600.
- Estados obligatorios: reposo, hover, focus-visible, activo y deshabilitado. El estado deshabilitado usa `--color-surface-muted` y se acompaña de una explicación de por qué la acción no está disponible.
- La etiqueta de un botón nunca ocupa más de una línea. Si no entra, se acorta el texto; no se reduce la fuente ni se permite el salto de línea dentro del botón.
- El borde del botón secundario usa `--color-border-strong` y no `--color-border`: un borde de 1.29:1 de contraste no comunica que el elemento es accionable.

#### Enlaces de navegación

- Color `--color-text-secondary`; pasan a `--color-primary` en hover y focus.
- Tipografía `--text-body`, peso 600, sin subrayado en el header y con subrayado dentro de bloques de texto.
- Todos los elementos del menú se mantienen en una sola línea. Etiquetas de una y de dos líneas conviviendo en la misma barra rompen la alineación de las líneas base y ensucian la lectura horizontal.
- Área accionable de 44 px de alto como mínimo, incluso cuando el texto es más bajo.

#### Header

- Altura de 80 px en escritorio y 64 px en móvil; fondo `--color-surface`; separado del contenido por un borde inferior de 1 px en `--color-border`.
- Contiene, de izquierda a derecha: logotipo, navegación por anclas, selector de segmento y acción principal.
- El logotipo es parte del header, no un elemento suelto sobre la página, y enlaza al inicio.
- En móvil la navegación colapsa en un menú desplegable con `aria-expanded`, mientras el logotipo y la acción principal permanecen visibles.
- El selector de segmento indica la opción activa con color de fondo **y** con `aria-selected`; la opción inactiva usa `--color-text-secondary` sobre `--color-surface-muted`, combinación que alcanza 8.08:1. No se utilizan grises de bajo contraste para la opción inactiva, ya que sigue siendo texto legible y accionable.

#### Tarjetas y contenedores

- Fondo `--color-surface`, borde 1 px `--color-border`, radio `--radius-lg`, padding `--space-4`, sombra `--shadow-sm`.
- **Las tarjetas de una misma fila tienen la misma altura**, con los botones alineados al pie mediante un contenedor flexible. Alinear los componentes entre sí facilita el escaneo y comunica que pertenecen al mismo nivel de información; bordes inferiores desparejos se leen como desorden.
- La separación entre el último elemento de contenido y el botón de la tarjeta es de `--space-4` como mínimo.
- Una tarjeta destacada se diferencia por borde en `--color-primary` y sombra `--shadow-md`, sin cambiar su ancho respecto de las demás.
- Las etiquetas que sobresalen del borde superior de una tarjeta se mantienen en una sola línea y en sentence case.

#### Secciones

- Padding vertical de `--space-7` en escritorio y `--space-6` en móvil.
- Se alternan fondos `--color-surface` y `--color-background` para separar bloques consecutivos, sin recurrir a líneas divisorias adicionales.
- Cada sección abre con un título `--text-h2` y, opcionalmente, un texto de apoyo `--text-lead` de dos líneas como máximo.
- Los elementos más importantes se ubican arriba y hacia el inicio de la línea de lectura, que es el orden en que se recorre la página.

#### Formularios

- Etiqueta siempre visible sobre el campo; el texto de ejemplo dentro del campo no reemplaza a la etiqueta.
- Altura de 44 px, borde 1 px `--color-border-strong`, radio `--radius-sm`.
- Los errores se muestran junto al campo, con ícono y texto que explique cómo corregir, y se anuncian mediante `aria-live`.
- Los campos obligatorios se marcan con texto, no solo con un asterisco de color.

#### Alertas y estados

- Alerta crítica: fondo `--color-danger-container`, texto e ícono `--color-danger`, borde izquierdo de 4 px.
- Cada alerta presenta ícono, etiqueta de nivel y descripción. El nivel de urgencia nunca se comunica únicamente por color.
- En la vista Familiar, la alerta se redacta sin jerga clínica y explica qué ocurrió, qué tan grave es y si alguien ya está atendiendo.

#### Imágenes y contenido visual

- Se integran en contenedores con radio `--radius-lg`; relación de aspecto fija para evitar saltos de composición durante la carga.
- Las fotografías representan al segmento al que se dirige la vista: la vista Familiar no utiliza imágenes de contexto hospitalario, porque contradice el mensaje de acompañamiento en el hogar.
- Todas llevan `alt` descriptivo y se entregan en formatos de peso reducido.

#### Movimiento

- Transiciones de 150 ms para estados de hover y foco, y de 250 ms para la aparición de bloques, con curva `ease-out`.
- El movimiento aporta continuidad, nunca información: si una animación no se ejecuta, la interfaz sigue siendo comprensible.

#### Correspondencia con Angular Material

Las Web Applications utilizan Angular Material como biblioteca de componentes. Los tokens de esta sección se aplican mediante un tema personalizado, de modo que los componentes del sistema hereden la identidad de VitaLink:

| Elemento de esta guía | Componente de Angular Material |
|---|---|
| Botón primario / secundario / terciario | `mat-flat-button` / `mat-stroked-button` / `mat-button` |
| Tarjeta | `mat-card` |
| Campo de formulario | `mat-form-field` con `appearance="outline"` |
| Selector de segmento | `mat-button-toggle-group` |
| Alerta y notificación | `mat-snack-bar` y contenedor propio para alertas persistentes |
| Navegación de la aplicación | `mat-sidenav` con `mat-nav-list` |
| Tabla de pacientes y alertas | `mat-table` con `matSort` y `mat-paginator` |

El Landing Page se construye con HTML5, CSS3 y JavaScript sin biblioteca de componentes, aplicando los mismos tokens mediante variables CSS. Esto mantiene la experiencia consistente entre el sitio estático y la aplicación, tal como exige la relación entre ambos productos.
