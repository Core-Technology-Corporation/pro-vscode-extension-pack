# Alvaro's Pro Dev Pack (Pro VSCode Extension Pack)

## Descripción breve (tarjeta)

Paquete que instala en un solo paso las cinco extensiones del ecosistema **Pro VSCode**: tema, atajos, snippets, herramientas y asistente de IA.

## Descripción completa

Extension Pack de VS Code que agrupa:

| Extensión | Qué aporta |
|---|---|
| Pro VSCode Themes | Tema Pro Dark generado a partir de tokens de color |
| Pro VSCode Keybindings | Atajos de teclado, Smart Run, flujo de commits y limpieza de código |
| Pro VSCode Snippets | Snippets de JavaScript, HTML y React Native |
| Pro VSCode Tools | JSON → TypeScript, generador de componentes y Quick Actions |
| Pro VSCode AI | Asistente de IA con cinco proveedores |

Instalar el pack instala las cinco extensiones, que siguen siendo independientes: cada una se puede desactivar o desinstalar por separado.

## Problema que resuelve

Configurar un entorno de trabajo completo implica buscar e instalar varias extensiones una por una. El pack lo reduce a una sola instalación.

## Objetivo

Distribuir de forma unificada el entorno de desarrollo personal y presentar las cinco extensiones como un ecosistema coherente.

## Público objetivo

Desarrolladores que quieren un entorno de VS Code listo para usar.

## Mi participación técnica

Confirmado por el historial de git: autor del pack (3 commits, 2026-07-09 → 2026-07-10) y de las cinco extensiones que incluye.

## Funcionalidades destacadas

- Instalación con un clic o `code --install-extension alvarosiles.pro-vscode-extension-pack`.
- Documentación de cada extensión (`docs/extensions.md`) y hoja de ruta (`docs/roadmap.md`).

## Tecnologías

| Categoría | Tecnologías |
|---|---|
| Plataforma | VS Code Extension Pack (`extensionPack` en `package.json`), VS Code ^1.85 |
| Ecosistema | TypeScript, esbuild, Node.js, SDKs de Anthropic, OpenAI y Google (en las extensiones incluidas) |
| Publicación | `vsce` |

## Arquitectura

Cinco repositorios independientes, cada uno con su ciclo de versiones, que este pack agrupa para distribuirlos. El pack no tiene código propio.

## Seguridad

El pack no ejecuta código. Las consideraciones de seguridad son las de cada extensión; las API keys de la extensión de IA se guardan en `SecretStorage`.

## Retos técnicos

Coordinar las versiones y los IDs de publicación entre cinco repositorios.

## Mejoras futuras recomendadas

- **Corregir el ID de la extensión de snippets**: el pack referencia `alvarosiles.pro-snippets`, pero la extensión se llama `pro-vscode-snippets`.
- Alinear `docs/extensions.md` con el contenido real de cada extensión.

## Estado

Versión `1.0.0`, publicada en el Marketplace. Las cinco extensiones también están publicadas (verificado el 2026-10-20), pero el pack referencia `alvarosiles.pro-snippets`, un ID que no existe en el Marketplace, así que la extensión de snippets no se instala con el pack hasta corregirlo.

## Capturas

| Archivo | Contenido |
|---|---|
| `presentacion/01-vista-principal.png` | Las cinco extensiones cargadas a la vez: tema Pro Dark, panel **Pro AI** abierto y `package.json` del pack con `extensionPack`. |
| `presentacion/02-funcionalidad-principal.png` | El pack en uso: README del pack con la tabla de extensiones y la vista **Pro Tools: Quick Actions** activa, con el tema Pro Dark. |
| `presentacion/03-funcionalidad-complementaria.png` | Editor de atajos filtrado por `@source:extension`, con los atajos de Pro VSCode Keybindings activos dentro del entorno del pack. |

Capturas de las extensiones ejecutándose juntas en un *Extension Development Host* (cargadas desde copias locales de los repositorios).
