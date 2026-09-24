# Conectar Claude a PVsyst

Una vez que Suntropy Connect está instalado y tu ordenador está conectado a
Suntropy, Claude puede leer tus proyectos de PVsyst, lanzar simulaciones y
preparar informes en ese ordenador. Esta guía te llevará unos dos minutos.

## Antes de empezar

- **Suntropy Connect** instalado en el ordenador Windows que tiene PVsyst, y
  conectado: la pestaña **Conexión** muestra una luz verde. Consulta el
  [README](../../README.es.md) para descargarlo.
- Un plan de **Claude** que permita conectores personalizados: Pro, Max, Team
  o Enterprise. En Team y Enterprise, un propietario de la organización tiene
  que añadir el conector primero, desde los ajustes de la organización.

## Opción 1: un clic desde la app

En Suntropy Connect, ve a **Conexión → Conectar un asistente → Claude** y
pulsa **Añadir a Claude**. Claude abre el diálogo «Añadir conector
personalizado» con el nombre y la dirección ya rellenados. Compruébalos y
confirma.

## Opción 2: a mano

1. En Claude, abre **Ajustes → Conectores** y elige **Añadir conector
   personalizado**.
2. Rellena:
   - **Nombre:** `PVsyst Connect`
   - **URL del servidor MCP remoto:** `https://pvsyst-connect-gateway.suntropy.ai/pvsyst/mcp`
3. Pulsa **Añadir** y luego **Conectar**.
4. Claude abre Suntropy. Inicia sesión con tu cuenta de Suntropy. Una página
   de consentimiento enumera exactamente qué podrá hacer el asistente y qué
   no; si fuiste tú quien añadió el conector, pulsa **Authorise**.

Para PV*SOL, repite el proceso con el nombre `PV*SOL Connect` y la dirección
`https://pvsyst-connect-gateway.suntropy.ai/pvsol/mcp`. El conector de PV*SOL
es de solo lectura: PV*SOL no tiene línea de comandos, así que se limita a
leer los resultados ya guardados en tus proyectos.

## Usarlo en una conversación

En un chat nuevo, abre el menú **+** → **Conectores** y asegúrate de que
**PVsyst Connect** está activado. Después, simplemente pregunta, por ejemplo:

> Lista mis proyectos de PVsyst y resume el sistema del más reciente.

Más ideas en [Ejemplos de peticiones](ejemplos.md).

Claude te pide confirmación antes de usar herramientas que cambian algo
(crear un proyecto, editar una variante). Las simulaciones consumen
ejecuciones de tu licencia de PVsyst: comprueba cuántas te quedan con
*«¿Cuántas ejecuciones de licencia de PVsyst me quedan?»*.

## Claude Code

Un solo comando, usando la credencial del ordenador conectado en lugar de
OAuth:

```
claude mcp add --transport http pvsyst https://pvsyst-connect-gateway.suntropy.ai/pvsyst/mcp --header "x-api-key: TU_CLAVE"
```

Suntropy Connect muestra el comando exacto con tu clave en
**Conexión → Conectar un asistente → Claude**, con un botón para copiarlo.

## Solución de problemas

- **«No hay ningún worker de PVsyst registrado» / el ordenador no
  responde:** Suntropy Connect tiene que estar en marcha y conectado en el
  ordenador con PVsyst. Busca su icono en la bandeja de Windows.
- **Rechazo por «Permisos del asistente»:** el asistente ha intentado algo
  que no has permitido en ese ordenador (por ejemplo, una simulación
  mientras el acceso está en *Solo leer*, o el acceso está en pausa).
  Cámbialo en Suntropy Connect, en **Conexión → Permisos del asistente**. El
  asistente no puede cambiarlo.
- **Falta una carpeta:** el asistente solo ve la biblioteca de Suntropy y
  las carpetas que hayas autorizado. Añádela en **Conexión → Carpetas
  autorizadas**.
- **Las herramientas nuevas no aparecen tras una actualización:** desconecta
  y vuelve a conectar el conector en los ajustes de Claude para refrescar la
  lista de herramientas.

## Desconectar

Elimina el conector en **Ajustes → Conectores** de Claude. Para cortar el
acceso a todos los asistentes a la vez, desconecta el ordenador de Suntropy,
o pausa el acceso desde el icono de la bandeja.
