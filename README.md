# TypeRush — Typing Speed Test

A single-file, interactive typing speed test web app. No frameworks, no build step, no external dependencies — just open it in a browser.

## Features

- **Dark, modern UI** built with plain CSS
- **Real-time stats**: countdown timer, WPM, and accuracy update live while you type
- **30-second timer** that starts automatically on your first keystroke
- **Character-level feedback**: correct characters turn green, wrong ones turn red
- **Results screen** at the end showing WPM, accuracy, and total characters typed correctly/incorrectly
- **Restart** available any time via the header button or the "Try Again" button on the results screen
- Backspace is supported and does not count against you

## How to Run

No installation needed. Either:

1. Open `index.html` directly in any modern browser, or
2. Serve it with any static file server, e.g.:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## How Scoring Works

- **WPM** = (characters typed ÷ 5) ÷ minutes elapsed — the standard gross-WPM formula (5 characters = 1 "word").
- **Accuracy** = (correct keystrokes ÷ total keystrokes) × 100%, tracking every key you press, including corrections.
- The test ends when 30 seconds have elapsed **or** you finish the paragraph, whichever comes first.

## Project Structure

```
.
├── index.html   # The entire app (HTML + CSS + JS)
├── README.md
└── .gitignore
```

## Browser Support

Any modern browser (Chrome, Firefox, Safari, Edge). Uses only standard DOM APIs and `requestAnimationFrame`.
