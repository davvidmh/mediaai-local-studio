# Instalación y fuentes oficiales

Esta es una guía de componentes. El repositorio público de documentación no contiene el lanzador ni el código del panel local, por lo que clonar este repositorio no instala el estudio.

1. Comprueba GPU, VRAM, RAM y espacio. Reserva espacio para archivos temporales y modelos; carga un solo motor pesado a la vez.
2. Usa entornos Python independientes para voz, música y FaceFusion. Conserva ComfyUI en su propio entorno. Evita modificar el Python global o los controladores por rutina.
3. Instala desde los proyectos oficiales y sigue sus versiones compatibles:

| Componente | Fuente |
| --- | --- |
| ComfyUI | https://docs.comfy.org/installation/comfyui_portable_windows |
| FLUX.2 Klein | https://docs.comfy.org/tutorials/flux/flux-2-klein |
| Qwen3-TTS | https://github.com/QwenLM/Qwen3-TTS |
| ACE-Step | https://github.com/ace-step/ACE-Step-1.5 |
| FaceFusion | https://docs.facefusion.io/installation |
| Wan | https://github.com/Wan-Video/Wan2.1 |
| FFmpeg | https://ffmpeg.org/download.html |
| Shotcut | https://www.shotcut.org/download/ |
| Audacity | https://www.audacityteam.org/download/windows/ |

4. Descarga los pesos de las cuentas oficiales. Fija una revisión, registra su licencia y verifica SHA-256. No reemplaces una instalación funcional antes de probar la alternativa.
5. Ubica aplicaciones, entornos, modelos, cachés y salidas dentro de una carpeta de trabajo elegida por ti. Los ejemplos usan rutas relativas ficticias.
6. Ejecuta las interfaces en localhost. Después de descargar los pesos, comprueba la inferencia con caché local y modo offline de los clientes que lo soporten. Esta configuración no equivale por sí sola a una auditoría de tráfico de todos los procesos.
7. Prueba creación, apertura, guardado, parada y reinicio. Conserva evidencia local sin subir medios personales al repositorio.

No se ofrece una orden universal de instalación: CUDA, PyTorch, bibliotecas y licencias deben revisarse para el sistema de destino.
