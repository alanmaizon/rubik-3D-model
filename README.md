# Rubik Bass

An interactive 4x4 Rubik's Cube audiovisual sequencer built with Three.js and Tone.js.

## About The Project

Rubik Bass is a unique web-based musical instrument that transforms a fully interactive 4x4 Rubik's Cube into a 16-step arpeggio sequencer. The colors on the face of the cube directly map to musical notes, creating a dynamic and visually engaging way to compose music.

What started as a simple 3D model has evolved into a feature-rich creative tool with controls for tempo, note muting, and cube manipulation, all wrapped in a modern, responsive interface.

## Features

  * **Interactive 4x4 Rubik's Cube:** A fully functional 4x4 cube that can be rotated and scrambled.
  * **Complete Rotational Control:** Use the UI to rotate all 12 slices (outer faces and inner slices) clockwise or counter-clockwise.
  * **Audiovisual Sequencer:** The 16 colors on the front face are read in real-time to create a looping 16-note arpeggio.
  * **Custom Audio Samples:** Uses `Tone.Sampler` to allow any `.wav` or `.mp3` files to be used for the notes, giving the instrument a unique sound.
  * **Interactive Muting:** Click or tap directly on any sticker on the cube to toggle its corresponding note on or off in the sequence.
  * **Real-time Tempo Control:** A BPM (Beats Per Minute) input allows for precise control over the sequencer's tempo.
  * **Note Length Switch:** A dedicated switch to toggle note lengths, allowing for rhythmic variation between standard and short, *staccato* notes.
  * **Master Controls:** Includes "Mute All," "Unmute All," "Reset Cube" to its solved state, and "Scramble" for instant randomization.
  * **Visual Feedback:** Each sticker emits a "halo" of light in sync with its note being played in the sequence, and muted stickers are visually dimmed.
  * **Responsive Collapsible UI:** All controls are housed in a sleek, collapsible side menu that works on both desktop and mobile devices.
  * **Mobile Touch Support:** Carefully designed touch handling to differentiate between rotating the cube (dragging) and muting a sticker (tapping).

## Getting Started

To get a local copy up and running, follow these simple steps.

### Prerequisites

You only need a modern web browser that supports ES6 Modules (like Chrome, Firefox, Edge, or Safari). No complex build tools are required.

### Installation

1.  **Get the Code:**
    Download or clone the project files (`index.html`, `script.js`) into a folder on your computer.

2.  **Add Your Audio Samples:**
    Place your six `.wav` audio sample files in the same root folder. The script is currently configured to look for these specific filenames:

      * `white.wav`
      * `red.wav`
      * `blue.wav`
      * `orange.wav`
      * `green.wav`
      * `yellow.wav`

3.  **Update File Paths (If Necessary):**
    If your audio files have different names, open `script.js` and update the `synthSamples` object accordingly:

    ```javascript
    const synthSamples = { 
        'C4': 'your_white_note.wav', 
        'D4': 'your_red_note.wav',
        // etc...
    };
    ```

4.  **Run a Local Server:**
    For security reasons (CORS policy), browsers cannot load local files (like your audio samples) directly. You need to serve the files from a simple local server.

      * If you have Python installed, navigate to your project folder in the terminal and run: `python -m http.server`
      * If you have Node.js, you can install a simple server: `npm install -g live-server` and then run `live-server` in your project folder.
      * You can also use the "Go Live" feature in VS Code's Live Server extension.

5.  **Open the Project:**
    Open your web browser and navigate to the local server address (usually `http://localhost:8000` or `http://127.0.0.1:8080`).

## How to Use

  * **Rotate the Cube:** Click and drag (or use touch) on the cube to rotate your view.
  * **Open the Controls:** Click the **MENU** tab on the right side of the screen to slide out the control panel.
  * **Turn Faces:** Use the `U`, `L`, `R`, `D` buttons for outer face turns and `u`, `l`, `r` for inner slice turns. The apostrophe (') indicates a counter-clockwise turn.
  * **Control the Sequencer:**
      * Use the **BPM** input to set the tempo.
      * Click the **"Half Note Length"** checkbox to toggle between short and long notes.
      * Press **Play/Stop** to start or stop the arpeggio.
  * **Mute Notes:** Click (or tap) directly on any colored sticker on the cube's surface to mute or unmute its note in the sequence.
  * **Master Controls:** Use "Mute All," "Unmute All," "Reset Cube," and "Scramble" for global actions.

## Technologies Used

  * **JavaScript (ES6 Modules)**
  * **Three.js:** For all 3D rendering and interaction.
  * **Tone.js:** For all audio synthesis, sequencing, and timing.

It's been a pleasure building this incredible project with help of Gemini 2.5
