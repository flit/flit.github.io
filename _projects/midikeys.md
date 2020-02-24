---
title: "MidiKeys"
---

MidiKeys is a small application for macOS that presents a resizeable MIDI keyboard onscreen.

[Download version 1.9](https://github.com/flit/MidiKeys/releases/download/v1.9.0/MidiKeys_1.9.zip){: .btn .btn--primary}

You can use the computer keyboard to play MIDI notes, or click on the keys with the mouse. There is
also an option to select a MIDI source and see incoming notes played on the keyboard. Global hotkeys
can be enabled, with configurable modifier keys, including none, to play notes using the computer
keyboard when other applications are frontmost.

![MidiKeys screenshot](/assets/images/midikeys_screen.png)

Note that MidiKeys has no way to produce sound on its own. In order to hear a sound when you press
keys, you need to connect the MIDI output to a synthesizer of some sort. This can be either a
software synth running on the Mac, a hardware synth, or even an iOS-based synth connected via
Bluetooth MIDI. Apple's AU Lab works nicely to play Audio Units.

MidiKeys is an open source project [hosted on GitHub](https://github.com/flit/MidiKeys). Contributions
are welcome!

[View release notes](https://github.com/flit/MidiKeys/releases/)

Version 1.9 requires macOS 10.11 or later.

If you need to run MidiKeys on older OS versions, you can use the
[version 1.8 release](https://github.com/flit/MidiKeys/releases/tag/v1.8.0).
It works all the way back to macOS 10.5.

