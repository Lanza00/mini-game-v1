# 🎩 Wonderland – Letak Betul-Betul!

A fun, party-style mini game set in Alice in Wonderland. One player puts a missing item (a hat, a tail, a crown...) back on a character **without looking at the screen**, while their team guides them with spoken directions: *kiri / kanan / atas / bawah*.

The whole game is a single self-contained HTML file. There's no build step, no dependencies, and no server needed.

## 🎮 How to Play

1. Open the game and enter your team name.
2. Adjust the mouse sensitivity if needed, then press **Mula Game**.
3. Each game picks **3 random characters** out of 5.
4. For every round, one player sits with their back to the screen (**no peeking at the TV!**).
5. The team shouts directions so the player can move the item to the marked spot.
6. Click to place the item. The closer and faster, the better.
7. After 3 rounds you get your total time. **Lower is better.**

### Characters

| Character | Item to place |
|-----------|---------------|
| Mad Hatter | Hat (*topi*) |
| Cheshire Cat | Tail (*ekor*) |
| Queen of Hearts | Crown (*mahkota*) |
| White Rabbit | Pocket watch (*jam poket*) |
| March Hare | Tie (*tali leher*) |

### Scoring

```
round score = time taken + distance penalty
```

- **Time:** seconds from "GO!" until you click, capped at 60 s. When the time runs out the item is placed automatically.
- **Distance penalty:** if the item lands outside the target tolerance, extra seconds are added the further away it is. A perfect placement has no penalty.
- **Feedback after each round:**
  - 🎯 *Tepat sangat!* means a perfect placement
  - *Dekat dah!* means close
  - *Jauh lagi…* means far off
- Don't like a round? Press `R` to redo that turn.

## ⌨️ Controls

| Input | Action |
|-------|--------|
| Mouse move | Move the item (pointer lock) |
| Left click | Place the item |
| `Space` / `Enter` | Start, continue, or play again |
| `R` | Redo the current round (on the result screen) |
| `F` | Toggle fullscreen |

## 🚀 Run It

**Option 1: open the file**

Double-click `wonderland-game.html`. It runs in any modern browser.

**Option 2: local server (Laragon/XAMPP)**

```
http://localhost/mini-game-v1/wonderland-game.html
```

**Option 3: GitHub Pages**

Enable Pages in the repo settings (branch `main`, root folder), then visit:

```
https://lanza00.github.io/mini-game-v1/wonderland-game.html
```

> 💡 Best on a laptop connected to a TV or projector, so the team can see the screen while the player can't.

## 🛠️ Tech

- Plain HTML, CSS and JavaScript
- HTML5 Canvas for rendering
- Web Audio API for sound effects
- Pointer Lock API for mouse control
- Images embedded as base64, so everything lives in one file
- Team name and mouse sensitivity are saved in `localStorage`

## ⚙️ Customising

Game settings are constants near the top of the script in `wonderland-game.html`:

```js
const ROUNDS = 3, TEAMS = 1, TIME_LIMIT = 60, PEN_PER_BODY = 25, TOL = 0.04;
```

| Constant | Meaning |
|----------|---------|
| `ROUNDS` | Number of rounds per game (random characters picked from the 5 above) |
| `TEAMS` | Number of teams (currently 1) |
| `TIME_LIMIT` | Max seconds per round |
| `PEN_PER_BODY` | Penalty scale for distance from the target |
| `TOL` | Placement tolerance with no penalty |

To add a character, add its images to `DATA` and an entry to `META` (name, item, start position).

## 📁 Project Structure

```
mini-game-v1/
├── wonderland-game.html   # The entire game
└── README.md
```

## 📄 License

No license has been chosen yet. Add a `LICENSE` file (for example MIT) if you want others to reuse the game.
