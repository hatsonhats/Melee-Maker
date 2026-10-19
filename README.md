# Melee Maker

**Build your own fighter in Super Smash Bros. Melee.** Put any character's specials, aerials, ground attacks and throws on any other character, then play it locally, in Training mode, or on Slippi Online.

### ▶ [Watch the trailer on YouTube](https://youtu.be/OTISApM0g88)

[![Melee Maker trailer: click to watch on YouTube](https://img.youtube.com/vi/OTISApM0g88/maxresdefault.jpg)](https://youtu.be/OTISApM0g88)

### [⬇ Download the latest release](../../releases/latest)

---

## What you can build

Every character has **21 slots**, and each one can hold another character's move:

| Slots | Moves |
| --- | --- |
| **Specials (4)** | Neutral B, Side B, Up B, Down B |
| **Aerials (5)** | Neutral, forward, back, up and down air |
| **Ground attacks (5)** | Jab, dash attack, forward / up / down tilt |
| **Smash attacks (3)** | Forward, up and down smash |
| **Throws (4)** | Forward, back, up and down throw |

Borrowed moves keep their real hitboxes, timing, effects and items. Marth's sword appears in your hand, Peach's parasol floats you down, Mr. Game & Watch's bucket fills. Moves are sized to fit your character.

## Install

You need **[Slippi](https://slippi.gg)** and your own clean **NTSC v1.02** Melee ISO. No game files are included; the patch only works on your own copy of Melee.

1. Download the `.zip` from the [latest release](../../releases/latest) and unzip it.
2. **Windows:** drag your Melee ISO onto `DRAG VANILLA MELEE HERE.bat`.
   **Linux/Mac:** run `./patch_linux_mac.sh "path/to/Melee 1.02.iso"` (needs `xdelta3`).
3. This creates `BuildAMelee.iso` in the same folder. Set it as your Melee ISO in the Slippi Launcher settings.

## Building your character

On the character select screen, pick a character and press **Z** to open the build panel.

| Input | Action |
| --- | --- |
| Up / Down | Choose a move slot |
| Left / Right | Change the move in that slot |
| L / R | Previous / next tab |
| X | Randomize every slot |
| Y | Reset the slot |
| A | Next slot / press the selected button |
| Start, B or Z | Lock in and close |

### Saving and sharing builds

The **Saved** tab holds 3 builds on your memory card, plus your build's **share code**.

- **A** loads a saved build (or saves into an empty slot), **X** saves, **Y** deletes.
- Select the code and press **A** to type in someone else's code.
- Post your codes so others can try your builds!

> Saving needs a memory card in Slot A. Slippi Dolphin has none by default: turn it on in Dolphin's GameCube settings and restart.

## Training mode

Your build works in Training mode, with extras:

| Input (in a match) | Action |
| --- | --- |
| D-Up | Open the build panel. The **Options** tab toggles hitboxes, hurtboxes, screen shake, a missed L-cancel flash and move info |
| D-Down | Freeze |
| D-Right | Step one frame (while frozen) |
| D-Left | Move info |

Changing your build in the panel restarts the match with the new build.

## Playing online

- Builds work in **Slippi Direct** (connect code) matches. Both players' builds are exchanged automatically on the loading screen.
- **Both players need the same Melee Maker version and build.** It's shown in the bottom-left corner of the character select screen.
- **Quick chat must be on** in Slippi's settings: builds are exchanged through it.
- In Unranked and Ranked, everyone plays their character's normal moves. Please don't take a modded ISO into the public queues.
- Replays record both builds, so they play back correctly.

If the exchange fails (different versions, quick chat off, connection trouble), both players simply use their normal moves.

## Troubleshooting

- **A borrowed move plays as the character's own move:** a match has limited memory. With many different donor characters, some moves can be skipped for that match. Fewer different donors, or a smaller stage, leaves more room.
- **Builds didn't load online:** check that both players show the same build in the bottom-left corner, and that quick chat is on.
- **Found a bug?** Open an issue with your build code, what happened, and your Dolphin log (Slippi Dolphin: View → Show Log, or `dolphin.log` in the Dolphin user folder). The [log guide](https://github.com/hatsonhats/MeleeMaker-dev/blob/main/docs/LOGS.md) explains every line.

## How this was made

Melee Maker was built with the help of AI (Claude). I'm a professional software developer with 8 years of experience, and this started as a passion project for a game I love. AI didn't replace the engineering: I designed it, directed it, reviewed it, and made the calls. AI is a tool in the toolbox, like a good debugger or a decompiler: powerful, not magic, and not the end-all be-all (yet). It's also where software development is heading, and I'd rather embrace that than pretend otherwise.

The mod isn't "vibe-coded" and shipped. It has a testing framework (host tests, an automated move sweep, and checks that refactors don't change the game's code), and it has been hand-tested for weeks by three people playing real matches. I've worked to keep the code friendly to future developers: plain-language docs, a glossary, comments that explain why, and a guide for common jobs. That said, the nature of this mod makes it complicated. It retargets one character's moves onto another character's skeleton inside a 25-year-old game, without changing the game's code layout, while staying in sync with Slippi online play.

## For developers

The source, build tools and developer docs live in the **[development repo](https://github.com/hatsonhats/MeleeMaker-dev)**. Start with its README and `CONTRIBUTING.md`.

## Credits

- **[Project Slippi](https://slippi.gg)** for online play, rollback and replays.
- **[The Melee decompilation project](https://github.com/doldecomp/melee)**, without which this mod could not exist.
- Everyone who playtested and sent logs.

Super Smash Bros. Melee is © Nintendo / HAL Laboratory. Melee Maker is a fan project, not affiliated with or endorsed by Nintendo or Project Slippi.
