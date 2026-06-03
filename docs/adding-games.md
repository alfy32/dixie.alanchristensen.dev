# Adding a Game

Each game lives in its own folder under `games/` and is linked from the main page (`index.html`).

## File Structure

```
games/
  <game-name>/
    index.html    — The game's page
    (any other assets: JS, CSS, images, etc.)
```

Use a short, lowercase, hyphenated name for the folder (e.g. `word-search`, `color-match`).

## Step 1 — Create the game page

Create `games/<game-name>/index.html`. At minimum it should:

- Have a page title and heading with the game's name
- Include a link back to the main page (`<a href="/">← Back</a>`)
- Contain the game itself (inline or via linked scripts/styles in the same folder)

## Step 2 — Add it to the main page

Open `index.html` at the root of the repo. Inside the games list, add a new entry:

```html
<li>
  <a href="/games/<game-name>/">Game Title</a>
  <p>One sentence describing what the game is.</p>
</li>
```

Keep the description short — one sentence is enough for the main page.

## Step 3 — Update the README

Open `README.md` and add a row to the Games table:

```markdown
| [Game Title](/games/<game-name>/) | One sentence description. |
```

## Example

Adding a game called "Color Match":

1. Create `games/color-match/index.html` with the game content.
2. Add to the list in `index.html`:
   ```html
   <li>
     <a href="/games/color-match/">Color Match</a>
     <p>Tap the color that matches the word before the timer runs out.</p>
   </li>
   ```
3. Add to the table in `README.md`:
   ```markdown
   | [Color Match](/games/color-match/) | Tap the color that matches the word before the timer runs out. |
   ```
4. Commit and push to `main` — GitHub Pages deploys automatically.
