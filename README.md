# TDA Mox — Android System Shell Terminal

**TDA Mox** is an Android system-shell terminal application that uses
**Shizuku** as its required system execution interface.

TDA Mox provides a practical terminal environment for executing
Android system commands and available Toybox utilities directly
from the device.

> **Shizuku is required for TDA Mox to operate.**

## What TDA Mox Does

TDA Mox is designed for users who need direct access to the Android
system-shell environment through a terminal interface.

Depending on the device, Android version, Shizuku configuration,
and available permissions, users can work with commands such as:

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

This makes TDA Mox useful for:

- Android system inspection
- process inspection
- package management
- Activity and service operations
- system-property inspection
- device diagnostics
- filesystem inspection
- Toybox command execution
- shell scripting
- Android system automation

Actual command availability and permissions depend on the device
and Android execution environment.

## Shizuku

**Shizuku is required.**

TDA Mox uses Shizuku as its system execution interface.

TDA Mox is **not an ADB client** and does not emulate an ADB shell.

When Shizuku is started using ADB, ADB is used to start the Shizuku
service. TDA Mox then communicates with Shizuku rather than acting
as an ADB client itself.

## Android Compatibility

TDA Mox is intended for modern Android versions, including:

- Android 14
- Android 15
- Android 16

Device manufacturers may expose different commands or permissions.

## APK Availability

The **TDA Mox APK is available for users to download and use**.

The availability of a downloadable APK does **not** mean that the
application source code is distributed as open-source software.

TDA Mox is distributed to users under the terms described in
`DISCLAIMER.md`.

## Download

Download TDA Mox from GitHub Releases:

https://github.com/TDA-Android/TDA-Mox/releases

## Documentation

- [Operation Manual](OPERATION_MANUAL.md)
- [Disclaimer](DISCLAIMER.md)

## Keywords

TDA Mox, TDA-Mox, Android terminal, Android system shell,
Android shell terminal, Shizuku terminal, Toybox terminal,
Android system commands, Android system tools, Android automation,
Android 14, Android 15, Android 16, dumpsys, pm, am, cmd,
Android system inspection, Android shell commands.

## Disclaimer

See [DISCLAIMER.md](DISCLAIMER.md) before using TDA Mox.
