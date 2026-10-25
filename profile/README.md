<div align="center">

<img src="https://github.com/unixwin.png?size=200" width="96" alt="unixwin logo" />

# unixwin

### Real Bash and Unix commands — native on Windows

**No WSL · No MSYS · No POSIX emulation layer**

<p>
  <a href="https://unixwin.dev"><img src="https://img.shields.io/badge/website-unixwin.dev-2ea44f" alt="Website: unixwin.dev" /></a>
  <a href="https://github.com/unixwin/niubash/releases"><img src="https://img.shields.io/github/v/release/unixwin/niubash?label=niubash%20release" alt="Latest niubash release" /></a>
  <a href="https://github.com/unixwin/WinuxCmd/releases"><img src="https://img.shields.io/github/v/release/unixwin/WinuxCmd?label=WinuxCmd%20release" alt="Latest WinuxCmd release" /></a>
  <a href="https://github.com/orgs/unixwin/followers"><img src="https://img.shields.io/github/followers/unixwin" alt="GitHub followers" /></a>
</p>

<p>
  <a href="https://unixwin.dev"><strong>🌐 Website</strong></a> ·
  <a href="https://github.com/unixwin/niubash/releases"><strong>📥 Downloads</strong></a> ·
  <a href="https://unixwin.dev"><strong>📚 Docs</strong></a> ·
  <a href="https://github.com/unixwin/.github/blob/main/CONTRIBUTING.md"><strong>🤝 Contributing</strong></a>
</p>

</div>

**unixwin** builds a Windows-native Unix command stack for developers and AI agents: a real Bash shell, the engine behind it, the core Unix commands, a Git distribution, a package manager, and a plugin framework — composable Unix workflows that run natively on Windows, with no WSL and no emulation layer in between.

## The family

```mermaid
flowchart TD
    U["You — or your AI agent"] --> NB["<b>niubash</b><br/>the shell"]
    NB --> RB["<b>rubash</b><br/>Bash 5.3 engine · Rust"]
    NB --> WC["<b>WinuxCmd</b><br/>native Unix commands"]
    NB --> NG["<b>niu-git</b><br/>Git without MSYS"]
    NB --> OMN["<b>oh-my-niu</b><br/>plugins &amp; themes"]
    WC --> WPM["<b>wpm</b><br/>package manager"]
```

<table>
  <tr>
    <th align="left" width="190">Project</th>
    <th align="left">What it is</th>
    <th align="left" width="170">Get it</th>
  </tr>
  <tr>
    <td>
      🐂 <a href="https://github.com/unixwin/niubash"><strong>niubash</strong></a><br/>
      <img src="https://img.shields.io/github/stars/unixwin/niubash" alt="niubash stars" />
    </td>
    <td>
      <strong>The shell.</strong> Real Bash for humans and AI agents — the interactive experience (REPL, completion, prompt, history) on top of the family stack.<br/>
      <sub>Rust · native on Windows, Linux &amp; macOS · no WSL, no MSYS</sub>
    </td>
    <td>
      <a href="https://github.com/unixwin/niubash/releases">Releases</a> ·
      <a href="https://unixwin.dev">Docs</a>
    </td>
  </tr>
  <tr>
    <td>
      🧰 <a href="https://github.com/unixwin/WinuxCmd"><strong>WinuxCmd</strong></a><br/>
      <img src="https://img.shields.io/github/stars/unixwin/WinuxCmd" alt="WinuxCmd stars" />
    </td>
    <td>
      <strong>The commands.</strong> 176 Unix commands in one ~3 MB native Windows executable — real Windows paths, no path-translation pain. Usable standalone today; also serves as niubash's coreutils layer.<br/>
      <sub>C++ · Windows x64 &amp; ARM64 · v1.0.0 stable is out</sub>
    </td>
    <td>
      <a href="https://github.com/unixwin/WinuxCmd/releases">Releases</a> ·
      <a href="https://unixwin.dev">Docs</a>
    </td>
  </tr>
  <tr>
    <td>
      🦀 <a href="https://github.com/unixwin/rubash"><strong>rubash</strong></a><br/>
      <img src="https://img.shields.io/github/stars/unixwin/rubash" alt="rubash stars" />
    </td>
    <td>
      <strong>The engine.</strong> A from-scratch, embeddable GNU Bash 5.3-compatible shell engine in Rust — parser, executor, builtins and all. Compatibility is measured, not claimed: 83/83 against GNU Bash's own upstream test-suite corpus.<br/>
      <sub>Rust · embeddable library · native on Windows, Linux &amp; macOS</sub>
    </td>
    <td>
      <a href="https://github.com/unixwin/rubash">Repository</a> ·
      <a href="https://unixwin.dev">Docs</a>
    </td>
  </tr>
  <tr>
    <td>
      🔀 <a href="https://github.com/unixwin/niu-git"><strong>niu-git</strong></a><br/>
      <img src="https://img.shields.io/github/stars/unixwin/niu-git" alt="niu-git stars" />
    </td>
    <td>
      <strong>The Git.</strong> A native Windows Git distribution without MSYS — built with MSVC, no bash/perl/MSYS2 bundled. The fast-starting Git that niubash ships; its shell-script parts run on niubash itself.<br/>
      <sub>MSVC + CMake · Windows</sub>
    </td>
    <td>
      <a href="https://github.com/unixwin/niu-git">Repository</a>
    </td>
  </tr>
  <tr>
    <td>
      🎨 <a href="https://github.com/unixwin/oh-my-niu"><strong>oh-my-niu</strong></a><br/>
      <img src="https://img.shields.io/github/stars/unixwin/oh-my-niu" alt="oh-my-niu stars" />
    </td>
    <td>
      <strong>The customization.</strong> The official Oh My-style plugin framework and bundled plugin distribution for niubash — plugins, themes, and prompt customization.<br/>
      <sub>Python · plugins are directories, themes are plugins</sub>
    </td>
    <td>
      <a href="https://github.com/unixwin/oh-my-niu">Repository</a>
    </td>
  </tr>
  <tr>
    <td>
      🌐 <a href="https://github.com/unixwin/unixwin.dev"><strong>unixwin.dev</strong></a><br/>
      <img src="https://img.shields.io/github/stars/unixwin/unixwin.dev" alt="unixwin.dev stars" />
    </td>
    <td>
      <strong>The website.</strong> Docs, downloads, and live changelogs for the whole family — the source of <a href="https://unixwin.dev">unixwin.dev</a>.<br/>
      <sub>Astro · day/night themes</sub>
    </td>
    <td>
      <a href="https://unixwin.dev">Visit site</a> ·
      <a href="https://github.com/unixwin/unixwin.dev">Repository</a>
    </td>
  </tr>
</table>

## Start here

| If you want… | Start with |
| --- | --- |
| A Unix-style shell on Windows | [niubash](https://github.com/unixwin/niubash) — the user-facing shell |
| Unix commands on Windows, today | [WinuxCmd](https://github.com/unixwin/WinuxCmd) — standalone, one small executable |
| A Bash-compatible engine to embed | [rubash](https://github.com/unixwin/rubash) — the shell language engine |
| Git on Windows without MSYS | [niu-git](https://github.com/unixwin/niu-git) — niubash's Git companion |
| Themes, plugins, prompt customization | [oh-my-niu](https://github.com/unixwin/oh-my-niu) — the configuration ecosystem |
| Docs, downloads, changelogs | [unixwin.dev](https://unixwin.dev) — the family portal |

## Why unixwin exists

AI agents, CI jobs, documentation, and developers constantly produce Unix-style commands — `grep`, `find`, `xargs`, `sed`, shell pipelines. On Windows those workflows usually detour through WSL, Git Bash, or per-shell workarounds, and the emulation layer leaks quirks into every script.

unixwin makes that layer native instead: real Bash semantics from a from-scratch engine, real Unix commands built for Windows paths, and predictable behavior for both humans and agents — the shell your fingers already know, and the one your AI agent actually speaks.

## Get involved

- 📖 Read the [contributing guide](https://github.com/unixwin/.github/blob/main/CONTRIBUTING.md) — it covers how work is organized across the family.
- 🐛 Found a bug or a compatibility gap? File it in the repo it belongs to — compatibility reports with a GNU Bash comparison are gold.
- 💬 Questions and ideas are welcome in the relevant repo's issues.

<details>
<summary><strong>Supporting repositories</strong> — the WPM ecosystem and more</summary>

<br/>

| Repository | Role |
| --- | --- |
| [wpm-source](https://github.com/unixwin/wpm-source) | Curated WPM index for standalone Windows command-line binaries |
| [wpm-artifacts](https://github.com/unixwin/wpm-artifacts) | Self-hosted portable binary artifacts for WPM (mirrors + CI builds, sha256 manifests) |
| [wpm-gui](https://github.com/unixwin/wpm-gui) | GUI front-end for the wpm package manager |
| [winuxcmd-i18n](https://github.com/unixwin/winuxcmd-i18n) | Optional WinuxCmd language catalogs |
| [winuxsh-profiles](https://github.com/unixwin/winuxsh-profiles) | Example configuration profiles and WPM package presets |
| [codex](https://github.com/unixwin/codex) | Lightweight coding agent that runs in your terminal (fork) |

</details>

## 中文简介

UNIXWIN 是面向 Windows 与 AI agent 的原生命令行基础设施：`niubash` 作为用户入口（真实 Bash、原生运行），`rubash` 提供从零实现的 GNU Bash 5.3 兼容引擎，`WinuxCmd` 提供 176 个原生 Unix 命令，`niu-git` 提供无 MSYS 的 Git 发行，`oh-my-niu` 提供插件与主题框架。目标不是把 Windows 变成 Linux，而是在 Windows 上原生提供可组合、可脚本化、agent 友好的 Unix 命令体验——不用 WSL，不用仿真层。官网：[unixwin.dev](https://unixwin.dev)。

<div align="center">
  <sub>unixwin — real Unix tooling, native on Windows · <a href="https://unixwin.dev">unixwin.dev</a></sub>
</div>
