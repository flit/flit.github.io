---
title: "New MidiKeys version 1.9 release"
#categories:
#  - projects
tags:
  - midi
  - software
  - music
  - mac
---

After a decade-long lapse, there is finally a new release of MidiKeys. Aside from long wanting to
get a new release out, the primary motivator for this release was that the last MidiKeys release was
32-bit only and will no longer work on Catalina later. Thus, the new MidiKeys is a proper 64-bit
build.

There are also some new features included. The keyboard window is resizeable now. This was the
number one requested change, and has become even more important after over a decade of increasing
display sizes. Dark mode is supported, too. See the list below for the full set of changes.

[MidiKeys project page](/projects/midikeys)

### Version 1.9 changes

- MidiKeys is now 64-bit compliant. (And no longer a universal binary.)
- Minimum system version is 10.11.
- Keys window is resizable (probably the most asked-for feature request).
- Support for system dark mode, including a dark mode keyboard. A "force light keyboard" preference is visible to allow you to revert the keyboard to a traditional appearance.
- Added Clear Stuck Keys command.
- On systems with a trackpad or mouse that reports pressure, MidiKeys will send channel aftertouch when keys are clicked and held.
- New "show C notes" feature that draws "Cn" where "n" is the octave (i.e., C3, C4, etc) on the keyboard.
- Fixed an issue with key caps where certain keys like tab and delete were not shown; they will now appear as the standard key icons.
- Changed version update feed URL to https.
- Updated Sparkle and ShortcutRecorder frameworks to modern versions.
