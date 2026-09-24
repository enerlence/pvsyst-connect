# Qué puede y qué no puede hacer el asistente

Suntropy Connect decide qué puede hacer un asistente de IA (Claude, ChatGPT
o cualquier cliente MCP) en tu ordenador. Las reglas se aplican **en el
propio ordenador**, antes de ejecutar cada petición. El asistente no puede
cambiarlas.

## Lo que decides tú

En Suntropy Connect, en **Conexión → Permisos del asistente**:

| Ajuste | Efecto |
|---|---|
| **Solo leer** | Explorar proyectos, variantes, resultados ya calculados y archivos de las carpetas autorizadas. Sin simulaciones, sin crear nada. |
| **Leer y simular** | También lanzar simulaciones, crear sites y convertir archivos meteorológicos. Cada una consume una ejecución de tu licencia de PVsyst. |
| **Leer, simular y crear** | También crear y editar proyectos, variantes y archivos en la biblioteca de Suntropy de ese ordenador. |
| **Máximo de ejecuciones de licencia al día** | Número máximo de ejecuciones de licencia al día que pueden lanzar los asistentes. Al alcanzarlo, las simulaciones se detienen hasta el día siguiente; la lectura sigue funcionando. |
| **Pausar el acceso de los asistentes** | Nada de nada hasta que lo reanudes. También disponible desde el icono de la bandeja. |

Y en **Conexión → Carpetas autorizadas**: las únicas carpetas que puede ver
el asistente, además de la biblioteca de Suntropy. Suntropy Connect puede
buscar workspaces de PVsyst y carpetas de PV*SOL en tu disco, pero solo las
**propone**; tú marcas cuáles compartir. Puedes quitar cualquier carpeta en
cualquier momento.

Esa misma pantalla muestra un registro de las últimas peticiones: qué se
pidió, sobre qué proyecto, y si se completó, falló o se bloqueó.

## Lo que nunca puede hacer, sea cual sea la configuración

- Cambiar, mover o borrar nada de tus propias carpetas de PVsyst o PV*SOL.
  Las lee, y las simulaciones se ejecutan sobre copias.
- Ver carpetas que no hayas autorizado, ni el resto de tu disco.
- Ejecutar otros programas o comandos: solo las operaciones de PVsyst
  listadas en el conector.

## Adónde van tus datos

- **Los proyectos y la licencia se quedan en tu ordenador.** Las
  simulaciones se ejecutan con tu propio PVsyst, a través de su línea de
  comandos, en tu máquina.
- La app mantiene una conexión **saliente** hacia Suntropy; no se abre
  ningún puerto en tu ordenador.
- Lo que pide el asistente (un resumen de proyecto, resultados de una
  simulación, un gráfico) viaja desde tu ordenador, a través de Suntropy,
  hasta el asistente, solo cuando se solicita. Suntropy no guarda copias de
  los archivos de tus proyectos.
- Archivos como informes en PDF o CSV horarios se entregan al asistente
  como un **enlace de descarga que caduca a las 24 horas** y que se sirve
  directamente desde tu ordenador.
- El historial de trabajos de simulación se guarda en tu ordenador.
- El asistente inicia sesión con **tu cuenta de Suntropy** mediante OAuth, y
  tú apruebas cada asistente en una página de consentimiento que enumera
  estos mismos permisos. Lo que el asistente haga después con las
  respuestas depende de su proveedor (Anthropic, OpenAI…) y de tus ajustes
  allí.

## Revocar el acceso

- Elimina el conector en los ajustes del asistente, o
- desconecta el ordenador de Suntropy (Conexión → Desconectar este
  ordenador, o desde tu cuenta de Suntropy), o
- pausa el acceso desde el icono de la bandeja.
