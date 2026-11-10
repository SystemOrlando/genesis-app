# GÉNESIS · beta

<p align="center">
  <a href="https://systemorlando.github.io/genesis-app/"><img src="demo.gif" alt="GÉNESIS en acción: el inicio de la app y un recorrido por sus paneles" width="800" /></a>
</p>

<p align="center">
  <a href="https://systemorlando.github.io/genesis-app/"><b>▶ Ver el recorrido interactivo</b></a> ·
  <a href="docs/genesis-beta.mp4">Video completo (MP4)</a> ·
  <a href="../../releases/latest"><b>Descargar la beta</b></a>
</p>

**GÉNESIS es un agente de escritorio: le pides algo en palabras normales y lo hace en tu computadora.** Abre programas, busca y ordena archivos, escribe documentos, programa y usa tus servicios (Gmail, Drive, Calendar, GitHub, Notion, Canva y más). No es un chat: es un asistente que *actúa* en tu PC, con los permisos que tú le das. Lo desarrolla **Brakescode**.

> **Esta es una versión beta.** Puede tener errores o cambiar de un día a otro. Si algo falla, cuéntanos: tu reporte decide qué arreglamos primero.

## Por qué GÉNESIS

- **Más de 1000 conectores.** Los del catálogo, los de la comunidad y cualquier servidor MCP publicado en GitHub: se buscan desde la app y se conectan sin tocar archivos.
- **Gratis para empezar, sin claves de API.** Funciona con OpenCode, que es gratuito y no pide cuenta. Si ya pagas Claude, ChatGPT o Gemini, usa tu mismo plan a través de la herramienta oficial de cada empresa: no pagas tokens aparte ni pegas claves.
- **Tus datos se quedan en tu PC.** Archivos, conversaciones y claves viven en tu computadora (las claves, en el llavero de Windows). GÉNESIS solo manda a internet lo que le pides.
- **Puede funcionar sin internet.** Con un **modelo local** (LocalAI) corre una IA en tu propia PC, sin límites de uso, y lo instala solo: detecta tu equipo y elige el modelo que le conviene.
- **Tú pones los límites.** Cuatro niveles de control del ordenador, rutas protegidas, apps vetadas, horario permitido y una palabra clave para lo delicado. Cada herramienta de cada conector se permite, se pregunta o se bloquea.
- **Un equipo, no un solo agente.** Varios agentes trabajan a la vez sobre tu proyecto, cada uno en su propia copia, con roles (programador, pruebas, seguridad, simplificador) y un revisor; tú eliges qué integrar.
- **Hecho para estudiantes y equipos pequeños.** Pensado para laptops normales (por ejemplo, una RTX 3050 con 16 GB de RAM) y en español.

## Qué tiene cada apartado

| Apartado | Qué hace | Lo que ganas |
|---|---|---|
| **Ahora** | Le das una orden por escrito o por voz y ves lo que va haciendo | Resultados en tu PC, no solo texto |
| **Historial** | Cada conversación con sus pasos: qué herramienta usó, con qué y cuánto tardó | Transparencia: sabes qué hizo en tu computadora |
| **Conectores** | **Más de 1000 conectores**: un catálogo de más de 60 con un clic (Gmail, Drive, Calendar, GitHub, Notion, Canva…), los que comparte la comunidad y cualquier servidor MCP de GitHub, que GÉNESIS busca y conecta por ti | Que haga cosas en tus servicios, no solo en tu PC |
| **Permisos** | Por cada herramienta: permitir, preguntar o bloquear | Control fino de lo que puede tocar |
| **Skills** | Instrucciones expertas (PDF, Excel, presentaciones, diseño, programación); algunas ya vienen incluidas | Mejores resultados en tareas concretas |
| **Comunidad** | Skills y conectores que comparte la gente; puedes publicar los tuyos | Aprovechar lo que ya armaron otros |
| **Equipo** | Varios agentes en paralelo sobre un proyecto, con revisión | Tareas grandes más rápido y con menos errores |
| **Directrices** | Qué no puede tocar y cuándo: rutas, apps, horario, palabra clave | Seguridad sobre un asistente que controla tu PC |
| **Avatar** | Nombre, ojos, voz natural y accesorios (chullo, lentes, bufanda…) | Un asistente con personalidad |
| **Ajustes** | Motor (OpenCode gratis o tu plan), modelo local, memoria, modo programación, voz e idioma | Que se adapte a tu equipo y a tu bolsillo |
| **Mensajes de mejora** | Botón BETA: ideas y errores llegan directo al equipo | Que la beta se construya contigo |

Además: **memoria** que sigue el hilo aunque cambies de motor, **modo programación** con método de ingeniería (explorar, cambiar, probar, verificar), **adjuntos** (archivos e imágenes en la orden) y **actualizaciones firmadas** con un clic.

## En qué se parece y en qué se diferencia

GÉNESIS no compite con todo lo que hay; hace una cosa distinta. Esta comparación es para que elijas lo que te conviene:

| | Qué es | Cómo se paga | Dónde actúa | Elígelo cuando… |
|---|---|---|---|---|
| **GÉNESIS** | Agente de escritorio: ejecuta tareas en tu PC y en tus servicios | Gratis con OpenCode, o con tu plan actual; modelo local sin costo | Tu computadora (archivos, programas, pantalla, conectores) | Quieres que *haga* cosas por ti, con límites claros y sin gestionar claves |
| **OpenRouter** | Puerta de entrada (API) a cientos de modelos de distintas empresas, con una sola clave | Por uso: pagas créditos y tokens | Ninguno por sí solo: devuelve texto a tu programa | Eres desarrollador y quieres elegir y cambiar modelos desde tu código |
| **Apps de chat** (ChatGPT, Claude, Gemini) | Chat para conversar, con algunas herramientas | Suscripción propia de cada empresa | Sobre todo en su ventana; el control de tu PC es limitado | Quieres conversar, redactar o analizar sin que toque tu computadora |
| **Agentes de código** (Claude Code, Codex CLI, Cursor) | Agentes para programar, en terminal o editor | Plan o API de cada uno | Tu proyecto de código | Tu trabajo es principalmente programar |
| **Ejecutores locales** (Ollama, LM Studio) | Corren modelos en tu PC y ofrecen chat o API | Gratis | Solo dan el modelo; la acción la pones tú | Quieres el modelo y armar el resto tú mismo |

**La diferencia central con OpenRouter:** OpenRouter te da *acceso a modelos* a cambio de pagar por uso y manejar una clave de API; no hace nada en tu computadora. GÉNESIS es el *agente* que usa un modelo para hacer tareas: puede usar el plan que ya pagas, uno gratuito o uno local, y trae lo que lo hace seguro de usar (permisos, directrices, historial de cada paso). Son capas distintas: el modelo y el agente.

**Con las herramientas de código** (Claude Code, Codex, Cursor): GÉNESIS las usa como motor si las tienes, y suma lo que ellas no cubren: Gmail, Drive y Calendar, ordenar archivos, usar programas, voz, un equipo de agentes con revisión y controles pensados para quien no es programador.

**Lo que GÉNESIS todavía no es:** está en beta y solo para Windows; la calidad del resultado depende del modelo que uses (un modelo local pequeño rinde menos que uno en la nube); y el código no es abierto (ver la licencia).

## Descargar e instalar (Windows 10 u 11, 64 bits)

1. Entra en **[Releases → la última versión](../../releases/latest)** y baja `GENESIS-<versión>-setup.exe`.
2. Ábrelo. No pide permisos de administrador: se instala solo para tu usuario.
3. **Si Windows muestra «Windows protegió tu PC»:** pasa porque el instalador todavía no tiene un certificado de firma de código de pago, no porque tenga un virus. Haz clic en **Más información → Ejecutar de todas formas**. Baja GÉNESIS solo desde esta página: así sabes que es el original.
4. Al abrir la app por primera vez, lee y acepta los términos, inicia sesión con Google o GitHub y sigue la guía rápida (puedes verla otra vez desde **Ajustes → Versión y guía**).

**Qué necesitas:**
- Un motor de IA. **OpenCode es gratis y no pide cuenta**: se instala desde Ajustes → Proveedores. Si tienes Claude, ChatGPT o Gemini, también sirven.
- Opcional: un **modelo local** que corre en tu propia PC, sin límites de uso y sin internet (Ajustes → Modelo local). Va mejor con una tarjeta gráfica NVIDIA (por ejemplo una RTX 3050) y 16 GB de RAM o más.

## Actualizaciones

GÉNESIS busca versiones nuevas al abrirse y cada 6 horas. Cuando hay una, aparece una banda arriba con **«Actualizar ahora»**: la baja, comprueba que la firmó Brakescode y la instala. Un archivo cambiado por el camino no pasa la comprobación y no se instala. La app se cierra y vuelve a abrir sola.

## Cuéntanos qué mejorar

Usa el botón **BETA** de la barra superior, o **Ajustes → Mensajes de mejora**: ideas, errores, conectores o skills que te faltan. Llega al equipo de Brakescode. Si dejas tu correo, te respondemos.

¿Prefieres el correo? Escribe a **contacto@brakescode.com**.

## Tu privacidad

- Tus archivos, conversaciones y claves se quedan en tu PC. Las claves se guardan en el llavero del sistema.
- GÉNESIS solo manda a internet lo que le pides: a tu motor de IA, a los servicios que conectaste y, si nos escribes, tu mensaje.
- En los mensajes de mejora solo va lo que escribes y, si marcas la casilla, la versión de la app, el sistema operativo y el motor que usas.

## Licencia

GÉNESIS es software propietario: se licencia, no se vende. Puedes instalarlo y usarlo en las computadoras que controlas. **No** está permitido descompilarlo, aplicarle ingeniería inversa, redistribuirlo, modificarlo ni usarlo para entrenar modelos de IA. El texto completo, con los términos de la beta, está en [LICENSE](LICENSE).

Este repositorio solo publica los instaladores: el código fuente de GÉNESIS no es público.

© 2026 SystemOrlando · Brakescode. Todos los derechos reservados.
