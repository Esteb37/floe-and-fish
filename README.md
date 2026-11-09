# Floe & Fish

A typing game for practicing the US QWERTY layout. Fish fall toward the sea, each one carrying a key or a word. Type it and the seal on the ice floe catches the fish. If five fish reach the water, the round ends. Each wave falls faster than the last.

The keyboard at the bottom of the screen colors every key by the finger that should press it. It also lights up the next key you need, plus the correct Shift key for capitals and symbols.

## Lessons

- **Keys:** home row, home row + G H, top row, bottom row, all letters, number row, capitals, symbols
- **Words:** home row words, top + home row words, common words, polar words

Turn on **Calm water** in the menu if you want a round with no lives, for learning new keys without pressure.

## Running it locally

There is nothing to build or install. The whole game is one file, `index.html`, written in plain HTML, CSS and JavaScript with no dependencies.

### Option 1: open the file

**Linux**

```sh
git clone <repo-url> floe-and-fish
cd floe-and-fish
xdg-open index.html
```

**macOS**

```sh
git clone <repo-url> floe-and-fish
cd floe-and-fish
open index.html
```

You can also double-click `index.html` in your file manager.

### Option 2: serve it over HTTP

Some browsers limit pages opened from `file://`. If anything misbehaves, serve the folder instead. Python 3 comes with macOS (or arrives with the Xcode Command Line Tools) and with most Linux distributions:

```sh
cd floe-and-fish
python3 -m http.server 8000
```

Then open <http://localhost:8000> in your browser. Press `Ctrl+C` in the terminal to stop the server.

## Controls

| Key | Action |
| --- | --- |
| Any character | Catch the fish carrying that key, or type the next letter of a word |
| `Backspace` | In word lessons, let go of the word you started |
| `Esc` | Pause or resume |
| `Enter` | Start the last lesson from the menu, resume, or play again |

## Notes

- The fonts load from Google Fonts. Without an internet connection the game still works but uses your system fonts.
- Best scores and settings are saved in your browser's local storage. Calm water rounds don't count toward best scores.
- To change how fast the first wave starts, edit `SPEED_HEAD_START` in `index.html`. Lower numbers give a gentler start, and `0` gives the slowest one.
