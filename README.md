# Windfall

Autumn leaves you play with using your webcam and breath, in a single HTML file.

Leaves drift down the screen. You move them with your hands and your breath, using only your webcam and microphone. Nothing is uploaded, and the app plays no sound.

## Controls

| Action | What it does |
|---|---|
| Open palm | Catches leaves (up to 18 rest on your palm) |
| Pinch | Picks up and holds a single leaf |
| Fist | Sweeps leaves aside |
| Blow toward the screen | Sends a gust from your mouth |
| Hold Space | Gust without a microphone |

The microphone is used only to detect breath. Nothing is recorded or played.

## Run it

There is no build step. Serve the folder and open the page:

```sh
python3 -m http.server 8765
```

Then open <http://localhost:8765/windfall.html> in a recent Chrome and allow camera and microphone access.

Browsers only allow camera and microphone access on `localhost` or HTTPS, so opening the file directly from disk will not work.

## How it works

- Hand and face tracking use [MediaPipe](https://developers.google.com/mediapipe) (Hands and Face Detection), loaded from jsDelivr and run entirely on your device.
- The scene is drawn on a single canvas.
- Fonts are Young Serif and Hanken Grotesk from Google Fonts.

## Files

- `windfall.html`: the whole app
