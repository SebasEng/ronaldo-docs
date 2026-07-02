# Assets / Imagenes del Proyecto Ronaldo

Coloca aqui las imagenes del proyecto. Los nombres de archivo deben ser **exactamente** estos para que el sitio los encuentre automaticamente.

## Imagenes Principales

| Archivo | Descripcion | Estado |
|---------|-------------|--------|
| `ibero-logo.png` | Logo de la Universidad Iberoamericana (header de la pagina) | Por conseguir |
| `arquitectura_general.png` | Diagrama de arquitectura general de las 3 capas del sistema | Ya lo tienes |
| `robot_go2.jpg` | Foto del Unitree Go2 Air utilizado en el proyecto | Por conseguir |
| `setup_fisico.jpg` | Foto del setup fisico (laptop + robot + hotspot) | Opcional |
| `rutas_robot.png` | Mapa real de la UIA con las rutas del robot sobrepuestas | Opcional |

## Diagramas (16 placeholders)

Genera cada diagrama con la herramienta que prefieras (Mermaid Live, draw.io, Excalidraw) y guardalo con el nombre exacto indicado.

| # | Archivo | Descripcion | Seccion |
|---|---------|-------------|---------|
| 1 | `diagrama-01-arquitectura-3-capas.png` | Diagrama de flujo de datos entre las 3 capas (Agente Python → Nodos ROS2 → WebRTC → Robot) | 2.2 Diagrama de Capas |
| 2 | `diagrama-02-nodos-ros2-topicos.png` | Arquitectura de nodos ROS2 y topicos (/webrtc_req, /cmd_vel_out, /odom, /go2_states) | 2.2 Diagrama de Capas |
| 3 | `diagrama-03-procesos-eventbus.png` | Los 4 procesos (AudioProcess, Orquestador, Playback, UnitreeRobot) comunicandose via EventBus | 2.3 Procesos y Bus de Eventos |
| 4 | `diagrama-04-cloud-vs-local.png` | Distribucion de computo: hardware local (Vosk, VAD, Edge TTS) vs cloud (Groq STT, LLM, MCP) | 2.5 Cloud vs Local |
| 5 | `diagrama-05-pipeline-voz.png` | Pipeline completo de voz: Microfono → Wake Word → VAD → STT → Clasificador → LLM → TTS → Altavoz | 3.1 Pipeline de Voz |
| 6 | `diagrama-06-estados-audioprocess.png` | Maquina de estados del AudioProcess: WAKE_WORD → LISTENING → COOLDOWN | 3.2 Palabra de Activacion y VAD |
| 7 | `diagrama-07-clasificacion-2-etapas.png` | Sistema hibrido: Clasificador YAML (1ra etapa) + LLM con Tool Calling (2da etapa) | 3.5 Clasificacion de Intenciones |
| 8 | `diagrama-08-tool-calling-secuencia.png` | Diagrama de secuencia Tool Calling: Usuario → LLM → ToolValidator → MCP → DB → Respuesta | 3.6 Motor de Dialogo y Tool Calling |
| 9 | `diagrama-09-arquitectura-mcp.png` | Arquitectura MCP: Agente Ronaldo ↔ Servidor MCP (tools tipadas) ↔ Base de Datos UIA (SQLite) | 3.7 Servidor MCP |
| 10 | `diagrama-10-estados-antifeedback.png` | Diagrama de estados con mecanismos antifeedback: MUTED_MIC y COOLDOWN | 3.9 Mecanismos Antifeedback |
| 11 | `diagrama-11-webrtc-secuencia.png` | Secuencia de handshake WebRTC: HTTP (puerto 9991) → SDP → DataChannel | 4.3 Comunicacion WebRTC |
| 12 | `diagrama-12-ros2-arquitectura.png` | 3 nodos ROS2 principales con sus topicos y comunicacion al robot | 4.4 Nodos ROS2 |
| 13 | `diagrama-13-archivos-json-flujo.png` | Flujo de archivos JSON entre agente Python y workspace ROS2 compartido | 4.5 Sistema de Archivos JSON |
| 14 | `diagrama-14-rutas-campus.png` | Mapa esquematico de rutas: Lab Robotica → Maquinas → Karpa, Giornale, Biblioteca, Biomedica | 4.6 Rutas de Navegacion |
| 15 | `diagrama-15-comando-secuencia.png` | Secuencia de ejecucion de comando: Usuario → Agente → UnitreeRobotClient → ROS2 → WebRTC → Robot | 4.7 Comandos Preprogramados |
| 16 | `diagrama-16-mapeo-resolucion.png` | Flujo de resolucion de ruta: Intencion → robot_routes.yaml → secuencia de rutas → MOVEMENT_COMPLETED | 4.8 Mapeo de Destinos |

## Videos de YouTube (opcionales)

Para embeber en las secciones de evidencia visual:

| # | Contenido | Seccion |
|---|-----------|---------|
| 1 | Robot activandose con wake word "Ronaldo" + comando simple | 3.2 / Inicio |
| 2 | Dialogo conversacional completo con tool calling y navegacion | 3.6 |
| 3 | Ruta de navegacion completa (Lab Robotica → Karpa o similar) | 4.6 |
| 4 | Compilacion de comandos preprogramados (sit, dance, hello) | 4.7 |

## Nota

Si el sitio se construye con Jekyll, coloca todos los archivos en esta carpeta y ejecuta:

```bash
bundle exec jekyll serve
```

Si usas Live Server de VS Code o abres el HTML directamente, asegurate de que las rutas a las imagenes sean correctas.
