# Conectar ChatGPT a PVsyst

ChatGPT puede usar Suntropy Connect como conector personalizado a través de
su **modo desarrollador**. Una vez conectado, puede leer tus proyectos de
PVsyst, lanzar simulaciones y preparar informes en tu ordenador.

## Antes de empezar

- **Suntropy Connect** instalado en el ordenador Windows que tiene PVsyst, y
  conectado: la pestaña **Conexión** muestra una luz verde.
- Un plan de pago de **ChatGPT** (Plus, Pro, Business, Enterprise o Edu). El
  modo desarrollador está disponible en la web, en chatgpt.com. En Business,
  Enterprise y Edu puede que un administrador del workspace tenga que
  habilitarlo.

## Pasos

1. En chatgpt.com, abre **Ajustes → Aplicaciones y conectores → Ajustes
   avanzados** y activa el **Modo desarrollador**. (Suntropy Connect puede
   abrirte esta pantalla directamente: **Conexión → Conectar un asistente →
   ChatGPT → Abrir los conectores de ChatGPT**.)
2. De vuelta en **Aplicaciones y conectores**, elige **Crear** (nuevo
   conector) y rellena:
   - **Nombre:** `PVsyst Connect`
   - **URL del servidor MCP:** `https://pvsyst-connect-gateway.suntropy.ai/pvsyst/mcp`
   - **Autenticación:** OAuth
3. Marca **Confío en esta aplicación** y pulsa **Crear**.
4. ChatGPT abre Suntropy. Inicia sesión con tu cuenta de Suntropy. La página
   de consentimiento enumera exactamente qué podrá hacer el asistente y qué
   no; si fuiste tú quien creó el conector, pulsa **Authorise**.

ChatGPT no acepta un enlace prerrellenado, así que la dirección hay que
pegarla a mano. No necesitas pegar ninguna clave: el inicio de sesión es por
OAuth.

Para PV*SOL, crea un segundo conector llamado `PV*SOL Connect` con
`https://pvsyst-connect-gateway.suntropy.ai/pvsol/mcp` (solo lectura).

## Usarlo en una conversación

En un chat nuevo, abre el menú **+**, elige **Modo desarrollador** y activa
**PVsyst Connect**. Después pregunta, por ejemplo:

> Lanza la simulación de la variante VC0 de mi proyecto «Nave» y enséñame la
> producción mensual.

Más ideas en [Ejemplos de peticiones](ejemplos.md).

En modo desarrollador, ChatGPT te pide confirmación para cada herramienta
que escribe algo. Las simulaciones consumen ejecuciones de tu licencia de
PVsyst.

## Solución de problemas

- **No se puede crear el conector / «URL no segura»:** el modo desarrollador
  solo acepta direcciones `https`. Usa la dirección de arriba, no la local
  (`http://127.0.0.1…`) que muestra la app antes de que el ordenador esté
  conectado.
- **El ordenador no responde:** Suntropy Connect tiene que estar en marcha y
  conectado en el ordenador con PVsyst (icono de la bandeja).
- **Rechazo por «Permisos del asistente»:** cámbialo en Suntropy Connect, en
  **Conexión → Permisos del asistente**. El asistente no puede cambiarlo.
- **Las herramientas nuevas no aparecen tras una actualización:** abre el
  conector en **Aplicaciones y conectores** y actualízalo, o bórralo y
  créalo de nuevo.

## Desconectar

Borra el conector en **Ajustes → Aplicaciones y conectores**. Para cortar el
acceso a todos los asistentes a la vez, desconecta el ordenador de Suntropy
o pausa el acceso desde el icono de la bandeja.
