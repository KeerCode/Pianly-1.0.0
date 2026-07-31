# Pianly

A free, open-source piano practice app. Upload any MusicXML or MIDI file, or try a built-in demo piece, and Pianly guides you through each note in real time — using your microphone or MIDI keyboard.

No paywall. No account. Just play.

Please consider donating once I set up a donation link lol. I need some money to train a new mic ML i'm working on. I'll also need some money to put this on the app store.

## Features

### Sheet Music Practice

Follow along with rendered sheet music. Pianly highlights the current note and waits for you to play it correctly before advancing.

- Sheet music rendering for `.xml`, `.musicxml`, and `.mxl` files
- Strict practice — must play the exact target note(s) to advance
- Chord support — build chords note-by-note; all notes must be held before moving on
- Tied note handling — notes connected by ties are automatically skipped
- Wrong note hints — after 3 wrong attempts, Pianly plays the target note for you
- Interval display — shows the interval between consecutive notes (Minor 3rd, Perfect 5th, etc.)
- Any-octave mode — accept the correct note name regardless of octave
- Auto-scroll — sheet music scrolls to keep the current bar in view
- Progress bar — visual note and measure progress
- Listen mode — play back the full piece with cursor following along
- Playback speed control — slow down or speed up from 25% to 200%

### Visualizer

A falling-notes view (Synthesia-style) with two sub-modes:

- **Watch mode** — Notes fall onto the piano keyboard; keys highlight as they play
- **Practice mode** — Pauses automatically when wrong or missing notes reach the keyboard
  - Green keys = correct notes being held
  - Red keys = wrong notes being held
  - Amber outline = target notes while paused
  - Anti-cheat rewind — pressing Play when a note was missed rewinds back to that note
  - Press any key to begin — practice starts only when you start playing
- Chord detection — all chord notes must be held with no extras to advance
- Customizable colors — set independent colors for right and left hand notes
- Note name labels — toggle note names on falling bars and piano keys
- Optional piano audio playback during Watch mode

### Input

- **MIDI keyboard** — Connect any MIDI keyboard for instant, precise detection
- **Microphone** — Play acoustically and Pianly detects your notes in real time

## Coming Soon

Currently building a custom ML model specifically designed for microphone-only detection. The goal is significantly better accuracy, lower latency, and fewer false notes compared to the current solution — making mic input feel as reliable as a MIDI keyboard.

Actively researching ways to accurately convert from more formats to MusicXML.

Also trying to find APIs/places to get open source sheet music in bulk.

## Download

Go to the [Releases](https://github.com/KeerCode/Pianly-1.0.0/releases) page and download the latest version for your platform:

| Platform | File |
|---|---|
| **macOS (Apple Silicon)** | `.dmg` (arm64) |
| **macOS (Intel)** | `.dmg` (x64) |
| **Windows** | `.msi` or `.exe` |

> **macOS note:** The app is not notarized, so on first launch you may need to right-click the app and select **Open**, then click **Open** again in the dialog. You only need to do this once.
> If that doesn't work run 
  xattr -cr /Applications/Pianly.app
  once you moved the Pianly to your applications folder.

## Finding Sheet Music

Public domain MusicXML files can be found at:

- [IMSLP](https://imslp.org) — Large collection of public domain scores
- [MuseScore](https://musescore.com) — Community-uploaded scores exportable as MusicXML (Behind a paywall)

## License

MIT
