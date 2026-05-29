<p align="center">
  <img src="https://raw.githubusercontent.com/Kern-Unikernel/.github/main/profile/kern-logo.png" width="600" alt="kern logo">
</p>

<h3 align="center">Build, run and distribute applications as unikernels</h3>

<p align="center">
  <a href="https://github.com/Kern-Unikernel/Kern-Unikernel">
    <img src="https://img.shields.io/badge/CLI-kern-white?style=flat-square" alt="kern CLI">
  </a>
  <img src="https://img.shields.io/badge/status-active-brightgreen?style=flat-square" alt="status">
  <img src="https://img.shields.io/badge/license-MIT-blue?style=flat-square" alt="license">
</p>

---

kern eliminates the operating system from the application lifecycle. Instead of packaging your app inside a container with a full Linux OS, kern compiles it directly into a unikernel — a single binary that contains exactly what your app needs and nothing else.

## Why kern?

| | Docker | kern |
|---|---|---|
| Boot time | 800ms - 2s | 5 - 12ms |
| Image size | 150MB - 800MB | 15 - 45MB |
| Memory usage | 50 - 150MB | 8 - 40MB |
| Attack surface | ~400 syscalls | ~50 syscalls |

## Get started

```bash
git clone https://github.com/Kern-Unikernel/Kern-Unikernel.git
cd Kern-Unikernel
go build -o kern ./cmd/
```

```bash
kern init      # detect runtime and create Kernfile
kern build     # compile as unikernel
kern run       # launch on QEMU/KVM
```

## Supported runtimes

| Runtime | Min memory | Boot time |
|---|---|---|
| Go 1.22 | 64Mi | ~8ms |
| Node.js 21 | 512Mi | ~10ms |

## Repositories

| Repo | Description |
|---|---|
| [Kern-Unikernel](https://github.com/Kern-Unikernel/Kern-Unikernel) | Main CLI tool |
