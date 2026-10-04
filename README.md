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
Building low-level hardware utilities, Linux systems software, and developer tooling with AI-assisted architectures.

🔭 Currently working on: **Linux systems, low-level tooling & kernel utilities**

---

## Some things I've built

**comixapi**  
A high-performance FastAPI REST API & scraper service for manga, manhwa & webtoons. Features a decoupled asynchronous Playwright session daemon, persistent browser state management to seamlessly resolve Cloudflare challenges, dynamic TLS fingerprint impersonation via `curl_cffi`, CORS/CORP media proxies, and automated format compilers (`.cbz` with `ComicInfo.xml`, `.epub`, `.pdf`).  
Explore on [GitHub](https://github.com/itznan/comixapi)

**fanrgbmpgb550**  
A zero-overhead, native Rust CLI lighting and motherboard controller for MSI MPG B550 Gaming Plus motherboards and Gigabyte RTX 3060 Ti GPUs. Bypasses bloated vendor software through direct USB HID (`0x52`) feature reports and NVAPI I2C probes, strictly writes to volatile RAM to prevent EEPROM flash wear, and features a real-time WASAPI sub-bass audio visualizer.  
Explore on [GitHub](https://github.com/itznan/fanrgbmpgb550)

**pankha**  
A unified hardware fan control and telemetry application designed specifically for 64-bit systems. Consolidates disparate cooling channels (motherboard Super I/O, CPU AIO pumps, and GPU fans) into a centralized, low-latency control interface with automated duty-cycle calibration, dynamic custom curves, and failsafe thermal cutoffs.  
Explore on [GitHub](https://github.com/itznan/pankha)

**wincallnotifier**  
A lightweight, 100% offline desktop and system tray application written entirely in Rust. Monitors incoming Android 15 phone call states via USB and ADB shell transports without requiring any APK installed on the phone, delivering native toast notifications with zero cloud reliance.  
Explore on [GitHub](https://github.com/itznan/wincallnotifier)

**locsim**  
A universal, cross-platform location simulator written in 100% safe Rust (published on [crates.io](https://crates.io/crates/locsim)). Seamlessly simulates device coordinates, altitude, accuracy, speed, and heading across Linux, Windows, Android emulators, iOS simulators, and headless browsers with a single unified CLI.  
Explore on [GitHub](https://github.com/itznan/locsim)

---

## Interests

- High-performance systems and software
- Everything I don't know

---

## Tech Stack

- **Languages:** Rust, Go, Python, C/C++, C#, TypeScript, JavaScript, SQL, Bash
- **Systems & Hardware:** Linux (POSIX, sysfs, systemd), Win32 API, WASAPI, Android ADB, Super I/O & SMBus, HID / Hardware I/O
- **Frameworks & Web:** FastAPI, Node.js, React, Tailwind CSS, REST APIs
- **Tooling & Workflows:** Git, Linux/Bash, Docker, PowerShell, AI agent orchestration & prompt architecture

---


<details>
<summary><h2>Some useful open-source tools I've been using (on Linux)</h2></summary>

- **btop**, a gorgeous, responsive resource monitor for Linux with detailed CPU, memory, disks, and network stats. [Repo](https://github.com/aristocratos/btop)
- **tmux**, terminal multiplexer for managing persistent workspace sessions, split panes, and detached background processes. [Repo](https://github.com/tmux/tmux)
- **Glow**, a very simple renderer for markdown files inside the terminal. [Repo](https://github.com/charmbracelet/glow)
- **Fastfetch**, blazingly fast system information fetcher written in C for Linux/POSIX systems. [Repo](https://github.com/fastfetch-cli/fastfetch)
- **Scrcpy**, ultra-low latency Android screen mirroring and control over USB/ADB with zero bloat. [Repo](https://github.com/Genymobile/scrcpy)
- **strace & perf**, indispensable diagnostic and profiling utilities for low-level systems and system call tracing on Linux.

And for coding agents & AI workflows...
- **Plannotator**, clean visual renderer and annotator for proposed agent plans directly in your browser. [Link to install](https://plannotator.ai/)
- **code-review-graph**, AST-driven repository graphing and context generation for agent sessions to lower token usage. [Repo](https://github.com/tirth8205/code-review-graph)
- **Antigravity CLI (AGY)**, agentic workflow companion for deep multi-agent coordination, subagents, and rapid prototyping.
</details>

---

<details>
<summary><h2>Some of my custom bash aliases (on Linux)</h2></summary>

```bash
# git stuff
alias gdn='git diff --name-only'
alias ga='git add'
alias gs='git status -sb'
alias glog='git log --oneline --graph --decorate'

# git add multiple files separated by line breaks (press enter after ga-mul, then paste all, and press enter again)
ga-mul() {
  if [ -t 0 ]; then
    local files=("$@")
    local line
    while IFS= read -r line; do
      [[ -z "$line" ]] && break
      files+=("$line")
    done
    git add "${files[@]}"
  else
    xargs git add
  fi
}

# type a commit message after 'gc ' and it will wrap in quotes and send the commit
gc() {
  git commit -m "$*"
}

# local dev & network inspection
alias ports='lsof -i -P -n | grep LISTEN'
alias activate='source venv/bin/activate'
alias myip='curl -s ifconfig.me'

# general & navigation
alias ..='cd ..'
alias ...='cd ../..'
alias ~='cd ~'
alias ll='ls -lah --color=auto'
alias adb-devices='adb devices -l'
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
