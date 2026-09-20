# 👁️ Overviews Workspace Rules & Architectural Invariants

> **Project**: Overviews (Google AI Overview & Instant Search Sentry)  
> **Framework**: .NET 9.0 WinExe (Native Windows Subsystem)  
> **Author**: Karan Singh Verma

---

## 🏛️ Core Principles & Invariants

### 1. ⚡ Zero Background Daemon Invariant (0 MB Idle Footprint)
- **Summon On Demand**: Overviews executes only when invoked via `Ctrl + Alt + O` or the CLI (`Overviews "<query>"`).
- **Zero Idle Overhead**: No persistent system tray daemons, telemetry hooks, or background polling loops.
- **Instant Clean Exit**: The process launches the target browser/webapp window and terminates immediately in <15ms.

### 2. 🪟 Full-Screen Immersion & Virtual Desktop Isolation
- **Active Workspace Concurrency**: Always summon the window on the operator's current active Virtual Desktop, avoiding Chromium workspace teleportation anomalies.
- **Window Maximization**: Enforce `SW_MAXIMIZE` natively so the window enters full-screen immersion without title bar distraction.

### 3. 🛡️ CLI & Query Parameterization
- **URL Encoding Safety**: When queries are passed via command line, validate and encode URL parameters to prevent command-line argument injection.
- **Browser Profile Isolation**: Use the operator's designated profile without corrupting main browser state.

### 4. 🛣️ Zero Absolute Machine Path Invariant
- **Portable Home Expansion**: Always resolve `%USERPROFILE%` or `Environment.GetFolderPath(...)` dynamically. Never commit machine-specific paths.
