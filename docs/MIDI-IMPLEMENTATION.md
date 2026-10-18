# Novation Peak: MIDI parameters (firmware 1.2)

Source: Novation Peak 1.2 user guide, "MIDI parameters list" (pages 40 to 43). Values are copied as printed in the manual. Check them against the real hardware before relying on them in code. NRPN numbers are written exactly as the manual prints them (for example `0:2`). Rows marked "pair" use two CCs; the manual does not say which is coarse and which is fine, so test it.

Settings that matter for the controller (Settings menu): MidiChan (default 1), Local, Arp>Midi, CC/NRPN (Disabled, Receive, Transmit, Rec+Tran; default Rec+Tran), Bank/Patch (same options). Patch data is sent as Program Change and Bank Change, not CC/NRPN. Patch backup goes over SysEx (Settings, Backup page).

## Voice and glide
| Parameter | CC / NRPN | Range | Default |
|---|---|---|---|
| Patch Category | NRPN 0:0 | 0-14 | 0 |
| Patch Genre | NRPN 0:1 | 0-9 | 0 |
| Voice Mode | NRPN 0:2 | 0-4 | 3 |
| Voice Unison | NRPN 0:3 | 0-4 | 0 |
| Voice Unison Detune | NRPN 0:4 | 0-127 | 25 |
| Voice Unison Spread | NRPN 0:5 | 0-127 | 0 |
| Voice Keyboard Octave | NRPN 0:6 | 61-67 (-3 to +3) | 64 (0) |
| Glide Time | CC 5 | 0-127 | 0 (60) |
| Voice Pre-Glide | NRPN 0:7 | 52-76 (-12 to +12) | 64 (Off) |
| Glide On | CC 35 | 0-1 | 0 |

## Oscillator common
| Parameter | CC / NRPN | Range | Default |
|---|---|---|---|
| Divergence | NRPN 0:9 | 0-127 | 0 |
| Drift | NRPN 0:10 | 0-127 | 0 |
| Noise LPF | NRPN 0:11 | 0-127 | 127 |
| Noise HPF | NRPN 0:12 | 0-0 | 0 |

## Oscillators 1, 2, 3
| Parameter | Osc 1 | Osc 2 | Osc 3 | Range |
|---|---|---|---|---|
| Range | CC 3 | CC 37 | CC 65 | 63-66 (-1 to +2) |
| Coarse | CC pair 14,46 | CC pair 17,49 | CC pair 20,52 | 0-255 (-128 to +127) |
| Fine | CC pair 15,47 | CC pair 18,50 | CC pair 21,53 | 28-228 (-100 to +100) |
| ModEnv2 > Pitch | CC 9 | CC 38 | CC 43 | 1-127 (-63 to +63) |
| LFO2 > Pitch | CC pair 16,48 | CC pair 19,51 | CC pair 22,54 | 1-255 (-127 to +127) |
| Wave | NRPN 0:14 | NRPN 0:23 | NRPN 0:32 | 0-4 |
| Wave More (wavetable) | NRPN 0:15 | NRPN 0:24 | NRPN 0:33 | 4-63 |
| Shape Source | NRPN 0:16 | NRPN 0:25 | NRPN 0:34 | 0-2 |
| Manual Shape | CC 12 | CC 39 | CC 71 | 0-127 (-64 to +63) |
| ModEnv1 > Shape | CC 119 | CC 40 | CC 72 | 0-127 (-64 to +63) |
| LFO1 > Shape | CC 33 | CC 41 | CC 73 | 0-127 (-64 to +63) |
| Vsync | CC 34 | CC 42 | CC 44 | 0-127 |
| Saw Density | NRPN 0:17 | NRPN 0:26 | NRPN 0:35 | 0-127 |
| Saw Density Detune | NRPN 0:18 | NRPN 0:27 | NRPN 0:36 | 0-127 |
| Fixed Note | NRPN 0:19 | NRPN 0:28 | NRPN 0:37 | 0-88 (0 = Off) |
| Bend Range | NRPN 0:20 | NRPN 0:29 | NRPN 0:38 | 40-88 (-24 to +24) |

## Mixer
| Parameter | CC / NRPN | Range | Default |
|---|---|---|---|
| Osc 1 level | CC pair 23,55 | 0-255 | 255 |
| Osc 2 level | CC pair 24,56 | 0-255 | 0 |
| Osc 3 level | CC pair 25,57 | 0-255 | 0 |
| Ring 1*2 | CC pair 26,58 | 0-255 | 0 |
| Noise level | CC pair 27,59 | 0-255 | 0 |
| Patch Level | NRPN 0:41 | 0-127 | 64 |
| VCA Gain | NRPN 0:42 | 0-127 | 127 |
| Dry Level | NRPN 0:43 | 0-127 | 127 |
| Wet Level | NRPN 0:44 | 0-127 | 127 |

## Filter
| Parameter | CC / NRPN | Range | Default |
|---|---|---|---|
| Overdrive | CC 80 | 0-127 | 0 |
| Post Drive | CC 36 | 0-127 | 0 |
| Slope | NRPN 0:45 | 0-1 | 1 |
| Shape | NRPN 0:46 | 0-2 | 0 |
| Key Tracking | CC 75 | 0-127 | 127 |
| Resonance | CC 79 | 0-127 | 0 |
| Frequency | CC pair 29,61 | 0-255 | 255 |
| LFO1 > Filter | CC pair 28,60 | 1-255 (-127 to +127) | 128 (0) |
| Osc3 > Filter | CC 76 | 0-127 | 0 |
| Env Select | NRPN 0:47 | 0-1 | 1 |
| AmpEnv > Filter | CC 77 | 1-127 (-63 to +63) | 64 (0) |
| ModEnv1 > Filter | CC 78 | 1-127 (-63 to +63) | 64 (0) |
| Divergence | NRPN 0:48 | 0-127 | 0 |

## Envelopes
| Parameter | Amp | Mod 1 | Mod 2 |
|---|---|---|---|
| Attack | CC 86 | CC 90 | CC 94 |
| Decay | CC 87 | CC 91 | CC 95 |
| Sustain | CC 88 | CC 92 | CC 117 |
| Release | CC 89 | CC 93 | CC 103 |
| Velocity (0-127, -64 to +63) | NRPN 0:55 | NRPN 0:60 | NRPN 0:64 |
| Trigger (0-1) | NRPN 0:56 | NRPN 0:61 | NRPN 0:65 |

Mod Envelope Select: NRPN 0:59 (0-1). Attack/decay/sustain/release range 0-127. Defaults: Amp 0/90/127/40, Mod 0/75/35/45.

## LFOs 1 and 2
| Parameter | LFO 1 | LFO 2 | Range |
|---|---|---|---|
| Range | NRPN 0:68 | CC 83 | 0-2 |
| Rate | CC pair 30,62 | CC pair 31,63 | 0-255 |
| Sync Rate | CC 81 | CC 84 | 0-34 |
| Wave | NRPN 0:69 | NRPN 0:78 | 0-3 |
| Phase | NRPN 0:70 | NRPN 0:79 | 0-120 |
| Slew | NRPN 0:71 | NRPN 0:80 | 0-127 |
| Fade Time | CC 82 | CC 85 | 0-127 |
| Fade In/Out | NRPN 0:72 | NRPN 0:81 | 0-3 |
| One Shot | NRPN 0:75 | NRPN 0:84 | 0-1 |
| Common | NRPN 0:76 | NRPN 0:85 | 0-1 |

LFO 3 and 4 have no CC/NRPN entries in the manual's list.

## Effects
| Parameter | CC / NRPN | Range | Default |
|---|---|---|---|
| Distortion Level | CC 104 | 0-127 | 0 |
| Effects Master Bypass | NRPN 0:88 | 0-1 | 0 |
| Effects Routing | NRPN 0:89 | 0-6 | 0 |
| Delay Level | CC 108 | 0-127 | 0 |
| Delay Time | CC 109 | 0-127 | 64 |
| Delay Width | NRPN 0:92 | 0-127 | 64 |
| Delay Sync | NRPN 0:93 | 0-1 | 0 |
| Delay Sync Time | NRPN 0:94 | 0-18 | 4 |
| Delay Feedback | CC 110 | 0-127 | 64 |
| Delay LP Damp | NRPN 0:95 | 0-127 | 85 |
| Delay HP Damp | NRPN 0:96 | 0-127 | 0 |
| Delay Slew Rate | NRPN 0:97 | 0-127 | 32 |
| Reverb Level | CC 112 | 0-127 | 0 |
| Reverb Type | NRPN 0:101 | 0-2 | 2 |
| Reverb Time | CC 113 | 0-127 | 90 |
| Reverb Damping LP | NRPN 0:102 | 0-127 | 50 |
| Reverb Damping HP | NRPN 0:103 | 0-127 | 1 |
| Reverb Size | NRPN 0:104 | 0-127 | 64 |
| Reverb Mod | NRPN 0:105 | 0-127 | 64 |
| Reverb Mod Rate | NRPN 0:106 | 0-127 | 4 |
| Reverb Low Pass | NRPN 0:107 | 0-127 | 74 |
| Reverb High Pass | NRPN 0:108 | 0-127 | 0 |
| Reverb Pre Delay | NRPN 0:109 | 0-127 | 40 |
| Chorus Level | CC 105 | 0-127 | 0 |
| Chorus Type | NRPN 0:111 | 0-2 | 2 |
| Chorus Rate | CC 118 | 0-127 | 20 |
| Chorus Mod Depth | NRPN 0:112 | 0-127 | 64 |
| Chorus Feedback | CC 107 | 0-127 (-64 to +63) | 64 |
| Chorus LP | NRPN 0:113 | 0-127 | 90 |
| Chorus HP | NRPN 0:114 | 0-127 | 2 |

## Arpeggiator and Animate
| Parameter | CC / NRPN | Range | Default |
|---|---|---|---|
| Arp/Clock Rate | not a CC/NRPN (listed NA) | 40-240 BPM | 120 |
| Sync Rate | NRPN 0:116 | 0-18 | 16th |
| Type | NRPN 0:117 | 0-6 | 0 |
| Rhythm | NRPN 0:118 | 0-32 | 0 |
| Octave | NRPN 0:119 | 0-5 | 1 |
| Gate | CC 116 | 0-127 | 64 |
| Swing | NRPN 0:120 | 20-80 | 50 |
| On | NRPN 0:121 | 0-1 | 0 |
| Key Latch | NRPN 0:122 | 0-1 | 0 |
| Key Sync | NRPN 0:123 | 0-1 | 0 |
| Animate 1 Hold | CC 114 | 0-1 | 0 |
| Animate 2 Hold | CC 115 | 0-1 | 0 |

## Mod matrix (16 slots)
Slot selection: NRPN 0:125 (0-15). For slot n (1 to 16), the manual lists:
- Source 1: NRPN n:0 (0-16)
- Source 2: NRPN n:1 (0-16)
- Depth: NRPN n:2 (0-127, meaning -64 to +63, 64 = 0)
- Destination: NRPN n:3 (0-36)

Source and destination names (display text) are in the manual's appendix; the numeric order is not printed there, so capture it from the hardware before coding the mapping.

Sources: Direct, ModWheel, AftTouch, ExprPED1, BrthPED2, Velocity, Keyboard, Lfo1+, Lfo1+/-, Lfo2+, Lfo2+/-, AmpEnv, ModEnv1, ModEnv2, Animate1, Animate2, CV +/-, Lfo3+, Lfo3+/-, Lfo4+, Lfo4+/-, BndWhl+, BndWhl-.

Destinations: O123Ptch, Osc1Ptch, Osc2Ptch, Osc3Ptch, Osc1VSnc, Osc2VSnc, Osc3VSnc, Osc1Shpe, Osc2Shpe, Osc3Shpe, Osc1 Lev, Osc2 Lev, Osc3 Lev, NoiseLev, Ring Lev, VcaLevel, Filt Drv, FiltDist, FiltFreq, Filt Res, Lfo1Rate, Lfo2Rate, AmpEnv A/D/R, ModEnv1A/D/R, ModEnv2A/D/R, FM O1>O2, FM O2>O3, FM O3>O1, FM Ns>O1, O3>FiltF, Ns>FiltF. Only positive depth works for the FM destinations.

FX matrix (4 slots) destinations: Dist Lev, Chor Lev, ChorRate, Chor Dep, Chor FB, Del Lev, Del Time, Del FB, Rev Lev, Rev Time, Rev LPF, Rev HPF. Its NRPN numbers are not in the manual's list.

## Open questions (test on hardware)
- Which CC of each pair is the high byte.
- Numeric order of mod sources and destinations.
- NRPN number format (the manual prints `0:2`; confirm how it maps to CC 99/98).
- Wave More is listed as 4-63 for 60 wavetables.
