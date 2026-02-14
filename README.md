Pixelated Arcade
Pixelated Arcade is a single‑page mini game collection built with plain HTML, CSS, and JavaScript. It’s designed as a fun, lightweight demo project to showcase simple game logic, UI styling, and basic state management in the browser.

Features
8 mini games in one HTML file:

Click the Square

Reaction Timer

Number Guess

Avoid the Dots

Type the Word (coding terms)

Clicker (with ripple effect)

Color Guess

Tic‑Tac‑Toe

Space‑themed UI with neon‑style panels and buttons.

Per‑game stopwatch in the header:

Only runs when that game has active gameplay.

Resets when you restart or leave the game.

Central translucent “Restart game” overlay:

Appears at the end of certain games (for example after losing or finishing a round).

Restarts only the currently active game.

All logic is client‑side, no frameworks or build tools required.

Games Overview
Click the Square
Click the moving square as many times as possible before the 30‑second timer ends.

Reaction Timer
Click to arm the game, wait for the box to turn green, then click as fast as you can and compare your reaction time.

Number Guess
Guess a random number between 1 and 20; the game tells you if you’re too high or too low until you get it right.

Avoid the Dots
Move the green circle with your mouse and avoid red dots that home in on you; survive as long as possible.

Type the Word
Quickly type coding‑related words (languages, concepts, tools) shown on screen and increase your score.

Clicker
Click the button to increase your count and enjoy a ripple/light‑up effect from the click location; use the overlay to restart.

Color Guess
A colored box is shown; type the color name (e.g., “red”, “cyan”) and press Guess. The input must be filled before guessing.

Tic‑Tac‑Toe
Classic 3×3 grid, local two‑player (X vs O). The stopwatch tracks how long a round takes.

Getting Started
Clone or download this repository.

Open index.html in your browser (double‑click or File → Open).

Use the buttons at the top to switch between games.

Use the “Restart game” overlay when it appears to reset the active game.

Project Structure
index.html
Contains:

All HTML markup for the 8 games.

Embedded CSS for layout, space background, and effects.

Embedded JavaScript for game logic, per‑game reset, and stopwatch handling.

You can easily split the CSS and JS into separate files later (style.css, script.js) if you want a more production‑style structure.

How It Works (High Level)
Each game has:

Its own DOM elements.

A small self‑contained script block.

A reset function registered in a shared map.

When you switch games:

The current game’s reset function is called.

Its stopwatch is cleared.

The new game is shown in the main container.

A single animation loop updates homing enemies and the stopwatch (using requestAnimationFrame and performance.now()).
