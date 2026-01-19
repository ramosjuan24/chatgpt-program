# Solución para aplicación web/web mobile de marcos personalizados

## Objetivo
Construir una aplicación web responsiva (desktop y mobile) que permita al cliente comprar marcos personalizados en un flujo máximo de 5 pasos, incorporando asesoría de imagen basada en selfie y reconocimiento facial para recomendar los diseños ideales.

## Resultado esperado
- Flujo completo desde selfie hasta pago en **≤ 5 pasos**.
- Recomendaciones personalizadas explicadas de forma clara.
- Checkout simple con carrito y confirmación de orden.

## Alcance funcional (MVP)
1. **Selfie / Foto**
   - Captura desde cámara (WebRTC) o carga de imagen.
   - Validación de calidad (iluminación, rostro centrado).
2. **Análisis automático**
   - Detección facial y puntos clave.
   - Colorimetría básica (subtono, contraste, temperatura).
   - Visagismo (forma del rostro).
3. **Resultados**
   - Resumen de atributos + paleta de color.
   - Reglas claras de recomendación.
4. **Selección y personalización**
   - Filtros inteligentes y prueba virtual (2D).
   - Comparación de 2–3 marcos.
5. **Carrito y compra**
   - Resumen, dirección, pago y confirmación.

## Requerimientos no funcionales
- **Performance**: análisis en < 5 s en dispositivos móviles medios.
- **Privacidad**: consentimiento explícito y eliminación de datos.
- **Accesibilidad**: contrastes, tipografías legibles, navegación simple.
- **Escalabilidad**: microservicios o módulos desacoplados.

## Arquitectura de solución
### Frontend (Web/Mobile)
- **React/Next.js** con diseño mobile-first.
- UI en 5 pasos con progreso visible.
- Integración de cámara y preview.

### Backend
- **API** para procesamiento de imágenes y recomendaciones.
- Servicio de catálogo y stock.
- Servicio de órdenes y pagos.

### IA/ML
- **Detección facial**: MediaPipe FaceMesh.
- **Colorimetría**: extracción de tonos de piel + reglas.
- **Visagismo**: clasificación de forma del rostro.
- **Recomendaciones**: reglas de negocio + ranking básico.

## Flujo de datos (alto nivel)
1. Usuario captura selfie.
2. Imagen → API de análisis facial.
3. Resultado → perfil de asesoría.
4. Perfil → motor de recomendaciones.
5. Resultados → selección de producto.
6. Checkout → creación de orden.

## Modelo de datos (simplificado)
- **UserSession**: id, idioma, dispositivo.
- **FaceProfile**: formaRostro, subtono, contraste, paleta.
- **Recommendation**: marcoId, score, explicación.
- **Cart**: items, precio, impuestos.
- **Order**: estado, envío, pago.

## UX/UI propuesto (pantallas clave)
1. **Landing**: valor principal + CTA “Comenzar”.
2. **Selfie**: cámara, tips y botón continuar.
3. **Resultados**: resumen visual y paleta.
4. **Catálogo**: filtros inteligentes + prueba virtual.
5. **Checkout**: carrito, datos y pago.

## Reglas de recomendación (ejemplo)
- Rostro **ovalado**: marcos rectangulares o cuadrados.
- Subtono **cálido**: tonos dorados o marrón.
- Contraste **alto**: colores más sólidos y oscuros.

## Seguridad y privacidad
- Consentimiento explícito antes de analizar imágenes.
- Almacenamiento cifrado temporal o procesamiento local.
- Opción de eliminación inmediata de selfie.

## Roadmap de implementación
### Fase 1 (4–6 semanas)
- Flujo selfie → análisis → resultados.
- Motor de recomendaciones por reglas.
- Catálogo y checkout básico.

### Fase 2 (6–8 semanas)
- Prueba virtual 2D/3D.
- Recomendaciones basadas en IA ligera.
- Panel administrativo de productos.

### Fase 3 (8–12 semanas)
- Analítica avanzada y A/B testing.
- Optimización de modelo de visagismo.
- Integraciones adicionales de pago/envío.

## Próximos pasos
1. Validar requisitos de negocio y catálogo.
2. Diseñar prototipo UI en Figma.
3. Desarrollar MVP con las fases 1 y 2.
4. Lanzar piloto y optimizar con métricas.

---
Si deseas, puedo convertir esto en un documento técnico con historias de usuario, backlog detallado y estimaciones de costos.
