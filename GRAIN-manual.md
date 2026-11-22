# GRAIN — User Manual

*A granular cloud synth with MPC-style pads, a 16-step sequencer and a small modular rack, running in your browser.*

---

## Contents

1. [What GRAIN is](#1-what-grain-is)
2. [Getting started](#2-getting-started)
3. [The screen](#3-the-screen)
4. [The cloud stage](#4-the-cloud-stage)
5. [Cloud tab](#5-cloud-tab)
6. [Beats tab](#6-beats-tab)
7. [Rack tab](#7-rack-tab)
8. [Pitch tab](#8-pitch-tab)
9. [Motion tab](#9-motion-tab)
10. [FX tab](#10-fx-tab)
11. [Presets and sharing](#11-presets-and-sharing)
12. [Keyboard shortcuts](#12-keyboard-shortcuts)
13. [Recipes](#13-recipes)
14. [Troubleshooting](#14-troubleshooting)
15. [Reference: ranges and limits](#15-reference-ranges-and-limits)

---

## 1. What GRAIN is

GRAIN has two engines that run separately or together:

- **The cloud.** A granular synth plays hundreds of tiny fragments ("grains") of a sound at once, so they blur into a texture. The source can be one of six built-in synth voices or an audio file you load. Grains are pitched to the current chord, so the texture is always in key.
- **The beats.** Sixteen pads play a built-in drum kit, your own samples or chops of the cloud's sound. A 16-step sequencer plays them, and extra lanes gate and stutter the cloud in time with the beat.

The **rack** connects the two: an envelope, random and step-CV sources, stutter and ratchet modules, patched into the cloud with virtual cables.

---

## 2. Getting started

1. **Put on headphones.** A lot of the stereo movement is lost on laptop speakers.
2. Click **ENTER THE CLOUD**. The cloud starts playing the built-in synth voice.
3. Press **▶ BEATS** in the top bar, or **Enter**, to start the drum pattern.
4. Drag across the cloud in the middle of the screen to move through the sound. Tap a few keys on the **NOTES** strip to change the chord.

To use your own sound, **drag an audio file anywhere onto the page**. It replaces the cloud's source. If you drop it on a pad, it loads into that pad instead.

> Browsers don't let pages make sound until you click. If you hear nothing, press **▶ CLOUD** or **▶ BEATS** once.

---

## 3. The screen

| Area | What it shows |
|---|---|
| **Top bar** | **▶ CLOUD** and **▶ BEATS** start and stop the two engines. Also here: the master volume knob, preset slots 1–8, **SAVE**, **SHARE** and **⚄ MUTATE ALL**. |
| **Readout** | The current chord, the harmony status (time until the next chord, or the current bar), the beats status (tempo, step, REC) and the cloud status (source, length, grains per second, grain size, FROZEN or LOOP). |
| **Cloud stage** | The source's waveform, with every grain drawn as a glowing dot. When the beats run, a 16-step bar appears along the top edge. |
| **Notes strip** | The notes of the current key and scale across four octaves. Lit keys are the notes sounding now. |
| **Dock** | Tabs for **cloud, beats, rack, pitch, motion** and **fx**. **MORE ▸** shows extra settings where a tab has them, and **▾ HIDE** collapses the dock to give the cloud more room. |

### Using knobs

- **Drag** up or down (or left or right) to turn. **Shift-drag** for fine control.
- **Mouse wheel** nudges the value.
- **Double-click** resets to the value the page started with.
- Click a knob, then use the **arrow keys**.

---

## 4. The cloud stage

The stage is a picture of the source sound, and you can play it directly.

| Gesture | Result |
|---|---|
| **Drag left and right** | Moves the **position**, the part of the sound grains are taken from. |
| **Drag up and down** | Sets the **spray**, how far grains scatter around the position. The top is wide and the bottom is tight. |
| **Tap** (no drag) | Fires a burst of grains at the playhead. The **tap burst** setting controls the size. |

What you see:

- **Blue vertical line:** the playhead (position).
- **Shaded band:** the spray window.
- **White and blue dots:** normal grains. **Pink dots** are reversed grains, and **violet dots** come from taps, pads or bursts.
- Dots rise or fall with their pitch and drift sideways with their stereo pan.
- The glow behind the cloud pulses with the kick drum.
- **FROZEN** appears top-left when freeze is on, and **REPEAT 1/16** (or similar) top-right while the stutter is active.

---

## 5. Cloud tab

### Cloud

| Control | What it does |
|---|---|
| **Grain** | Turns the cloud on or off. |
| **Position** | Where in the source the grains are taken from (0–100%). |
| **Spray** | Random scatter around the position. Low spray stays focused and high spray jumps around the whole sound. |
| **Grain size** | Length of each grain, 10–500 ms. Short grains sound buzzy and glitchy; long grains sound smooth, close to the original. |
| **Fade in** | How long each grain takes to swell in, shown in ms. Short values sound clicky and percussive; long values sound soft. |
| **Fade out** | How long each grain takes to die away. Short values cut off cleanly. |
| **Density** | Grains per second, 2–120. More grains make a thicker cloud. |
| **Scan** | Makes the playhead travel through the sound on its own, left (←) or right (→). Centre = still. |
| **Freeze** | Holds the playhead in place. It stops the scan and any LFO that is moving the position, and grains keep playing. |
| **Level** | The cloud's volume, 0–200%. |

Fade in and fade out are fractions of the grain size, so changing the grain size changes the times shown. If the two add up to more than the whole grain, they are scaled to fit.

### Rhythm · 8-bar loop

This turns the cloud from a free-flowing texture into a repeating, rhythmic loop. It only works while the beats are running.

| Control | What it does |
|---|---|
| **Lock to loop** | Grains fire only on grid hits, in time with the beat and its swing. Every grain choice (where it lands, its pitch, whether it plays reversed, its pan) repeats exactly every 8 bars. At the start of each loop the scan and both LFOs restart from the beginning. |
| **Grid** | Grid spacing: 1/4, 1/8, 1/16 or 1/32 notes. |
| **Re-roll** | Gives a new variation of the loop. The variation is saved with presets. |

When locked, **density** sets how busy each hit is. Low density gives sparse, skipping hits and high density gives thick stabs.

### Source

| Control | What it does |
|---|---|
| **Source** | Chooses what the cloud plays: one of six built-in voices or your own sound. |
| **Load sound** | Opens a file picker. Dropping a file anywhere on the page does the same. |
| **Forget** | Removes your loaded sound and goes back to the built-in synth. |

Built-in voices. Each is a 6-second sound generated in the browser the first time you pick it:

| Voice | Character |
|---|---|
| **synth · classic** | A tour of textures: filtered noise, vocal formants, FM bell, resonant saw sweep, metallic shimmer. |
| **synth · glass** | Struck bell and glass tones spread across the stereo field. |
| **synth · choir** | A detuned "aah" that morphs through vowels (aah → ooh → ee → aah). Moving the position changes the vowel. |
| **synth · tape strings** | A warm string ensemble with tape wow and flutter and a slowly opening filter. |
| **synth · sub drone** | A dark resonant drone with a sweeping filter and sub bass, about an octave lower than the others. |
| **synth · bowed metal** | A bowed metal bar that swells and wavers, then is struck twice near the end. |

Your own sound is kept in the browser and is still there the next time you open the page.

### Texture (MORE ▸)

| Control | What it does |
|---|---|
| **Reverse** | Chance that a grain plays backwards. |
| **Width** | Stereo spread of the grains. |
| **Tap burst** | Number of grains in a burst from a tap or note key, 3–25. |

---

## 6. Beats tab

### Pads

Sixteen pads in a 4×4 grid, laid out like an MPC: pad 1 is bottom-left and pad 16 is top-right.

- **Click** a pad to play it and select it. Hitting nearer the top of a pad plays louder.
- While the beats tab is open, the **keyboard** plays the pads (hold **Shift** for full volume):

```
  1   2   3   4      ← pads 13–16
  Q   W   E   R      ← pads 9–12
  A   S   D   F      ← pads 5–8
  Z   X   C   V      ← pads 1–4
```

- Each pad shows its name and a tiny version of its 16-step pattern.
- Name colours: **yellow** = your own sample or a chop, **blue** = the cloud pad. A dimmed pad is muted.

**The built-in kit**

| Pad | Sound | Pad | Sound |
|---|---|---|---|
| 1 | kick | 9 | low tom |
| 2 | snare | 10 | hi tom |
| 3 | clap | 11 | 808 (tuned to E) |
| 4 | rim | 12 | cowbell |
| 5 | hat | 13 | zap |
| 6 | open hat | 14 | blip |
| 7 | shaker | 15 | stab |
| 8 | crash | 16 | **cloud** |

- The **hat** and **open hat** cut each other off, like a real kit.
- The **cloud** pad fires a burst of grains from the cloud, pitched to the current chord. Its **decay** knob sets the size of the burst.

### Sequencer

| Control | What it does |
|---|---|
| **▶ Play / ■ Stop** | Starts and stops the beat. The **▶ BEATS** button in the top bar and **Enter** do the same. |
| **● Rec** | Record mode. While the beat runs, pads you play are written onto the nearest step. |
| **Tempo** | 60–180 BPM. |
| **Swing** | Delays every second 16th note, 0–60%. |
| **Beat level** | Volume of all the pads together. |
| **New beat** | Writes a random pattern. |
| **Clear all** | Empties every pad's pattern. |

**Steps.** The row of 16 steps shows the selected pad's pattern.

- Click a step to cycle: **off → on → accent → off**.
- **Shift-click** a step to jump straight to accent or back to off.
- Accents play at full volume; normal steps play at about 70%.

**Ratchet row.** This row sits under the steps. Click a step to cycle **· → ×2 → ×3 → ×4**, which fires the pad that many times within the step. Use it for hi-hat rolls and snare flams.

**Row tools** (selected pad only):

| Tool | What it does |
|---|---|
| **Clear row** | Empties the row. |
| **Quarters** | Turns steps 1, 5, 9 and 13 on, or off if they're already on. |
| **Random** | Fills the row with a random pattern. |
| **◂ shift / shift ▸** | Rotates the pattern one step left or right. |

### Lanes

Two extra rows that act on the cloud and the whole mix rather than on a pad.

| Lane / control | What it does |
|---|---|
| **Cloud gate** (blue row) | While the beat runs and the **VCA** is on, the cloud only sounds on lit steps. The ADSR on the rack tab shapes each note. Clicking a gate step turns the VCA on automatically. |
| **Stutter** (pink row) | Lit steps repeat a short slice of the whole mix. Lit steps next to each other hold the same slice. |
| **VCA** | Turns the cloud gate on or off. |
| **Gate length** | How long each gate step is held before the release, 10–100% of the step. |
| **Repeat** | Stutter slice length: 1/4, 1/8, 1/16, 1/32 or 1/64. |
| **Repeat level** | **Hold** loops the slice forever; lower values make it fade away like an echo. |
| **Retrig** | When on, every lit stutter step grabs a fresh slice instead of holding the first one. |

### Chops

Slices the cloud's current sound into 16 equal pieces, one per pad. Chops cut each other off, like an MPC in mono mode.

| Button | What it does |
|---|---|
| **Chop whole sound** | Slices the entire source. |
| **Chop around playhead** | Slices only the area around the playhead: about a third of the sound, or more if spray is high. Freeze on a section you like first. |
| **In-order pattern** | Puts each chop on its own step, so the sound plays back in order at your tempo. Rearrange it from there. |
| **Keep used chops** | Chops with no steps go back to their drum sounds, and chops you've sequenced stay. |
| **Reset all pads** | Puts the whole built-in kit back. |

### Selected pad

| Control | What it does |
|---|---|
| **Level** | Pad volume, 0–150%. |
| **Tune** | ±24 semitones. |
| **Decay** | Shortens the sound; "full" plays it to the end. On the cloud pad it sets the burst size. |
| **Pan** | Left and right position. |
| **FX send** | How much of the pad goes to the reverb and delay. |
| **Mute** | Silences the pad, including its pattern. |
| **Load sample** | Puts an audio file on this pad. You can also drop a file on the pad. |
| **Grab cloud** | Copies a 0.7-second slice from the cloud's playhead onto this pad. |
| **Swap with…** | Click this, then another pad, to trade the two pads' sounds, settings and steps. |
| **Reset** | Puts this pad's original drum sound back. |

Samples you load, grab or chop are saved in the browser.

---

## 7. Rack tab

A small Eurorack-style panel. **Source modules** have output jacks, the **cloud · in** module has input jacks, and you connect them with cables. Most modules are clocked by the beat, so start the beats to hear them.

### Patching

1. Click an **output jack**. It blinks, and the cloud inputs light up.
2. Click a **cloud input**. A cable appears.
3. To unplug, click a patched input. All cables into it are removed.

The knob under each input sets **how much** the cables move that setting. Turn it negative to flip the direction. Each output can feed several inputs, and each input can take several cables.

### Modules

**ENV · ADSR**

| Control | What it does |
|---|---|
| **Attack / Decay / Release** | 2 ms – 4 s. |
| **Sustain** | Level held after the decay (0–100%). |
| **Trigger** | What fires the envelope: the gate lane, every 1/16, every 1/8, every beat or every bar. |
| **VCA** | When on, the envelope controls the cloud's volume. |
| **Gate length** | How long each trigger is held before the release starts. |

Output: **env** (0 to 1).

**RND · S&H.** Picks a new random value on each clock tick. Output: **rnd** (−1 to +1).

| Control | What it does |
|---|---|
| **Clock** | 1/16, 1/8, 1/4 or one bar. |
| **Slew** | Smooths the jumps into glides. |

In lock-to-loop mode the random values repeat with the loop.

**STEP · CV.** Eight sliders, played in order on the clock (1/16, 1/8, 1/4 or bar). Drag a slider up or down to set its value. The current step is outlined. Output: **step** (−1 to +1).

**LFO.** Output jacks for LFO 1 and LFO 2. Their rate and shape are set on the motion tab, and cables carry the full LFO swing regardless of each LFO's depth knob.

**Stutter**

| Control | What it does |
|---|---|
| **Repeat / Repeat level / Retrig** | Same as on the beats tab. |
| **HOLD** | Press and hold to stutter the whole mix live. **T** on the keyboard does the same. While the beats run, the stutter starts on the next 1/16. |

**Ratchet**

| Control | What it does |
|---|---|
| **Cloud ratchet** | Chance that an envelope trigger, or a loop hit in lock-to-loop mode, splits into fast repeats. |
| **Max** | Most repeats allowed: ×2, up to ×3 or up to ×4. |

**Cloud · in.** Inputs: **position, spray, size, density, pitch, width, cutoff, volume, fade** (both grain fades) and **ratchet** (cloud ratchet chance).

The page starts with one cable connected: **step → cutoff** at +35.

---

## 8. Pitch tab

### Key

| Control | What it does |
|---|---|
| **Root** | The key's starting note (C–B). |
| **Scale** | phrygian, locrian, harmonic minor, phrygian dominant, double harmonic, hirajoshi, iwato, in sen, minor or dorian. |

### Notes strip

The strip above the dock shows the scale across four octaves. A dot marks each root note.

- Tap a key to add it to the chord or remove it.
- Up to 8 notes can sound at once; adding a ninth drops the oldest.
- Keys flash blue when grains play that note.
- **New chord** (or **G**) makes a random chord in the scale, and **clear** removes all notes.

### Chords

| Control | What it does |
|---|---|
| **Chord every** | Changes the chord automatically every 10, 20, 40, 80 or 160 seconds, or **never · hold**. |
| **Note drift** | How often single notes wander to a neighbouring note (checked every 8 seconds). |

Both pause while **lock to beat** is on.

### Chord sequence · 8 bars

Eight chord slots, one per bar.

| Control | What it does |
|---|---|
| **Lock to beat** | While the beats run, each bar plays the next chord and the sequence loops every 8 bars. The playing bar lights up. |
| **New progression** | Writes a fresh progression that fits the scale. |

**Editing a bar:** click it, then tap note keys. While the beat plays, edits go to the bar you're hearing. **G** replaces that bar with a random chord.

Changing the root or scale moves the whole progression into the new key.

### Grain pitch

| Control | What it does |
|---|---|
| **Pitch** | **Follow chord**: each grain plays a note from the current chord. **Fixed pitch**: grains play at the source's own pitch, plus transpose and scatter. |
| **Transpose** | ±24 semitones for all grains. |
| **Scatter** | In follow-chord mode, the chance a grain jumps up an octave, two octaves, a fifth or down an octave. In fixed mode, a random pitch spread. |

> **How pitch works.** In follow-chord mode, the note **C4** on the strip plays the source at its original pitch. Higher notes speed the grains up and lower notes slow them down.

---

## 9. Motion tab

Two LFOs that move cloud settings automatically. Each shows a live scope.

| Control | What it does |
|---|---|
| **Target** | position, spray, size, density, pitch, width, cutoff, volume, fade or off. |
| **Shape** | sine, triangle, square, saw, s&h (stepped random) or smooth random. |
| **Rate** | From one cycle every 50 seconds up to 12 Hz. |
| **Depth** | How far it moves the target. |

LFO 1 starts on **position** (slow sine) and LFO 2 on **size** (smooth random). Both are also available as patch sources on the rack.

---

## 10. FX tab

The cloud runs through the lowpass and drive. The cloud and the pads (each pad by its FX send) feed the shared reverb and delay.

| Control | What it does |
|---|---|
| **Lowpass** | The cloud's filter, 200 Hz – 20 kHz. |
| **Drive** | Saturation on the cloud. |
| **Reverb** | Level of a long, dark reverb. |
| **Delay** | Delay level. |
| **Delay time** | 50 ms – 1.25 s. |
| **Feedback** | How many delay repeats. |

The whole mix then passes through the stutter and a gentle compressor.

---

## 11. Presets and sharing

### Slots

| Action | How |
|---|---|
| **Load** a slot | Click a numbered button, or press **1–8**. |
| **Save** | Click **SAVE**, then a slot (or **Shift + 1–8**). |
| **Clear** a slot | Right-click it. |

Hover a slot to see what's in it and when it was saved. Slots are kept in your browser.

### Share codes

Click **SHARE** → **copy code** to copy the current setup as text. Paste a code into the box and click **load** to restore it.

### What a preset saves

| Saved | Not saved |
|---|---|
| Every knob and switch, including key, chords, cloud, beats, rack and fx settings | The master volume |
| Both LFOs | Audio samples — your own sound, loaded pad samples and chops (GRAIN reminds you if a preset used one) |
| The held chord and the 8-bar progression | |
| All 16 pad patterns and pad settings | |
| Ratchets, gate and stutter lanes | |
| Rack cables, amounts and step-CV values | |
| The lock-to-loop variation | |

### Mutate all

**⚄ MUTATE ALL** (or **R**) randomizes the key, scale, cloud, texture, pitch, fx and LFO settings, and makes a new chord. It leaves the beats alone.

---

## 12. Keyboard shortcuts

| Key | Action |
|---|---|
| **Space** | Start or stop the cloud |
| **Enter** | Start or stop the beats |
| **F** | Freeze on/off |
| **G** | New chord (into the current bar when locked) |
| **R** | Mutate all |
| **T** (hold) | Stutter the whole mix |
| **1–8** | Load preset slot |
| **Shift + 1–8** | Save to preset slot |
| **Z X C V / A S D F / Q W E R / 1 2 3 4** | Play pads 1–16 (beats tab only; **Shift** = accent) |
| **Arrow keys** | Adjust the focused knob |

> While the beats tab is open, **1–4**, **R** and **F** play pads instead of their normal jobs. Switch tabs, or use the buttons, to load presets 1–4, mutate or freeze.

---

## 13. Recipes

### Frozen pad with moving chords
1. On the cloud tab, set grain size to about 200 ms, spray low and density medium.
2. Press **F** to freeze on a spot you like.
3. On the pitch tab, turn on **lock to beat** and press **Enter**.

The texture holds still while the chords change every bar.

### A rhythmic 8-bar loop
1. Start the beats (**Enter**).
2. On the cloud tab, turn on **lock to loop** and set the grid to **1/16**.
3. On the pitch tab, turn on **lock to beat**.
4. Press **re-roll** until you like the variation, then save it to a slot.

### Chop your own sample and sequence three slices
1. Drop your file on the cloud.
2. Freeze on the part you want and press **chop around playhead**.
3. Press **clear all**, then give your three chops a step each.
4. Press **keep used chops**. The other pads go back to drums.
5. Use **swap with…** to move the chops off the kick, rim or shaker slots, then **reset** those slots.

### Avoid the "chipmunk" sound
- Lower **transpose** (−12 is a good start).
- Turn **scatter** down to 0–10%.
- Keep chord notes around C4 and below.
- Or set **pitch** to **fixed pitch**, with transpose 0 and scatter 0, for the source's natural pitch.

### Plucked, rhythmic cloud
1. On the rack, turn the **VCA** on and set the ADSR to attack ≈ 5 ms, decay ≈ 150 ms, sustain 0 and release ≈ 100 ms.
2. Light a few steps in the **cloud gate** lane.
3. Patch **env → size** at around +40 so grains open up on each hit.

### End-of-bar fills
- Light step 16 in the **stutter** lane with repeat set to 1/32.
- Give the snare a **×3** ratchet on step 15.

### Evolving filter and melody
- Patch **step → cutoff**, and draw a shape with the 8 sliders.
- Patch **rnd → pitch** with the amount at about +10 for small melodic jumps, and **slew** at about 50% for glides.

---

## 14. Troubleshooting

| Problem | Fix |
|---|---|
| **No sound** | Click **ENTER THE CLOUD**, **▶ CLOUD** or **▶ BEATS**. Check the master volume, the cloud **level**, the **grain** switch and **beat level**. |
| **Cloud is silent while the beats play** | The **VCA** is on and the gate lane is empty, or sustain is 0 with no triggers. Light some gate steps or turn the VCA off. |
| **The playhead moves when frozen** | Freeze holds the scan, LFOs and rack cables, so only dragging the cloud or turning the **position** knob can move it. Check you aren't touching either, or turn freeze off and on again (**F**). |
| **Notes sound too high** | See *Avoid the "chipmunk" sound* above. Also check for LFO or rack cables going to **pitch**. |
| **Keys 1–4 play pads instead of loading presets** | That happens on the beats tab. Switch tabs or click the slot buttons. |
| **Rack modules do nothing** | Most modules are clocked by the beat. Start the beats with **Enter**. |
| **A loaded preset says it used a sound** | Samples aren't saved in presets. Load the same file again. |
| **"Browser storage blocked"** | Your browser is blocking storage. Presets and samples then last only until the page closes. |
| **A file won't load** | Use WAV or MP3. The cloud takes files up to 40 MB and uses the first 60 seconds; pads take files up to 20 MB. |

---

## 15. Reference: ranges and limits

| Setting | Range |
|---|---|
| Grain size | 10 – 500 ms |
| Density | 2 – 120 grains/s |
| Transpose (cloud) | ±24 semitones (grains are limited to ±36 overall) |
| Tempo | 60 – 180 BPM |
| Swing | 0 – 60% |
| Pad tune | ±24 semitones |
| ADSR times | 2 ms – 4 s |
| Stutter slice | 1/4 – 1/64 note |
| LFO rate | about 0.02 Hz (one cycle every 50 s) – 12 Hz |
| Lowpass | 200 Hz – 20 kHz |
| Delay time | 50 ms – 1.25 s |
| Cloud source file | up to 40 MB; first 60 s used; leading silence trimmed |
| Pad sample file | up to 20 MB |
| Held notes | up to 8 |
| Preset slots | 8 |
| Chord sequence | 8 bars, one chord per bar |
| Loop length (lock to loop) | 8 bars (128 sixteenth steps) |
