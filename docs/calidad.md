# Calidad y límites

El objetivo es escoger la mejor calidad que se pueda demostrar en el hardware disponible, conservando una opción ligera cuando resulte útil.

## Método de comparación

1. Usar instrucciones equivalentes y referencias sintéticas o autorizadas.
2. Fijar versiones, revisión de pesos, semilla y parámetros; registrar los valores realmente resueltos.
3. Medir tiempo de carga e inferencia, memoria de GPU y RAM. Distinguir el pico de un proceso de la memoria total del sistema.
4. Guardar originales y revisar el resultado visual o auditivo. Las estadísticas de nitidez, volumen o espectro son auxiliares; no demuestran por sí solas identidad, naturalidad ni fidelidad.
5. Conservar el modelo anterior hasta tener una mejora comprobada. No declarar superioridad general desde una muestra.

## Resultados generales comprobados

- FLUX.2 Klein 4B base FP8 produjo una imagen de 1024 × 1024 en el perfil de 8 GB VRAM y 16 GB RAM, usando descarga dinámica de pesos y VAE en CPU. La prueba de cartel presentó un error ortográfico: no se promete texto exacto generado por el modelo.
- La edición por instrucciones con FLUX.2 cambió el color de un objeto en una referencia sintética a 1024 × 1024. El resultado mantuvo visualmente la composición en esa muestra, con variaciones de píxeles fuera del objeto. El trabajo tardó aproximadamente dos minutos y medio. Para conservar exactamente la zona exterior existe un flujo distinto de inpainting con composición enmascarada. La validación de importación y diseño del flujo en la interfaz visual se registra por separado.
- Qwen3-TTS 0.6B y 1.7B generaron muestras españolas con la misma referencia sintética y su transcripción correcta. Ambos caben en el perfil probado. La preferencia perceptual debe contrastarse mediante escucha.
- FaceFusion con GFPGAN produjo una restauración más definida en una muestra pequeña; el alisado de piel y la fidelidad de identidad requieren revisar otras referencias.
- ACE-Step generó instrumentales y aceptó letras mediante su API. La primera muestra con letra fue una introducción instrumental. En una segunda muestra de 30 segundos, Gemini/Antigravity informó una escucha directa: vocalizaciones aproximadamente desde el segundo 12 y dos versos en español aproximadamente desde el segundo 19. Los versos restantes no entraron antes del final. La capacidad de canto tiene esa evidencia auditiva atribuida; todavía no se garantiza entrega completa de letras ni entrada vocal inmediata.
- Wan 2.1 1.3B produjo una vista previa de 17 fotogramas a 512 × 288, con 20 pasos. Una segunda prueba completó 33 fotogramas a 832 × 480 con 50 pasos y decodificación VAE por bloques en CPU: aproximadamente 18 minutos, pico observado de 7,2 GiB de memoria GPU total y 12,1 GiB de RAM del sistema. El MP4 pasó una decodificación completa, pero los fotogramas inicial y final presentaron bandas visibles en el fondo y encuadre casi estático. Este perfil todavía no se recomienda como mejora de calidad. Una comparación con los mismos parámetros y VAE por bloques en GPU terminó en aproximadamente 4 minutos, 4,38 veces más rápido, con pico observado de 7,2 GiB de GPU y 11,3 GiB de RAM del sistema. El primer fotograma resultó visualmente equivalente y conservó las bandas: se comprobó mayor velocidad, no mayor calidad visual. La configuración anterior permanece disponible. No se extrapolan estas muestras a video largo ni se confunde una diferencia de píxeles con movimiento útil.

La duración máxima de cuatro segundos ofrecida por el panel produjo 65 fotogramas a 512 × 288. El recorrido real tardó aproximadamente 104 segundos, incluido el arranque, con pico muestreado de 6,9 GiB de memoria GPU total y 12,4 GiB de RAM del sistema. El MP4 pasó una decodificación completa. La inspección del inicio, medio y final mostró una escena coherente con aspecto ilustrado pese a solicitar fotorrealismo; no sustituye una revisión temporal completa. Las miniaturas y ocho originales también se entregaron mediante conexiones HTTP persistentes mientras esa inferencia estaba activa.

Se evalúa por separado un perfil de cuatro segundos a 832 × 480 y 50 pasos para acercarse a la resolución recomendada por el [repositorio oficial de Wan 2.1](https://github.com/Wan-Video/Wan2.1). Sigue siendo una prueba, sin mejora visual confirmada ni cambio del perfil rápido.

## Pendientes

- Más escenas y edición guiada con los modelos de imagen candidatos.
- Mejorar la entrada de voz y comprobar la entrega completa de letras propias.
- Comparar perfiles de video con mayor calidad dentro de los límites reales.
- Completar la revisión visual del panel y la integración de las opciones nuevas.
- Las voces comerciales opcionales requieren disponibilidad y autorización de uso; no se redistribuyen aquí.

## Ejemplos ficticios

- Imagen: «Un velero rojo sobre un lago tranquilo al amanecer».
- Voz: «Esta es una demostración sintética del estudio local».
- Música instrumental: «Piano suave y guitarra acústica, ambiente tranquilo».
- Letra original: «Una luz sobre el mar / nos invita a imaginar».
