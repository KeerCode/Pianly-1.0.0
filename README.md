# Pianly

A free, open-source piano practice app. Upload any MusicXML or MIDI file, or try a built-in demo piece, and Pianly guides you through each note in real time — using your microphone or MIDI keyboard.

With Pianly, you don't have to worry about any "Free Practice!" message, where if you open the sheet music you get hit with a paywall.

I made this for the frustrated like me, who spent hours trying to find a way to learn and relax with piano, just to be met with greedy companies.

While it is open source, if you'd want to show appreciation/support, please consider donating once I set up a donation link lol. I need some money to train a new mic ML I'm working on. Currently, MIDI is your best bet.

I'll also need some money to put this on the app store. 

For now, enjoy, more features will be coming your way.

## IMPORTANT
The app is currently unsigned, which is why computers tend to say it's corrupt/missing files. To get through the process of getting the annoying message out, apple wants 99 dollars and Microsoft wants more money to get the app signed. Please let me know if you guys know someone who could help me out with this.


But for now, to get around them, scroll to releases

You also WILL need your own sheet music/midi file. I'm working on connecting a larger repository of sheet music for a future update. I would also recommend a cable to connect your piano to your laptop, since the current mic detection is slow.

While MIDI works very well, the mic has some troubles with latency.

The visualizer also has a bug when you change the speed in the middle of a listening session, where the notes just move to a random point.

## Features

Please do recommend any features you would like to see as well as any bugs in the issues tab.

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
> **Windows note:** Again, the app isn't notarized. to get around, click **More info** and then **Run anyway**

## Finding Sheet Music

Public domain MusicXML files can be found at:

- [IMSLP](https://imslp.org) — Large collection of public domain scores
- [MuseScore](https://musescore.com) — Community-uploaded scores exportable as MusicXML (Behind a paywall)

## License

MIT
