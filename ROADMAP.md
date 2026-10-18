# Roadmap: Peak controller

Controller for the Novation Peak.

## Next
- [ ] Screen follows whatever is moved or played; oscilloscope of the playing waveform when nothing is touched
- [ ] Use the free space for the X-Y pad
- [ ] Patch data over SysEx, live edits over CC/NRPN (from the Peak manual appendix)
- [ ] Patch librarian: fetch, send, import and export .syx, backup, compare

## Every cat plugin
- Draw through `catui::RenderGate` so meters and animations stop when the window is not in front (audio, automation and MIDI keep running)
- Settings page with MIDI filters on by default, selectable preset/backup folders, UI size reset to 100%
