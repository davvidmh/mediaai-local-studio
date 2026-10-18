# MediaAI Local Studio

Documentación de un estudio creativo que procesa imágenes, audio y video en una computadora local, con un panel sencillo en español.

Este repositorio contiene documentación y configuración ficticia. No incluye modelos, instaladores, medios de usuarios, grabaciones, fotografías, credenciales ni la implementación privada del panel.

## Funciones y estado

| Área | Herramientas | Estado comprobado |
| --- | --- | --- |
| Imágenes | ComfyUI, DreamShaper 8, FLUX.2 Klein 4B base FP8 | Generación local a 512 y 1024 píxeles; edición por máscaras y ampliación disponibles |
| Voz | Qwen3-TTS 0.6B y 1.7B Base | Síntesis en español y clonación con referencia sintética; selector y transcripción probados mediante la API del panel; revisión visual pendiente |
| Música | ACE-Step 1.5 Turbo | Instrumentales locales; entrada de letras e idioma integrada, canto todavía en validación |
| Rostros | FaceFusion y GFPGAN 1.4 | Intercambio y restauración probados con material de demostración; calidad dependiente de la referencia |
| Video IA | Wan 2.1 T2V 1.3B | Vista previa corta de 512 × 288 y 17 fotogramas verificada; formatos superiores pendientes |
| Edición | FFmpeg, Shotcut, Audacity | Herramientas locales de conversión y edición instaladas |

El perfil de referencia tiene una GPU de **8 GB de VRAM** y **16 GB de RAM**. Una prueba funcional no demuestra que un modelo sea el mejor para todos los casos.

## Cómo se organiza

El panel permite describir una creación, seleccionar opciones sencillas, previsualizar resultados y abrir las interfaces completas. Un registro comprueba la identidad de cada proceso antes de detenerlo. Los motores pesados se ejecutan de uno en uno.

- [Instalación y fuentes oficiales](docs/instalacion.md)
- [Arquitectura](docs/arquitectura.md)
- [Criterios de calidad y límites](docs/calidad.md)
- [Privacidad de la publicación](docs/privacidad.md)
- [Configuración ficticia](examples/config.example.json)

## Desarrollo en curso

Se comparan calidad visual y auditiva, fidelidad, memoria y tiempo antes de recomendar cambios. El reconocimiento de una reserva externa de inferencia, el inicio y la parada de interfaces y la preservación fuera de una máscara tienen comprobaciones específicas.

Quedan pendientes la revisión visual completa del panel, la comparación de más escenas, la validación de voz cantada y la disponibilidad de voces comerciales opcionales. Qwen3-TTS no es el motor propietario Loquendo.

## Licencias y referencias

El código y los pesos de cada proyecto conservan sus propias licencias. Consulta las fuentes antes de redistribuir o dar un uso comercial a los modelos. Las referencias de voz y rostro deben ser propias, sintéticas o autorizadas.
