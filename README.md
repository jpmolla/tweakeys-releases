# Tweakeys — Downloads

**Tweakeys** is a keyboard layout engine. Instead of relying on your operating
system's layout, it emulates the whole keyboard in software. This brings
features usually reserved for programmable keyboards to any standard keyboard:

- 9 layers (Shift, AltGr, AltGr+Shift, CapsLock, Left Alt, Ctrl, Win…)
- chainable dead keys, Greek and Cyrillic alphabets, math symbols, ligatures
- combos (several keys pressed together) and hold-tap (tap ≠ hold)
- physical key remapping (e.g. CapsLock → Shift)

Any layout can be described in a single `config.json` file. Tweakeys ships with a default **US QWERTY** layout with dead keys on AltGr; other layouts are distributed separately by their authors.

This repository only hosts **prebuilt binaries**. The source code is not (yet) public.

## Download the latest version

| System | File |
|---|---|
| Windows 10/11 (64-bit) | [twk-windows-x64.zip](https://github.com/jpmolla/tweakeys-releases/releases/latest/download/twk-windows-x64.zip) |
| Linux X11 (64-bit) | [twk-linux-x64.tar.gz](https://github.com/jpmolla/tweakeys-releases/releases/latest/download/twk-linux-x64.tar.gz) |

All versions and release notes: [Releases](https://github.com/jpmolla/tweakeys-releases/releases).

## Installation

### Windows

1. Extract the archive to a folder of your choice.
2. Run `twk.exe`. An icon appears in the system tray.
3. Use this icon to pause or quit Tweakeys.

> **SmartScreen / antivirus warning**: Tweakeys intercepts keystrokes to
> transform them, which may trigger a warning. Verify the file's SHA256
> checksum (see below), then choose "More info → Run anyway".

### Linux

```bash
tar -xzf twk-linux-x64.tar.gz
cd twk
./twk
```

> **Current Linux limitations**: **X11 sessions only** (no Wayland).
> Only layers and dead keys are supported; combos, hold-tap and remapping
> are currently Windows-only.

## Verify integrity

Each release includes a `SHA256SUMS` file.

**Windows (PowerShell)**:
```powershell
Get-FileHash .\twk-windows-x64.zip -Algorithm SHA256
```
Compare the result with the matching line in `SHA256SUMS`.

**Linux**:
```bash
sha256sum -c SHA256SUMS --ignore-missing
```

## Customize your layout

Tweakeys reads the `config.json` file located next to the executable.
A visual online editor for creating your own layout is in the works.

## Report an issue

Open an [issue](https://github.com/jpmolla/tweakeys-releases/issues) with your
system, Tweakeys version and steps to reproduce the problem.

## License

See the `LICENSE` file included in each archive.