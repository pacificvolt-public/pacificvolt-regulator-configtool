# LVR Configuration Tool — downloads

Pacific Volt's tool for configuring and monitoring low voltage regulators (LVRs), over
Bluetooth, serial or the network. Windows 10 and 11, 64-bit.

This repository holds the published builds and nothing else — no source code.

## Download

### 1.1.0 — current

| | |
|---|---|
| **Installer** (recommended) | [LVR_Configuration_Tool-1.1.0.exe](https://github.com/pacificvolt-public/pacificvolt-regulator-configtool/raw/main/installers/LVR_Configuration_Tool-1.1.0.exe) |
| Portable zip (no installer) | [LVR_Configuration_Tool-1.1.0.zip](https://github.com/pacificvolt-public/pacificvolt-regulator-configtool/raw/main/installers/LVR_Configuration_Tool-1.1.0.zip) |

New in 1.1.0: a **Language** page in Settings, offering Portuguese, French, Italian and
Spanish alongside English. The tool still starts in English, and English is unchanged.

The translations are a first pass that a native speaker has not yet reviewed. They cover
the whole interface, but expect wording a native reader would put differently — the
electrical terminology especially. Corrections are welcome: send them to the support
address below.

### 1.0.0 — previous

Kept available for anyone who needs to go back to it.

| | |
|---|---|
| Installer | [LVR_Configuration_Tool-1.0.0.exe](https://github.com/pacificvolt-public/pacificvolt-regulator-configtool/raw/main/installers/LVR_Configuration_Tool-1.0.0.exe) |
| Portable zip (no installer) | [LVR_Configuration_Tool-1.0.0.zip](https://github.com/pacificvolt-public/pacificvolt-regulator-configtool/raw/main/installers/LVR_Configuration_Tool-1.0.0.zip) |

Both versions are signed by Pacific Volt Inc.

## Install

1. Run the downloaded `.exe`.
2. Windows shows two prompts — **both are expected**. See below.
3. Accept the licence, choose the folder, and finish. Installing replaces any earlier
   version in place; you do not need to uninstall first. **Close the tool before updating.**
4. Start it from the desktop shortcut or the Start menu.

The portable zip needs no installation: unzip it anywhere and run
`LVR_Configuration_Tool-gui.exe` from the folder. It creates no shortcuts and does not
appear in Add/Remove Programs.

## The two prompts Windows shows

### 1. "Windows protected your PC"

A blue screen saying Microsoft Defender SmartScreen prevented an unrecognised app from
starting.

**To continue: click "More info", then "Run anyway".**

This appears because the installer is new, not because anything is wrong with it. Windows
recognises files that very large numbers of people have already downloaded, and a new
release from a company our size has not reached that threshold. It says *unrecognised*, not
*unsafe*.

### 2. "Do you want to allow this app to make changes to your device?"

Windows asking for administrator permission, which any program installing for all users
needs. Before clicking Yes, check that it reads:

> **Verified publisher: Pacific Volt Inc.**

That line is the one that matters — it confirms the installer genuinely came from Pacific
Volt and has not been altered since we built it. Every file we ship is signed.

**If it says "Unknown publisher", stop and contact us.** The file did not come from us, or
was damaged on the way down.

You can check this at any time without running anything: right-click the installer, choose
**Properties**, and open the **Digital Signatures** tab.

## Support

user_support@pacificvolt.com — also the address for the default Advanced and Administrator
passwords.
