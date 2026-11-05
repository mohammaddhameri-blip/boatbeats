# BoatBeats v1.3

A responsive single-file rhythm-powered boat racing game for phones, tablets, laptops and smartboards.

## Quick start

1. Open `index.html` in a browser for the tap-to-test version.
2. Open **Settings** (gear icon) to choose your crew size, difficulty, input and rival boat speed. The rival slider defaults to a slower 1.8 pace and remembers your selection.
3. Press **🏁 BEGIN RACE** on the river racing screen.
4. Follow the audible drums and musical notation on the staff. Clap or tap at the indicated times. Correctly clapped notes turn green; missed notes turn red; notes played in the listening demonstration turn blue. Better accuracy increases speed; missed notes slow you down.
5. Each rhythm plays **five times**: the first bar is a listening-only demonstration, followed by four scored clapping bars. During the listening bar the boat accelerates automatically by the equivalent of four correctly clapped crotchet beats; listening does not affect accuracy or missed notes. After five bars, the next pattern starts automatically.

## Microphone mode

On an actual phone or classroom device, the most reliable way to use the microphone is to serve the `index.html` file on an **HTTPS** website (for example GitHub Pages) or `http://localhost` for local testing. Grant microphone permission when requested. The default device microphone is used automatically.

Headphones are recommended: without them, game audio played by the device's speakers may be detected as a percussion hit. You may need to change the Timing offset slightly to compensate for a device's audio latency.

The game detects sharp percussive sound onsets and measures *rhythmic timing*. It does not classify instrument types, estimate each participant's individual clap or count people through the microphone. Crew size is entered manually, multiplying the boost awarded for synchronized hits.

## Modes

- **Mic**: clap, use a DIY drum or tap a desk; detection uses live device audio and an adaptive onset threshold.
- **Tap to test**: use the big drum button or Spacebar (no mic required).
- **Easy**: four simple rhythmic variations, 92 BPM, using crotchets, minims and quavers.
- **Medium**: four mixed off-beat patterns, 106 BPM, introducing semiquavers.
- **Hard**: four faster syncopated patterns, 116 BPM, with more frequent quavers and semiquavers.

## Music notation and race settings

Rhythms are genuine 4/4 bars built from minim (2 beats), crotchet (1 beat), quaver (1/2 beat), and semiquaver (1/4 beat) durations. Each note is drawn as an SVG staff symbol rather than a flashing beat square. The number at the bottom marks each of the four beats. The default rival speed can be changed using the Settings slider from 0.4 to 5.0 pace. Settings are accessible during a race and suspend/resume play while open.

## Technical details

- No third-party scripts, images, trackers, frameworks or dependencies.
- All drum sounds are synthesized with the Web Audio API.
- HTML/CSS/JavaScript, no backend required.
- The browser needs microphone permission only when microphone mode is selected.
- This is a first playable prototype. Microphone sensitivity, input delay and speaker feedback must be tested on target Android devices.

## Deploy to GitHub Pages

Create a repository, put `index.html` at its root, then enable GitHub Pages for the main branch root in repository Settings > Pages. Open the Pages HTTPS URL on the device and grant mic permission.
