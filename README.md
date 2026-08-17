# TDA Mox — Android System Shell Terminal

**TDA Mox** is an Android system-shell terminal application that uses
**Shizuku as its required system execution interface**.

TDA Mox is designed to provide users with a practical Android terminal
for executing native Android system commands and Toybox utilities directly
from the device.

> **Important:** Shizuku is required for TDA Mox to operate.

## What is TDA Mox?

TDA Mox provides a terminal interface running in the Android system-shell
environment.

It works with Android's native command environment and Toybox utilities,
including commands such as:

- `ps`
- `dumpsys`
- `pm`
- `am`
- `cmd`
- `getprop`
- `log`
- `top`
- `mount`
- `kill`
- `readelf`
- `find`
- `grep`
- `sed`
- `tar`
- and other available Android/Toybox commands.

## Shizuku Integration

**Shizuku is required for TDA Mox to operate.**

TDA Mox requests authorization from Shizuku and uses the Shizuku
execution interface for supported Android system operations.

TDA Mox is **not an ADB client** and is **not an ADB shell emulator**.

When Shizuku is started through ADB, ADB is only involved in starting
the Shizuku service. TDA Mox communicates with Shizuku rather than
acting as an ADB client itself.

## Android System Operations

TDA Mox is designed for users who need a terminal capable of working
with Android's native system environment.

Typical uses include:

- Android system inspection
- process inspection
- package management
- Activity and service interaction
- system-property inspection
- device diagnostics
- filesystem inspection
- Toybox command execution
- local shell scripting
- Android system automation

Actual capabilities depend on the Android version, device,
Shizuku configuration, and permissions available to the execution context.

## Android Compatibility

TDA Mox is designed for modern Android versions, including:

- Android 14
- Android 15
- Android 16

Command availability may vary between Android versions and device
manufacturers.

## APK Availability

The **TDA Mox APK is provided for users to download and use**.

TDA Mox being available as a downloadable APK does **not** mean that
its source code is distributed as open-source software.

The TDA Mox release is intended to make the application available
for users under the terms described in `DISCLAIMER.md`.

## Download

Download the latest TDA Mox APK from GitHub Releases:

https://github.com/TDA-Android/TDA-Mox/releases

## Documentation

- [Operation Manual](OPERATION_MANUAL.md)
- [Disclaimer](DISCLAIMER.md)

## Keywords

TDA Mox, TDA-Mox, Android terminal, Android system shell,
Android shell terminal, Shizuku terminal, Shizuku Android terminal,
Toybox terminal, Android system commands, Android shell commands,
Android 14 terminal, Android 15 terminal, Android 16 terminal,
dumpsys terminal, pm command, am command, Android automation,
Android system tools, Android system shell terminal.

## Disclaimer

See [DISCLAIMER.md](DISCLAIMER.md) before using TDA Mox.
