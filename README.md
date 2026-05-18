# ZeroCPP — Zero-Configuration C++ Project Manager

ZeroCPP is a zero-configuration C++ project manager designed to simplify modern C++ development. It combines instant project scaffolding with seamless dependency management, powered by vcpkg and modern CMake.

With ZeroCPP, you can create clean C++20 projects, add libraries, and build your code in seconds — without dealing with complex setup or manual configuration.

```bash
zerocpp init my_app     # scaffolds a project
zerocpp add raylib      # links raylib to your project
zerocpp build           # builds the project
zerocpp run             # runs the executable
```

As simple as that.

ZeroCPP handles vcpkg setup, integration, and linking behind the scenes while still generating clean, portable CMake projects — so you stay in control without the usual friction.

No more linker errors.  
No more environment issues.  

Just focus on writing code.

> Because setting up C++ projects shouldn’t hurt this much.

---

# Features

- Instant C++20 project scaffolding
- Automatic dependency management with vcpkg
- Clean and portable CMake generation
- One-command build and run workflow
- Regex-powered auto-linker for `target_link_libraries`
- Blazingly fast global binary caching
- Minimal setup with sane defaults
- Cross-platform support (Windows, Linux, macOS)

---

# Quick Start

## Initialize a Project

```bash
zerocpp init my_app
cd my_app
```

## Add Dependencies

```bash
zerocpp add fmt
zerocpp add raylib
```

## Build & Run

```bash
zerocpp build
zerocpp run
```

---

# Installation

## Windows

Download the latest precompiled `zerocpp.exe` release and add it to your system `PATH`.

---

## Linux & macOS (Build from Source)

Compile ZeroCPP into a native executable using PyInstaller.

### Install PyInstaller

```bash
pip install pyinstaller
```

### Build the Binary

```bash
# Navigate to the repository root
pyinstaller --onefile zerocpp.py
```

### Move Binary to PATH

```bash
# Move the generated binary from the dist folder
sudo mv dist/zerocpp /usr/local/bin/
```

---

# Requirements

- Git >= 2.19.0
- CMake >= 3.21
- A C++ compiler
  - GCC
  - Clang
  - MSVC
- vcpkg  
  (ZeroCPP can automatically install and configure it)

---

# Philosophy

ZeroCPP exists because modern C++ development still requires too much boilerplate, configuration, and dependency pain.

The goal is simple:

- Create projects instantly
- Add dependencies effortlessly
- Keep generated projects clean and portable
- Let developers focus on writing code instead of fighting tooling

---

# Example Workflow

```bash
# Create project
zerocpp init game_engine

# Enter project
cd game_engine

# Install dependencies
zerocpp add sdl2
zerocpp add glm

# Build project
zerocpp build

# Run executable
zerocpp run
```

---

# Why ZeroCPP?

C++ is powerful.  
Its tooling shouldn't feel ancient.

ZeroCPP brings a modern developer experience inspired by tools like:

- Cargo (Rust)
- npm (JavaScript)
- pip (Python)

But built specifically for modern C++.

---

# Roadmap

- [ ] Package version locking
- [ ] Project templates
- [ ] Remote package registry
- [ ] Build profiles
- [ ] Testing integration
- [ ] CI/CD helpers
- [ ] IDE integrations

---

# License

MIT License

---

# Contributing

Pull requests, ideas, and feedback are always welcome.

If C++ tooling has ever frustrated you, this project is for you.
