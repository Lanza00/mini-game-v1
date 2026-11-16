# 🎩 Wonderland – Letak Betul-Betul!

A fun, party-style mini game for groups, set in Alice in Wonderland. One player puts a missing item (a hat, a tail, a crown) back on a character **without looking at the screen**, while their team guides them with spoken directions: *kiri / kanan / atas / bawah*.

The whole game is a single self-contained HTML file. There's no build step, no dependencies, and no server needed.

## 🎮 How to Play

1. Open the game and enter a name for each of the 3 teams.
2. Adjust the mouse sensitivity if needed.
3. Each turn, one player sits with their back to the screen (**no peeking at the TV!**).
4. The team shouts directions so the player can move the item to the marked spot.
5. Click to place the item. The closer and faster, the better.
6. After all rounds, the team with the **shortest total time** wins.

### Characters

| Character | Item to place |
|-----------|---------------|
| Mad Hatter | Hat (*topi*) |
| Cheshire Cat | Tail (*ekor*) |
| Queen of Hearts | Crown (*mahkota*) |

### Rules at a glance

- 3 teams, 3 rounds each
- 60-second time limit per turn
- Placing the item on the character's body adds a time penalty (25 s per body hit)
- Lowest total time wins

## ⌨️ Controls

| Input | Action |
|-------|--------|
| Mouse move | Move the item (pointer lock) |
| Left click | Place the item |
| `Space` / `Enter` | Start, continue, or play again |
| `R` | Redo the current turn (on the result screen) |
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
- Team names and sensitivity are saved in `localStorage`

## ⚙️ Customising

Game settings are constants near the top of the script in `wonderland-game.html`:

```js
const ROUNDS = 3, TEAMS = 3, TIME_LIMIT = 60, PEN_PER_BODY = 25, TOL = 0.04;
```

| Constant | Meaning |
|----------|---------|
| `ROUNDS` | Rounds per team |
| `TEAMS` | Number of teams |
| `TIME_LIMIT` | Seconds allowed per turn |
| `PEN_PER_BODY` | Penalty for placing on the body |
| `TOL` | Placement tolerance |

## 📁 Project Structure

```
mini-game-v1/
├── wonderland-game.html   # The entire game
└── README.md
```

## 📄 License

No license has been chosen yet. Add a `LICENSE` file (for example MIT) if you want others to reuse the game.
