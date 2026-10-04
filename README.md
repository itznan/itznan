## Hi, I'm Itznan 👋

<!--
**itznan/itznan** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->

Computer Science & Engineering (AI) Student from Rajkot, Gujarat  
Systems & Native Software Engineer | Rajkot, India  
Building low-level hardware utilities, native Windows software, and developer tooling with AI-assisted architectures.

---

## Some things I've built

**comixapi**  
A high-performance FastAPI REST API & scraper service for manga, manhwa & webtoons. Features a decoupled asynchronous Playwright session daemon, persistent browser state management to seamlessly resolve Cloudflare challenges, dynamic TLS fingerprint impersonation via `curl_cffi`, CORS/CORP media proxies, and automated format compilers (`.cbz` with `ComicInfo.xml`, `.epub`, `.pdf`).  
Explore on [GitHub](https://github.com/itznan/comixapi)

**fanrgbmpgb550**  
A zero-overhead, native Rust CLI lighting and motherboard controller for MSI MPG B550 Gaming Plus motherboards and Gigabyte RTX 3060 Ti GPUs. Bypasses bloated vendor software through direct USB HID (`0x52`) feature reports and NVAPI I2C probes, strictly writes to volatile RAM to prevent EEPROM flash wear, and features a real-time WASAPI sub-bass audio visualizer.  
Explore on [GitHub](https://github.com/itznan/fanrgbmpgb550)

**pankha**  
A unified hardware fan control and telemetry application designed specifically for 64-bit Windows. Consolidates disparate cooling channels (motherboard Super I/O, CPU AIO pumps, and GPU fans) into a centralized, low-latency control interface with automated duty-cycle calibration, dynamic custom curves, and failsafe thermal cutoffs.  
Explore on [GitHub](https://github.com/itznan/pankha)

**wincallnotifier**  
A lightweight, 100% offline native Windows desktop and system tray application written entirely in Rust. Monitors incoming Android 15 phone call states via USB and ADB shell transports without requiring any APK installed on the phone, delivering native Windows toast notifications with zero cloud reliance.  
Explore on [GitHub](https://github.com/itznan/wincallnotifier)

**locsim**  
A universal, cross-platform location simulator written in 100% safe Rust (published on [crates.io](https://crates.io/crates/locsim)). Seamlessly simulates device coordinates, altitude, accuracy, speed, and heading across Windows, Linux, Android emulators, iOS simulators, and headless browsers with a single unified CLI.  
Explore on [GitHub](https://github.com/itznan/locsim)

---

## Interests

- Low-level systems programming & native Windows internals (Win32, WASAPI, Super I/O)
- Hardware telemetry, kernel driver interop & custom fan/RGB controllers
- Cross-platform developer tooling, simulation & mock environments
- Network protocol inspection, reverse engineering & high-throughput scrapers
- AI-assisted engineering & autonomous agent workflows

---

## Tech Stack

- **Languages:** Rust, Go, Python, C#, TypeScript, JavaScript, SQL
- **Systems & Hardware:** Win32 API, WASAPI, Android ADB, Super I/O & SMBus, HID / Hardware I/O
- **Frameworks & Web:** FastAPI, Node.js, React, Tailwind CSS, REST APIs
- **Tooling & Workflows:** Git, PowerShell, Docker, AI agent orchestration & prompt architecture

---

## Outside of Code

- Anime, manga & light novel enthusiast 📖
- PC hardware tinkering, custom loop tuning & silent builds 🖥️
- Competitive gaming (Valorant, Minecraft mechanics) 🎮
- Exploring autonomous agentic architectures ⚡

---

<details>
<summary><h2>Some useful open-source tools I've been using (on Windows / Dev)</h2></summary>

- **Windows Terminal**, GPU-accelerated terminal emulator with custom color palettes, split panes, and seamless PowerShell/WSL integration. [Download](https://github.com/microsoft/terminal)
- **Glow**, a terminal-based markdown reader designed for quick documentation review on the fly. [Repo](https://github.com/charmbracelet/glow)
- **LibreHardwareMonitor**, open-source monitor providing real-time CPU/GPU temperature, fan speeds, and voltage sensors via clean WMI / .NET interfaces. [Repo](https://github.com/LibreHardwareMonitor/LibreHardwareMonitor)
- **Scrcpy**, ultra-low latency Android screen mirroring and control over USB/ADB with zero bloat. [Repo](https://github.com/Genymobile/scrcpy)
- **Sysinternals Suite**, the industry-standard Windows kernel & process diagnostics toolkit (Process Explorer, ProcMon, TCPView). [Download](https://learn.microsoft.com/en-us/sysinternals/)

And for coding agents & AI workflows...
- **Plannotator**, clean visual renderer and annotator for proposed agent plans directly in your browser. [Link to install](https://plannotator.ai/)
- **code-review-graph**, AST-driven repository graphing and context generation for agent sessions to lower token usage. [Repo](https://github.com/tirth8205/code-review-graph)
- **Antigravity CLI (AGY)**, agentic workflow companion for deep multi-agent coordination, subagents, and rapid prototyping.
</details>

---

<details>
<summary><h2>Some of my custom PowerShell / Git aliases</h2></summary>

```powershell
# Git shortcuts
function gc ($msg) { git commit -m "$msg" }
Set-Alias gdn "git diff --name-only"
Set-Alias ga "git add"
Set-Alias gs "git status -sb"
Set-Alias glog "git log --oneline --graph --decorate"

# Git add multiple files interactively from input/pipe
function ga-mul {
    $files = $input | Where-Object { $_ -ne "" }
    if ($files) { git add $files }
}

# Local dev & port inspection (Windows)
function ports {
    Get-NetTCPConnection -State Listen | Select-Object LocalAddress, LocalPort, OwningProcess | Sort-Object LocalPort
}
function killport ($port) {
    $proc = (Get-NetTCPConnection -LocalPort $port -ErrorAction SilentlyContinue).OwningProcess
    if ($proc) { Stop-Process -Id $proc -Force; Write-Host "Killed PID $proc on port $port" -ForegroundColor Green }
    else { Write-Host "No process listening on port $port" -ForegroundColor Yellow }
}

# Android / ADB helpers
function adb-devices { adb devices -l }
function adb-reboot-bl { adb reboot bootloader }

# Navigation
Set-Alias .. "cd .."
Set-Alias ... "cd ../.."
```

*(For Bash / WSL users)*:
```bash
alias gdn='git diff --name-only'
alias ga='git add'
alias ports='lsof -i -P | grep LISTEN'
alias ..='cd ..'
alias ...='cd ../..'
gc() { git commit -m "$*"; }
```
</details>

---

## Contribution-eating snake

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/itznan/itznan/output/github-snake-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/itznan/itznan/output/github-snake.svg">
  <img alt="github contribution grid snake animation" src="https://raw.githubusercontent.com/itznan/itznan/output/github-snake.svg">
</picture>

---

<p align="center">
  <a href="https://itznan.tech/">Website</a> •
  <a href="https://github.com/itznan">GitHub</a> •
  <a href="mailto:vishalxnan@gmail.com">Email</a> •
  <span>Discord: @itznan</span>
</p>
