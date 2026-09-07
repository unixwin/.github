# UNIXWIN

Native Unix-style command-line infrastructure for Windows and AI agents.

UNIXWIN builds a Windows-native command stack for workflows that expect Unix commands, Bash-like scripting, pipelines, and agent-friendly automation without requiring WSL.

```text
niubash
├── rubash        Bash-compatible shell engine written in Rust
└── WinuxCmd      Native Windows coreutils layer

oh-my-niu         Themes, plugins, and shell configuration
```

## Start Here

| If you want... | Start with | Role |
| --- | --- | --- |
| A Unix-style shell on Windows | [niubash](https://github.com/unixwin/niubash) | User-facing shell |
| GNU-style commands available today | [WinuxCmd](https://github.com/unixwin/WinuxCmd) | Native coreutils layer; usable standalone |
| A Bash-compatible execution engine | [rubash](https://github.com/unixwin/rubash) | Shell language engine |
| Themes, plugins, and shell customization | [oh-my-niu](https://github.com/unixwin/oh-my-niu) | Configuration ecosystem |

## Why UNIXWIN Exists

AI agents, CI jobs, documentation, issue comments, and developers often produce Unix-style commands such as `grep`, `find`, `xargs`, `sed`, and shell pipelines. On Windows, those workflows often require WSL, Git Bash, or shell-specific workarounds.

UNIXWIN aims to make that layer native on Windows: composable commands, Bash-compatible execution, familiar text workflows, and predictable behavior for both humans and agents.

## Project Stack

### [niubash](https://github.com/unixwin/niubash)

The primary user-facing shell. `niubash` combines `rubash` for Bash-compatible language execution with `WinuxCmd` as its native coreutils layer, then adds the interactive Windows experience: REPL, completion, prompt themes, configuration, history, and Ctrl+C handling.

### [WinuxCmd](https://github.com/unixwin/WinuxCmd)

A lightweight native Windows implementation of GNU-style command tools. It can be used standalone today, and its long-term role in UNIXWIN is to serve as the coreutils layer for `niubash`.

### [rubash](https://github.com/unixwin/rubash)

A Bash-compatible shell engine written in Rust. It provides the parser, executor, builtins, shell language behavior, and script compatibility layer used by `niubash`.

### [oh-my-niu](https://github.com/unixwin/oh-my-niu)

The planned configuration ecosystem for `niubash`: themes, plugins, prompt customization, and shell setup conventions.

## Current Focus

- Make `niubash` the main entry point for the UNIXWIN command-line experience.
- Keep `WinuxCmd` useful standalone while hardening it as the native coreutils layer.
- Improve Bash compatibility in `rubash` through real compatibility tests.
- Build a Windows command-line stack that works well for AI agents, local automation, and developer workflows.

## 中文说明

UNIXWIN 是面向 Windows 和 AI agent 的原生命令行基础设施。

我们的目标不是把 Windows 变成 Linux，而是在 Windows 上提供可组合、可脚本化、agent 友好的 Unix-style 命令体验：`niubash` 作为用户入口，`rubash` 提供 Bash 兼容执行引擎，`WinuxCmd` 提供原生 Windows coreutils 层。
