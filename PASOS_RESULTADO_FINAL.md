# Pasos seguidos para llegar al resultado final

## 1. Revisión inicial del proyecto
- Revisé la estructura del workspace para identificar archivos base.
- Confirmé que el servidor Flask entrega index.html y assets estáticos.
- Verifiqué que no existía una implementación previa del dashboard.

## 2. Definición de la estrategia de implementación
- Decidí implementar el dashboard como sitio estático semántico en HTML.
- Separé responsabilidades en:
  - index.html para estructura y contenido.
  - src/styles.css para tema y estilos fuente.
  - styles.css como salida compilada final.

## 3. Preparación del entorno frontend local
- Inicialicé npm en el repositorio.
- Instalé dependencias locales:
  - tailwindcss
  - @tailwindcss/cli
  - charts.css
- Añadí scripts de compilación en package.json para generar styles.css.

## 4. Construcción de la interfaz principal
- Creé una maquetación mobile-first con semántica completa:
  - header
  - nav
  - aside
  - main
  - section
  - article
  - footer
- Usé Grid para distribución general y Flexbox para componentes internos.
- Apliqué breakpoints sm, md y lg.

## 5. Sistema de diseño y marca
- Configuré variables de color en el bloque @theme:
  - Instagram, TikTok, YouTube
  - Éxito, alerta y crítico
  - Escala neutral de grises
- Definí patrones consistentes para tarjetas KPI, tablas, chips y paneles.
- Apliqué tipografía y valores tabulares para alinear métricas.

## 6. Accesibilidad (A11y)
- Incorporé estructura semántica y atributos aria en navegación, filtros y tablas.
- Aseguré foco visible con focus-visible.
- Mantuvé contraste visual robusto y textos alternativos en captions.

## 7. Integración de gráficos con Charts.css
- Implementé:
  - Embudo de conversión
  - Barras por plataforma
  - Barras por producto
- Configuré colores de barras usando variables de marca y soporte.

## 8. Modelado de datos de negocio
- Simulé portafolio y métricas realistas:
  - Producto A: 50 EUR
  - Producto B: 120 EUR
  - Producto C: 80 EUR
  - Comisión: 15 por ciento por venta
- Construí bloques de KPI, tablas operativas y panel de alertas.

## 9. Correcciones durante compilación
- Primer ajuste:
  - Corregí la importación de Charts.css a su ruta resoluble desde src/styles.css.
- Segundo ajuste:
  - Eliminé un uso no compatible de @apply sobre clase custom (surface-card) en Tailwind v4.
- Resultado:
  - Compilación exitosa de styles.css.

## 10. Resolución del solapamiento en Rendimiento por producto
- Identifiqué que la superposición venía de capas visuales internas de Charts.css en tablas bar.
- Solución aplicada:
  - Encapsulé los gráficos en contenedores dedicados.
  - Añadí aislamiento visual y recorte de desborde para separar contextos.
  - Ajusté estructura para evitar interferencia entre bloques.
- Recompilé y validé nuevamente.

## 11. Validación final
- Verifiqué que no quedaran errores en:
  - index.html
  - src/styles.css
  - styles.css
  - package.json
- Confirmé que el dashboard quedó funcional, consistente y sin superposiciones visuales.

## 12. Entregables finales
- index.html con dashboard completo.
- src/styles.css con sistema de diseño, tema y utilidades.
- styles.css compilado para ejecución.
- package.json con scripts de build.
- Documento actual con trazabilidad del proceso.
