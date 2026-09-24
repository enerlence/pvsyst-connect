# Suntropy Connect para PVsyst y PV*SOL

Descargas y actualizaciones del programa de escritorio que conecta el **PVsyst
con licencia instalado en tu ordenador** con Suntropy y con un asistente de IA.

**[Descargar para Windows](https://github.com/enerlence/pvsyst-connect/releases/latest)**

Requiere Windows y PVsyst 8.x con licencia activa. No hace falta ser
administrador para instalarlo. El programa está en español y en inglés: sigue
el idioma del sistema y se cambia en Conexión → Idioma o desde el icono de la
bandeja.

*English version: [README.md](README.md).*

## Guías

- [Conectar Claude](docs/es/conectar-claude.md): claude.ai, Claude Desktop y Claude Code.
- [Conectar ChatGPT](docs/es/conectar-chatgpt.md): modo desarrollador de chatgpt.com.
- [Qué puede y qué no puede hacer el asistente](docs/es/permisos-y-privacidad.md): permisos, datos y privacidad.
- [Ejemplos de peticiones](docs/es/ejemplos.md): qué pedirle una vez conectado.

## Qué hay aquí

Sólo los binarios publicados. **El código fuente no está en este repositorio**:
vive en uno privado, y aquí se publican únicamente las versiones ya compiladas
y el fichero de metadatos que usa el actualizador automático del programa.

| Fichero | Para qué |
|---|---|
| `PVsystConnect-Setup-<version>.exe` | El instalador. Es lo que hay que descargar |
| `latest.yml` | Lo lee el propio programa para saber si hay versión nueva |
| `*.blockmap` | Deja que una actualización descargue sólo lo que ha cambiado |

El programa se actualiza solo: comprueba si hay versión nueva, se la descarga
en segundo plano y avisa. Nunca se reinicia por su cuenta mientras está
atendiendo una simulación.

## Qué hace el programa

Tu licencia de PVsyst y tus proyectos **no salen de tu ordenador**. El programa
abre una conexión saliente hacia Suntropy —no hay que abrir ningún puerto ni
tocar el cortafuegos— y atiende lo que se le pide desde ahí: leer proyectos,
lanzar simulaciones y devolver resultados.

Se puede revocar en cualquier momento desde la web de Suntropy.

## Aviso de Windows al instalar

El instalador todavía no está firmado con un certificado de editor, así que
Windows SmartScreen puede avisar de que no reconoce al autor. Es esperable
mientras no haya certificado: en «Más información» → «Ejecutar de todas formas».

## Más

- Presentación: <https://pvsyst-connect.suntropy.ai>
- Suntropy: <https://suntropy.ai>
