Actúa como un Desarrollador Frontend Senior experto en Tailwind CSS v4, Accesibilidad Web (A11y) y Sistemas de Diseño de Interfaces Analíticas. Tu objetivo es construir un Dashboard de analítica publicitaria completo, altamente estructurado y con datos de prueba realistas mediante un enfoque Mobile-First.

Aplica estrictamente las siguientes especificaciones técnicas, de diseño, de negocio y operacionales:

### 1. Sistema de Colores e Identidad de Marca (Tailwind v4 @theme)
Configura en tu bloque de estilos base las variables de color personalizadas para reflejar el ecosistema de redes sociales del cliente de forma limpia y sin saturación:
- **Instagram (Acento fucsia/púrpura):** `--color-brand-ig: #E1306C;`
- **TikTok (Acento cian/oscuro):** `--color-brand-tk: #00F2FE;`
- **YouTube (Acento rojo vivo):** `--color-brand-yt: #FF0000;`
- **Sistema de Apoyo WCAG AA:** Verde éxito (`#10B981`) para ROI positivo, Naranja alerta (`#F59E0B`), Rojo crítico (`#EF4444`) para caídas de conversión, y escala neutral de grises para fondos y tarjetas.

### 2. Estructura y Accesibilidad (A11y)
- **HTML Semántico:** Utiliza etiquetas precisas (`<header>`, `<nav>`, `<aside>`, `<main>`, `<section>`, `<footer>`, `<article>`, `<button>`, `<table>`).
- **Maquetación:** Distribución general en CSS Grid y componentes internos con Flexbox. Incluye cabecera, navbar, sidebar, footer y un `<main>` con los 3 bloques analíticos.
- **Mobile-First & Breakpoints:** Maquetación fluida utilizando exactamente tres breakpoints de Tailwind (`sm:`, `md:`, `lg:`).
- **Unidades Relativas:** Prohibido el uso de píxeles (`px`). Utiliza unidades relativas (`rem`, `em`, `%`, `vh`, `vw`) o escalas de Tailwind.
- **Accesibilidad:** Contraste WCAG AA, atributos `aria-*`, estados `:focus-visible` y textos alternativos.

### 3. Diseño Visual y Gráficos (Charts.css)
- **Framework:** Exclusivamente Tailwind CSS v4 mediante directivas o clases nativas. Sin CDN externos ni estilos en línea.
- **Consistencia:** Todas las tarjetas de KPI comparten idénticos patrones de padding, bordes sutiles y tipografía tabular para alinear cifras decimales.
- **Gráficos:** Utiliza únicamente Charts.css para renderizar visualmente el embudo de conversión y las barras de rendimiento por plataforma/producto.

### 4. Contexto de Negocio y Datos
- **Portafolio y Modelo:** Producto A (50 €), Producto B (120 €) y Producto C (80 €) con 15% de comisión por venta.
- **Datos Inyectados:** Simula métricas reales de ingresos, comisiones, alcance y conversiones para Instagram, TikTok y YouTube.

### 5. Organización del Dashboard y Filtrado Avanzado
El bloque inferior operacional debe incluir un **mecanismo de filtrado multicriterio interactivo** (simulado con estructura HTML/Tailwind clara para lógica de estado):
- **Controles de Filtrado Global y por Tabla:** Selectores desplegables o pestañas para filtrar por *Plataforma* (Todas, IG, TikTok, YouTube), por *Rango de Rango de Rendimiento* (Top / Bajo desempeño) y ordenamiento de columnas numéricas (Ascendente/Descendente) en las tablas.
- **Bloque Superior (KPI Cards):** Tarjetas con volumen, ingresos por comisiones, precio medio (AOV), CTR y Engagement.
- **Bloque Intermedio (Drivers):** Gráficos con Charts.css del embudo de ventas y comparativas de canales usando los colores oficiales de las marcas (`brand-ig`, `brand-tk`, `brand-yt`).
- **Bloque Inferior (Detalles y Alertas):**
  - **Tabla de Productos:** Columnas interactivas con números tabulares alineados para Precio, Conversiones, Comisiones y ROI.
  - **Tabla de Plataformas y Campañas:** Desglose con métricas de alcance, interacciones y plataforma líder.
  - **Panel de Alertas:** Notificaciones visuales de anomalías de conversión basadas en los colores de apoyo (ej. picos o caídas drásticas).

### Restricción de Entrega
