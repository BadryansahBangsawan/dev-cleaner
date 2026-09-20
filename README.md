<div align="center">

# Dev Cleaner

**One-click interactive shell script to deep-clean development caches on macOS and Linux.**  
Frees 50 GB+ of storage by clearing Xcode, Flutter, Android, npm, Gradle, Python, and IDE caches.

<br/>

[![Shell](https://img.shields.io/badge/Shell-bash-4EAA25?style=flat-square&logo=gnubash&logoColor=white)](https://github.com/BadryansahBangsawan/dev-cleaner)
[![macOS](https://img.shields.io/badge/macOS-supported-black?style=flat-square&logo=apple)](https://github.com/BadryansahBangsawan/dev-cleaner)
[![Linux](https://img.shields.io/badge/Linux-supported-FCC624?style=flat-square&logo=linux&logoColor=black)](https://github.com/BadryansahBangsawan/dev-cleaner)
[![Windows](https://img.shields.io/badge/Windows-PowerShell-0078D4?style=flat-square&logo=powershell&logoColor=white)](https://github.com/BadryansahBangsawan/dev-cleaner)

<br/>

</div>

---

## Install

### macOS and Linux

```bash
curl -fsSL https://raw.githubusercontent.com/BadryansahBangsawan/dev-cleaner/main/dev-cleaner.sh | bash
```

Or clone and run manually:

```bash
git clone https://github.com/BadryansahBangsawan/dev-cleaner.git
cd dev-cleaner
bash dev-cleaner.sh
```

### Windows — PowerShell

```powershell
irm https://raw.githubusercontent.com/BadryansahBangsawan/dev-cleaner/main/dev-cleaner.ps1 | iex
```

---

## Features

| Target | What gets cleaned |
|---|---|
| **Xcode** | Derived Data, Archives, Simulators, device symbols |
| **Flutter / FVM** | Build artifacts, .dart_tool, FVM SDK cache, Pub cache |
| **Android** | Gradle caches and build directories |
| **npm / Node** | node_modules, npm / yarn / pnpm cache |
| **Python** | __pycache__, .pyc files, pip cache, virtualenvs |
| **IDEs** | JetBrains, VS Code, Android Studio caches |
| **Claude Code** | Old version binaries left behind by the native installer |
| **System** | macOS DS_Store files, Trash, log files |

- Interactive menu — pick only the targets you want to clean.
- Dry run mode — see what would be deleted before committing.
- Multi-platform — same clean interface on macOS, Linux, and Windows (PowerShell).

---

## Requirements

- **bash 3.2+** (ships on macOS; pre-installed on most Linux distros)
- **zsh** users: run via `bash dev-cleaner.sh`, not `zsh dev-cleaner.sh` — the script uses bash-specific arrays
- **Windows**: PowerShell 5.1 or PowerShell 7+ for `dev-cleaner.ps1`

---

## Notes

– Run with `bash dev-cleaner.sh` — no install, no dependencies beyond bash.
– The script always asks for confirmation before deleting anything.
– Flutter cleanup recurses into nested projects found under your home directory.
– AI CLI cleanup prunes old Claude Code binaries (~/.local/share/claude/versions), keeping only the currently active version.
– Windows support is via the separate dev-cleaner.ps1 script.
– First run on a machine with many projects? Select all targets in dry-run first to preview the total size before committing.
– Prefer cloning the repo and running `bash dev-cleaner.sh` if you want to inspect the script before it runs; the curl | bash one-liner is convenience only.

---

<div align="center">

Made with ♥ for developers drowning in gigabytes of cache.

</div>
