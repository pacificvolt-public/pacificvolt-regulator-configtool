# LVR Configuration Tool 1.1.2 — beta

Pacific Volt's tool for configuring and monitoring low voltage regulators (LVRs), over
Bluetooth, serial or the network. Windows 10 and 11, 64-bit.

**This is a beta, not a release.** The current release is
[1.0.0](https://github.com/pacificvolt-public/pacificvolt-regulator-configtool), and it is
what to install for normal use. 1.1.2 carries work that is still being tested, on top of the
translations first added in 1.1.0.

## What is new since 1.0.0

- **7 Day Summary chart.** A regulator window's **SD Card → Download and Plot 7 Day
  Summary** reads the unit's daily summary files and plots a week of half-hour averages of
  input voltage, output voltage and power on one 24-hour chart, with a slider to step
  through the days. It needs firmware that writes those summary files, which is itself still
  in test. **File → Load Month File for Summary** draws the same chart from a month log any
  regulator already produces, so the chart works on units in the field today.
- **Connecting to a regulator by IP address.** A regulator reached over the internet by IP
  now connects correctly. The address you type is the address the tool connects to, and the
  connection editor's address field is a plain text box you type the full address into.
- **A Language page in Settings** (from 1.1.0), offering Portuguese, French, Italian and
  Spanish alongside English. The tool starts in English, and English is unchanged.

The translations are a first pass that a native speaker has not yet reviewed, and some text
added since 1.1.0 is not yet translated at all. English is unaffected. Translation
corrections, and the review tables, are with the 1.1.0 beta
[here](https://github.com/pacificvolt-public/pacificvolt-regulator-configtool/tree/main/v1.1.0).

The built-in user guides under the Help menu remain in English in every language.

## Download

| | |
|---|---|
| Installer | [LVR_Configuration_Tool-1.1.2.exe](https://github.com/pacificvolt-public/pacificvolt-regulator-configtool/raw/main/v1.1.2-beta/LVR_Configuration_Tool-1.1.2.exe) |
| **Portable zip** (recommended for a beta) | [LVR_Configuration_Tool-1.1.2.zip](https://github.com/pacificvolt-public/pacificvolt-regulator-configtool/raw/main/v1.1.2-beta/LVR_Configuration_Tool-1.1.2.zip) |

**The zip is the better choice for trying this.** Unzip it anywhere and run
`LVR_Configuration_Tool-gui.exe` from the folder: it installs nothing, creates no
shortcuts, does not appear in Add/Remove Programs, and leaves an installed release exactly
as it is. Delete the folder and it is gone.

The installer will **replace an installed 1.0.0**, because to Windows both are the same
product — same folder, same entry in Add/Remove Programs. Going back afterwards means
installing 1.0.0 again.

## Install

1. Run the downloaded `.exe`.
2. Windows shows two prompts — **both are expected**. See below.
3. Accept the licence, choose the folder, and finish. **Close the tool before updating.**
4. Start it from the desktop shortcut or the Start menu.

## The two prompts Windows shows

### 1. "Windows protected your PC"

A blue screen saying Microsoft Defender SmartScreen prevented an unrecognised app from
starting.

**To continue: click "More info", then "Run anyway".**

This appears because the installer is new, not because anything is wrong with it. Windows
recognises files that very large numbers of people have already downloaded, and a new
build from a company our size has not reached that threshold. It says *unrecognised*, not
*unsafe*.

### 2. "Do you want to allow this app to make changes to your device?"

Windows asking for administrator permission, which any program installing for all users
needs. Before clicking Yes, check that it reads:

> **Verified publisher: Pacific Volt Inc.**

That line is the one that matters — it confirms the installer genuinely came from Pacific
Volt and has not been altered since we built it. Every file in this beta is signed, the
same as in a release.

**If it says "Unknown publisher", stop and contact us.** The file did not come from us, or
was damaged on the way down.

You can check this at any time without running anything: right-click the installer, choose
**Properties**, and open the **Digital Signatures** tab.

## Support

user_support@pacificvolt.com — for anything that behaves differently from 1.0.0, for
translation corrections, and for the default Advanced and Administrator passwords.
