# TDA Mox — Android System Shell Terminal

**TDA Mox** is an Android system-shell terminal application using
**Shizuku** as its required system execution interface.

It provides users with a practical Android terminal for executing
native Android system commands and Toybox utilities directly from
the device.

> **Important:** Shizuku is required for TDA Mox to operate.

## Shizuku Integration

TDA Mox requests authorization from Shizuku and uses the Shizuku
execution interface for supported Android system operations.

TDA Mox is **not an ADB client** and is **not an ADB shell emulator**.

When Shizuku is started through ADB, ADB is only involved in starting
the Shizuku service. TDA Mox communicates with Shizuku rather than
acting as an ADB client itself.

## Android System Commands

TDA Mox works with Android's native system environment and Toybox
utilities, including commands such as:

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

Command availability depends on the Android version, device,
manufacturer, Shizuku configuration, and execution permissions.

## Android Compatibility

Designed for modern Android versions including:

- Android 14
- Android 15
- Android 16

## APK Availability

The **TDA Mox APK is available for users to download and use**.

Availability of the APK does **not** mean that the application's
source code is distributed as open-source software.

See `DISCLAIMER.md` for the applicable terms.

## Download

https://github.com/TDA-Android/TDA-Mox/releases

## Documentation

- [Operation Manual](OPERATION_MANUAL.md)
- [Disclaimer](DISCLAIMER.md)

## Keywords

TDA Mox, TDA-Mox, Android terminal, Android system shell,
Android shell terminal, Shizuku terminal, Toybox terminal,
Android system commands, Android automation, Android 14,
Android 15, Android 16, dumpsys, pm, am, Android system tools.

## Disclaimer

See [DISCLAIMER.md](DISCLAIMER.md) before using TDA Mox.
