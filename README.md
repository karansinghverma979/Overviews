# 👁️ Overviews — Google AI Overview & Instant Search Sentry

<p align="center">
  <img src="https://img.shields.io/badge/PLATFORM-WINDOWS%2011-0078D6?style=for-the-badge&logo=windows&logoColor=white" alt="Windows 11"/>
  <img src="https://img.shields.io/badge/RUNTIME-.NET%209%20WinExe-512BD4?style=for-the-badge&logo=dotnet&logoColor=white" alt=".NET 9"/>
  <img src="https://img.shields.io/badge/IDLE%20RAM-0%20MB-brightgreen?style=for-the-badge" alt="0 MB Idle RAM"/>
  <img src="https://img.shields.io/badge/LAUNCH-%3C15ms-orange?style=for-the-badge" alt="<15ms Cold Launch"/>
  <img src="https://img.shields.io/badge/LICENSE-MIT-blue?style=for-the-badge" alt="MIT License"/>
</p>

> **Instant full-screen Google AI Overview summoner & distraction-free desktop sentry for Windows 11.**  
> Zero persistent background daemons. Zero idle RAM. Global native `Ctrl + Alt + O` hotkey.

---

## ⚡ 5-Second System Flowcard

```text
┌────────────────┐      ┌─────────────────────────┐      ┌─────────────────────────┐
│  Ctrl+Alt+O    │ ──►  │ Native Win32 Launcher   │ ──►  │ Enforce SW_MAXIMIZE     │
│  Global Hotkey │      │ Sub-15ms Process Exec   │      │ Standalone AI Overview  │
└────────────────┘      └─────────────────────────┘      └─────────────────────────┘
                                                                     │
                                                                     ▼
                                                         Tap Ctrl+W / Alt+F4 to Vanish
                                                         System returns to 0 MB RAM
```

---

## 🏛️ System Philosophy

**Overviews** eliminates cognitive friction when querying knowledge during deep focus work. Instead of opening a full browser window with dozens of distracting tabs, toolbars, and bookmarks, pressing **`Ctrl + Alt + O`** instantly summons a clean, maximized, standalone Google AI Overview window.

- **Zero-Daemon Invariant**: Strictly **0 MB idle RAM** and **0% idle CPU**. No persistent background processes or tray watchers.
- **Full-Screen Immersion**: Natively enforced full-screen maximized window (`SW_MAXIMIZE`) for instant focus.
- **Current Desktop Isolation**: Bypasses Chromium workspace teleportation bugs; always opens on your active virtual desktop.
- **Single Keystroke Dismissal**: When done reading, tap `Ctrl + W` or `Alt + F4` to close and return instantly to your code.

---

## ⚡ Controls & Usage

| Trigger | Context | Behavior |
| :--- | :--- | :--- |
| **`Ctrl + Alt + O`** | Global (Anywhere) | Summons the maximized Google AI Overview window natively with 0 background RAM. |
| **`Overviews`** | CLI / Terminal | Launches the maximized Google AI Overview home window. |
| **`Overviews "<query>"`** | CLI / Terminal | Directly opens the Google AI Overview for `<query>` in maximized webapp mode. |

---

## 🚀 30-Second Quickstart

### Option A: 1-Line Universal PowerShell Installer
Execute the universal setup script directly in your terminal (compatible with **Windows PowerShell 5.1 and PowerShell 7+**):

```powershell
irm https://raw.githubusercontent.com/karansinghverma979/Overviews/main/Overviews_SelfContained_Setup.ps1 | iex
```

### Option B: Local Developer Compilation
```powershell
git clone https://github.com/karansinghverma979/Overviews.git
cd Overviews
.\Install-Overviews.ps1
```
* Compiles `Overviews.exe` framework-dependent binary directly to `~/.local/bin/Overviews.exe`.
* Registers the native Windows Explorer shortcut (`Ctrl + Alt + O`) in the Start Menu.

---

## 🧹 Complete Uninstallation & Vanish

To completely remove Overviews from your machine (0 background services, 0 residue):
```powershell
powershell -ExecutionPolicy Bypass -File .\Overviews_SelfContained_Setup.ps1 -Uninstall
```

---

## 🛡️ Security & Governance

- **Vulnerability Disclosures**: Please see our [Security Policy](SECURITY.md) to report vulnerabilities privately.
- **Contributing**: Please review [PULL_REQUEST_TEMPLATE.md](.github/PULL_REQUEST_TEMPLATE.md) before submitting changes.
- **License**: Distributed under the [MIT License](LICENSE).
