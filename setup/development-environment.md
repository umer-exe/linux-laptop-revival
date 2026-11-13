# Development environment plan

**Status: planned, not installed.**

## Priorities
1. Responsive Xfce desktop and Firefox for everyday work.
2. LibreOffice for offline writing, spreadsheets and presentations.
3. Git and VS Code for modest coding sessions.
4. Codex CLI for agent-assisted coding; local commands and tests still use laptop resources.
5. Docker **Engine** and Compose for small Linux containers, not Docker Desktop.

## Constraints
- 8 GB physical RAM, no upgrade planned.
- AMD A8-6410 is an older CPU; avoid concurrent heavy builds and services.
- Chrome/Firefox tabs and multiple profile sessions may consume more RAM than the desktop itself.
- Docker images/volumes consume limited 256 GB SSD space.

## After installation
- Update Mint and inspect Driver Manager.
- Install and configure chosen browser and editor.
- Set up Git identity and authentication.
- Install Codex CLI using its current official Linux instructions.
- Install Docker Engine and Compose using verified distro-compatible instructions.
- Measure idle memory and actual workflows before changing swap/zram settings.
- Keep a record of installed versions and any performance tweaks.
