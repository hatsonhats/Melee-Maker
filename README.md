# Melee Maker

Build your own fighter in Super Smash Bros. Melee: put any character's
specials, aerials, jab, dash attack, tilts, smash attacks and throws on any
other character, then play locally or on Slippi Online. Also works in Training mode and Vs mode locally.

https://youtu.be/OTISApM0g88?si=uny6zhEeD--oX1FH

development repo: [https://github.com/hatsonhats/BuildAMelee-dev](https://github.com/hatsonhats/MeleeMaker-dev)

## [Download the latest release](../../releases/latest)

## Install

You need **Slippi** and a clean **NTSC v1.02** Melee ISO.

1. Download the `.zip` from the [latest release](../../releases/latest) and unzip it.
2. **Windows:** drag your Melee ISO onto `DRAG VANILLA MELEE HERE.bat`.
   **Linux/Mac:** `./patch_linux_mac.sh "path/to/Melee 1.02.iso"` (needs `xdelta3`).
3. This creates `BuildAMelee.iso` in the same folder. Set it as your Melee ISO
   in the Slippi Launcher settings.

To play online, both players need the same BuildAMelee version. The version
is shown in the bottom-left corner of the character select screen (1.1 and later).

## How this was made

Melee Maker was built with the help of AI (Claude). I'm a professional software developer with 8 years of experience, and this started as a passion project for a game I love. AI didn't replace the engineering: I designed it, directed it, reviewed it, and made the calls. AI is a tool in the toolbox, like a good debugger or a decompiler: powerful, not magic, and not the end-all be-all (yet). It's also where software development is heading, and I'd rather embrace that than pretend otherwise.

The mod isn't "vibe-coded" and shipped. It has a testing framework (host tests, an automated move sweep, and checks that refactors don't change the game's code), and it has been hand-tested for weeks by three people playing real matches. I've worked to keep the code friendly to future developers: plain-language docs, a glossary, comments that explain why, and a guide for common jobs in CONTRIBUTING.md. That said, the nature of this mod makes it complicated. It retargets one character's moves onto another character's skeleton inside a 25-year-old game, without changing the game's code layout, while staying in sync with Slippi online play.

## Controls

On the character select screen, pick a character and press **Z** to open the
build panel.

| Input | Action |
| --- | --- |
| Up / Down | Choose a move slot |
| Left / Right | Change the move in that slot |
| L / R | Previous / next tab |
| X | Randomize every slot |
| Y | Reset the slot |
| A | Next slot / press the selected button |
| Start, B or Z | Lock in and close |

No game files are included. The patch only works on your own copy of Melee.
