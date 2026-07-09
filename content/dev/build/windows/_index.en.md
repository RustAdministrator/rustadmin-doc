---
title: Windows
weight: 20
description: "Build RustDesk on Windows with MSVC, Rust, vcpkg, Sciter, and LLVM. This guide covers the required toolchain setup before compiling the desktop app from source."
keywords: ["build rustdesk windows", "rustdesk windows build", "rustdesk vcpkg windows", "rustdesk sciter dll", "rustdesk llvm libclang"]
---

Use this guide to build RustDesk on Windows by preparing the MSVC toolchain, Rust, `vcpkg`, Sciter, and LLVM first.

{{% notice note %}}
The command line commands here must be run in Git Bash not command prompt or you will get syntax errors.
{{% /notice %}}

## What do you need before building on Windows?

Building RustDesk on Windows requires a Visual Studio C++ toolchain, Rust, `vcpkg`, `sciter.dll`, and LLVM with `LIBCLANG_PATH` configured. Run the shell commands from Git Bash so the examples and environment-variable syntax work as written.

## Windows build checklist

- Install Visual Studio with the C++ workload.
- Install Rust through `rustup-init.exe`.
- Clone and bootstrap `vcpkg`, then set `VCPKG_ROOT`.
- Download `sciter.dll` for the desktop UI.
- Install LLVM and set `LIBCLANG_PATH` to its `bin` directory.
- Clone RustDesk and run the default build steps in Git Bash.

## Dependencies

### C++ build environment

Download [MSVC](https://visualstudio.microsoft.com/) and install.
Select `Windows` as Developer machine OS and check `C++`, then download Visual Studio Community version and install. The installation may take a while.

### Rust develop environment

Download [rustup-init.exe](https://static.rust-lang.org/rustup/dist/x86_64-pc-windows-msvc/rustup-init.exe) and run it as administrator to install `rust`.

### vcpkg

Go to the folder you want to clone vcpkg and use [Git Bash](https://git-scm.com/download/win) to run the following commands, download `vcpkg`, install 64-bit version of `libvpx`, `libyuv` and `opus`.
If you don't have `Git` installed, get `Git` [here](https://git-scm.com/download/win).

```sh
git clone https://github.com/microsoft/vcpkg
vcpkg/bootstrap-vcpkg.bat
export VCPKG_ROOT=$PWD/vcpkg
vcpkg/vcpkg install libvpx:x64-windows-static libyuv:x64-windows-static opus:x64-windows-static aom:x64-windows-static
```

Add System environment variable `VCPKG_ROOT`=`<path>\vcpkg`. The `<path>` should be the location you choose above to clone `vcpkg`.

![](/docs/en/dev/build/windows/images/env.png)

### Sciter

Desktop versions use [Sciter](https://sciter.com/) for GUI, please download [sciter.dll](https://raw.githubusercontent.com/c-smile/sciter-sdk/master/bin.win/x64/sciter.dll).

### LLVM

`rust-bindgen` depends on `clang`, download [LLVM](https://github.com/llvm/llvm-project/releases) and install, add System environment variable `LIBCLANG_PATH`=`<llvm_install_dir>/bin`.

You can download version 15.0.2 of the LLVM binaries here: [64 bit](https://github.com/llvm/llvm-project/releases/download/llvmorg-15.0.2/LLVM-15.0.2-win64.exe) / [32 bit](https://github.com/llvm/llvm-project/releases/download/llvmorg-15.0.2/LLVM-15.0.2-win32.exe).

## Build

### Default

```sh
git clone --recurse-submodules https://github.com/rustdesk/rustdesk
cd rustdesk
mkdir -p target/debug
wget https://raw.githubusercontent.com/c-smile/sciter-sdk/master/bin.win/x64/sciter.dll
mv sciter.dll target/debug
cargo run
```

## Runtime capture notes for developers

Windows capture and input code must account for the active desktop, not only the
process elevation level. The normal interactive desktop is usually
`WinSta0\Default`; logon, lock-screen password entry, and UAC secure prompts use
a different secure input desktop such as `WinSta0\Winlogon`.

For the normal unlocked user desktop, RustAdmin should prefer capture backends in
this order:

```text
Windows Graphics Capture -> WinMag -> DXGI Desktop Duplication -> GDI
```

This priority is not valid unchanged for lock screen, logon, or UAC secure
desktop capture. On secure desktops:

- Windows Graphics Capture is not a logon-screen capture solution.
- WinMag is a normal-desktop fallback, not a reliable secure-desktop backend.
- DXGI Desktop Duplication can lose access during desktop transitions and must
  recreate its capture backend/pipeline after lock, unlock, display, session, or
  desktop changes.
- GDI is the practical last fallback to try from an installed service or helper
  that has access to the current input desktop.

Portable elevation is not the same thing as installed service mode. An elevated
portable GUI still runs with the user's token and must not be treated as
equivalent to `LocalSystem`. For unattended access and lock/logon support, use
installed service mode and make sure capture and input injection are recreated
for the current input desktop after each desktop transition.

Here, a helper means a RustAdmin-owned companion process launched in a specific
Windows session or privilege context, for example a user-session capture helper
for WGC or a portable helper for elevated portable work. A helper is not
automatically equivalent to Administrator, `LocalSystem`, or installed service
mode.

For deeper implementation notes, see
`rustdesk-client/docs/WINDOWS_DEVELOPMENT.md` in the source tree.
