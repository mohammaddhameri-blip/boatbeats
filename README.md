# BoatBeats v1.2

A responsive single-file rhythm-powered boat racing game for phones, tablets, laptops and smartboards.

## Quick start

1. Open `index.html` in a browser for the tap-to-test version.
2. Select crew size, difficulty and input type.
3. Press **START RACE**.
4. Follow the audible drums and highlighted beat boxes. Clap or tap at the indicated times. Better beat accuracy adds more speed; missed beats slow you down.
5. Each drum rhythm plays for **four full repetitions (four bars)**, then the next pattern starts automatically. The beat boxes and `P1 · 1/4` progress indicator update at the exact new bar. Four patterns rotate within the chosen difficulty.

## Microphone mode

On an actual phone or classroom device, the most reliable way to use the microphone is to serve the `index.html` file on an **HTTPS** website (for example GitHub Pages) or `http://localhost` for local testing. Grant microphone permission when requested. The default device microphone is used automatically.

Headphones are recommended: without them, game audio played by the device's speakers may be detected as a percussion hit. You may need to change the Timing offset slightly to compensate for a device's audio latency.

The game detects sharp percussive sound onsets and measures *rhythmic timing*. It does not classify instrument types, estimate each participant's individual clap or count people through the microphone. Crew size is entered manually, multiplying the boost awarded for synchronized hits.

## Modes

- **Mic**: clap, use a DIY drum or tap a desk; detection uses live device audio and an adaptive onset threshold.
- **Tap to test**: use the big drum button or Spacebar (no mic required).
- **Easy**: four simple rhythmic variations, 92 BPM.
- **Medium**: four mixed off-beat patterns, 106 BPM.
- **Hard**: four faster syncopated patterns, 116 BPM.

## Technical details

- No third-party scripts, images, trackers, frameworks or dependencies.
- All drum sounds are synthesized with the Web Audio API.
- HTML/CSS/JavaScript, no backend required.
- The browser needs microphone permission only when microphone mode is selected.
- This is a first playable prototype. Microphone sensitivity, input delay and speaker feedback must be tested on target Android devices.

## Deploy to GitHub Pages

Create a repository, put `index.html` at its root, then enable GitHub Pages for the main branch root in repository Settings > Pages. Open the Pages HTTPS URL on the device and grant mic permission.
