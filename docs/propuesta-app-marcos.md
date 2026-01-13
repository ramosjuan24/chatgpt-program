# Propuesta de aplicación web/web mobile para venta de marcos personalizados

## Objetivo
Crear una aplicación web responsiva (desktop y mobile) que permita al cliente comprar marcos de lentes personalizados en un flujo simple (máximo 5 pasos), incorporando asesoría de imagen basada en captura de selfie y reconocimiento facial para sugerir diseños ideales.

## Perfil del usuario
- **Cliente final** que busca marcos personalizados y asesoría de imagen rápida.
- **Nivel de habilidad digital**: básico a intermedio.
- **Objetivo principal**: obtener recomendaciones confiables y comprar sin fricción.

## Principios de experiencia (UX)
- **Flujo en 5 pasos máximo**: desde selfie hasta compra.
- **Lenguaje claro** y guías visuales.
- **Feedback inmediato**: resultados y explicaciones concisas.
- **Accesible y responsivo**: mobile-first.

## Flujo principal (5 pasos)
1. **Captura selfie / subir foto**
   - Guía visual y consejos de iluminación.
   - Validaciones básicas: rostro centrado, buena iluminación.
2. **Análisis automático**
   - Reconocimiento facial.
   - Colorimetría personal (subtono, contraste, intensidad).
   - Visagismo (forma del rostro: ovalado, cuadrado, redondo, triangular, etc.).
   - Morfología corporal (si aplica, opcional).
3. **Resultados y perfil**
   - Resumen de atributos clave.
   - Paleta de color sugerida.
   - Tipologías de armazones recomendados.
4. **Personalización y selección**
   - Filtros: material, tamaño, color, estilo.
   - “Probar virtualmente” (lente 2D/3D sobre selfie).
   - Comparación de 2-3 opciones.
5. **Carrito y compra**
   - Resumen de producto.
   - Opciones de pago y envío.
   - Confirmación y seguimiento.

## Funcionalidades clave
### Captura y reconocimiento
- Cámara en navegador (WebRTC) o subida de imagen.
- Detección de rostro y puntos faciales.
- Validaciones automáticas de calidad.

### Análisis de asesoría de imagen
- **Colorimetría**: subtono, temperatura y contraste.
- **Visagismo**: forma de rostro y proporciones.
- **Morfología**: análisis opcional con parámetros básicos.
- **Recomendaciones**: estilos y colores óptimos.

### Catálogo y recomendación
- Catálogo con filtros inteligentes basados en el perfil.
- Motor de recomendación (reglas + IA)
- Descripciones con “por qué” se recomienda cada marco.

### Compra
- Carrito sencillo con edición rápida.
- Checkout en 1 paso si es posible.
- Métodos de pago locales.

## Arquitectura sugerida
- **Frontend**: React/Next.js, diseño mobile-first.
- **Backend**: Node.js o Python (FastAPI).
- **IA/ML**:
  - Detección facial: MediaPipe o FaceMesh.
  - Análisis de colorimetría: extracción de tonos de piel.
  - Recomendaciones: reglas + modelos ligeros.
- **Infraestructura**: CDN para imágenes, almacenamiento seguro.

## Diseño UI/UX propuesto
- **Pantalla inicial**: propuesta de valor y botón “Comenzar”.
- **Paso a paso** con barra de progreso.
- **Resultados visuales**: paleta de color + ejemplos.
- **Catálogo** con filtros contextuales.

## Requisitos de privacidad
- Consentimiento explícito para uso de imágenes.
- Procesamiento seguro de imágenes (idealmente local o con cifrado).
- Opción de eliminar datos y fotografías.

## Métricas clave
- Conversión de selfie a compra.
- Tiempo promedio de flujo.
- Tasa de abandono por paso.
- Satisfacción del cliente (NPS).

## Próximos pasos recomendados
1. **Discovery**: investigación con clientes reales.
2. **Prototipo** en Figma con los 5 pasos.
3. **MVP** con análisis facial y recomendaciones básicas.
4. **Iteración** con datos reales.

---
Si deseas, puedo desarrollar un prototipo visual o definir el roadmap técnico con prioridades, costos aproximados y tiempos de implementación.
