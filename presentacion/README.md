# Alvaro's Pro Dev Pack

[![Version](https://img.shields.io/badge/version-1.0.0-blue)](CHANGELOG.md)
[![License: MIT](https://img.shields.io/badge/license-MIT-green)](LICENSE)
[![VS Code](https://img.shields.io/badge/VS%20Code-%5E1.85.0-007ACC?logo=visualstudiocode)](https://code.visualstudio.com/)

A curated collection of **Pro VSCode** extensions, bundled into a single install. Get themes, keybindings, snippets, developer tools, and AI assistance set up in one click — no need to search and install each one separately.

## What's included

| Extension | Description |
|---|---|
| 🎨 [Pro VSCode Themes](https://github.com/alvarosiles/pro-vscode-themes) | Professional, low-contrast color themes for long coding sessions. |
| ⌨️ [Pro VSCode Keybindings](https://github.com/alvarosiles/pro-vscode-keybindings) | Productivity-focused keyboard shortcuts for editing, git, debugging, and the terminal. |
| 🧩 [Pro VSCode Snippets](https://github.com/alvarosiles/pro-snippets) | Ready-to-use code snippets for JavaScript, TypeScript, HTML, CSS, and React. |
| 🛠 [Pro VSCode Tools](https://github.com/alvarosiles/pro-vscode-tools) | Everyday developer utilities and commands. |
| 🤖 [Pro VSCode AI](https://github.com/alvarosiles/pro-vscode-ai) | AI-assisted chat, inline edits, code review, and commit messages, with multi-provider support. |

See [docs/extensions.md](docs/extensions.md) for details on each extension.

## Installation

1. Open **Extensions** in VS Code (`Ctrl+Shift+X`).
2. Search for **"Pro VSCode Extension Pack"**.
3. Click **Install** — every extension in the pack installs automatically.

Or install from the command line:

```bash
code --install-extension alvarosiles.pro-vscode-extension-pack
```

## Managing individual extensions

Installing the pack installs all extensions listed above, but you can disable or uninstall any of them individually at any time from the Extensions view — they don't depend on each other.

## Roadmap

Planned additions and ideas for future extensions live in [docs/roadmap.md](docs/roadmap.md).

## Contributing

Found a bug or have a suggestion for one of the bundled extensions? Open an issue in that extension's own repository (linked in the table above). For issues with the pack itself (installation, bundling, missing extensions), open an issue [here](https://github.com/alvarosiles/pro-vscode-extension-pack/issues).

## Technical notes

- This is a pure **Extension Pack**: it has no code, and `package.json` only declares `extensionPack` with five IDs. VS Code installs those extensions from the Marketplace when the pack is installed.
- Requires VS Code `^1.85.0`. Packaged with `vsce package` (no build step).

### Known issues

- **Mismatched ID for the snippets extension.** The pack (and `docs/extensions.md`) reference `alvarosiles.pro-snippets`, but the snippets repository declares `"name": "pro-vscode-snippets"`, so its ID is `alvarosiles.pro-vscode-snippets`. The pack will not find it unless one of the two names is changed.
- All five extensions are published on the Marketplace (checked 2026-10-20). Because of the ID mismatch above, the snippets extension is not installed together with the pack.
- `docs/extensions.md` lists TypeScript and CSS snippets, but the snippets extension doesn't ship them.

## License

[MIT](LICENSE)
