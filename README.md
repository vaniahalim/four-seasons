# Four Seasons

Four seasons you play with using your webcam and breath, in a single HTML file.

Leaves, petals, snow and dandelion seeds drift across your camera. You move them with your hands and your breath, using only your webcam and microphone. Nothing is uploaded, and the app plays no sound.

## Seasons

Pick one on the start screen, or switch while playing with the buttons at the bottom or keys `1`–`4`. The page opens on the current season, and `#spring`, `#summer`, `#autumn` or `#winter` on the URL picks one directly.

| Season | What it does |
|---|---|
| Spring | Blossom petals fall. Hold a palm open and flowers rise from the ground toward it. Blow on a flower and it loses its petals one at a time. |
| Summer | Golden hour on a trail. Dandelion seeds drift past and butterflies wander. Butterflies land on an open palm, and fireflies gather around a hand that holds still. |
| Autumn | Leaves fall and pile up. Catch them, throw them, sweep the floor. |
| Winter | Snow falls and builds up. Your breath fogs the glass. Pinch with no flake in reach to draw in the fog, and frost grows where it stays thick. |

## Controls

| Action | What it does |
|---|---|
| Open palm | Catches leaves (up to 18 rest on your palm) |
| Pinch | Picks up and holds a single leaf |
| Fist | Sweeps leaves aside |
| Blow toward the screen | Sends a gust from your mouth |
| Hold Space | Gust (or breath, in winter) without a microphone |
| `C` | Clear the floor (also flowers, fog and frost) |
| `S` | Save a picture |
| `Esc` | Back to the start screen |

The microphone is used only to detect breath. Nothing is recorded or played.

## Run it

There is no build step. Serve the folder and open the page:

```sh
python3 -m http.server 8765
```

Then open <http://localhost:8765/four-seasons.html> in a recent Chrome and allow camera and microphone access.

Browsers only allow camera and microphone access on `localhost` or HTTPS, so opening the file directly from disk will not work.

## How it works

- Hand and face tracking use [MediaPipe](https://developers.google.com/mediapipe) (Hands and Face Detection), loaded from jsDelivr and run entirely on your device.
- The scene is drawn on a single canvas.
- Each season has its own sprites, colour grade and behavior, all in the same file.
- Fonts are Young Serif and Hanken Grotesk from Google Fonts.

## Files

- `four-seasons.html`: the whole app
