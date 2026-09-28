# LVR Configuration Tool 1.1.0 — beta

Pacific Volt's tool for configuring and monitoring low voltage regulators (LVRs), over
Bluetooth, serial or the network. Windows 10 and 11, 64-bit.

**This is a beta, not a release.** The current release is
[1.0.0](https://github.com/pacificvolt-public/pacificvolt-regulator-configtool), and it is
what to install for normal use. 1.1.0 exists so that the translations in it can be tried
and corrected.

## What is new in 1.1.0

A **Language** page in Settings, offering Portuguese, French, Italian and Spanish alongside
English. Choosing a language takes effect immediately. The tool starts in English, and
English is unchanged from 1.0.0 — as is everything else the tool does.

The translations are a first pass that a native speaker has not yet reviewed. They cover
the whole interface — every screen, message and menu — but expect wording a native reader
would put differently, the electrical terminology especially. **Corrections are what this
build is for**; send them to the support address below.

The built-in user guides under the Help menu remain in English in every language.

## Reviewing the translations

Every translated string is listed in [docs/](docs/), one document per language, as Markdown
and as a spreadsheet holding the same table:

| Language | Table | Spreadsheet |
|---|---|---|
| European Portuguese (pt-PT) | [portugal-localize.md](docs/portugal-localize.md) | [portugal-localize.xlsx](https://github.com/pacificvolt-public/pacificvolt-regulator-configtool/raw/main/v1.1.0/docs/portugal-localize.xlsx) |
| French (fr-FR) | [france-localize.md](docs/france-localize.md) | [france-localize.xlsx](https://github.com/pacificvolt-public/pacificvolt-regulator-configtool/raw/main/v1.1.0/docs/france-localize.xlsx) |
| Italian (it-IT) | [italy-localize.md](docs/italy-localize.md) | [italy-localize.xlsx](https://github.com/pacificvolt-public/pacificvolt-regulator-configtool/raw/main/v1.1.0/docs/italy-localize.xlsx) |
| Spanish (es-ES) | [spain-localize.md](docs/spain-localize.md) | [spain-localize.xlsx](https://github.com/pacificvolt-public/pacificvolt-regulator-configtool/raw/main/v1.1.0/docs/spain-localize.xlsx) |

Each row gives the English, our translation, any question we have about it, and an empty
**Your correction** column. Fill that column in — or edit the translation directly — and
send the file back; nothing needs to be installed and no software knowledge is required.
The spreadsheet is easier for long text and for anything carrying markup.

The rows are grouped by where the text appears in the tool, so a reviewer can work through
one screen at a time rather than an alphabetical list, and the questions are there because a
first pass that says where it is unsure is worth more than one that sounds confident
throughout.

## Download

| | |
|---|---|
| Installer | [LVR_Configuration_Tool-1.1.0.exe](https://github.com/pacificvolt-public/pacificvolt-regulator-configtool/raw/main/v1.1.0/LVR_Configuration_Tool-1.1.0.exe) |
| **Portable zip** (recommended for a beta) | [LVR_Configuration_Tool-1.1.0.zip](https://github.com/pacificvolt-public/pacificvolt-regulator-configtool/raw/main/v1.1.0/LVR_Configuration_Tool-1.1.0.zip) |

**The zip is the better choice for trying this.** Unzip it anywhere and run
`LVR_Configuration_Tool-gui.exe` from the folder: it installs nothing, creates no
shortcuts, does not appear in Add/Remove Programs, and leaves an installed 1.0.0 exactly
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

user_support@pacificvolt.com — for translation corrections, for anything that behaves
differently from 1.0.0, and for the default Advanced and Administrator passwords.
