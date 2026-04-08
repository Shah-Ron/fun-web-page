# 🚀 MAGIQ Launchpad: The "Arcade" Edition

A sleek, modern enterprise launchpad that secretly doubles as a complex, state-managed browser game. 

**The Story:** I was tasked with building a clean, professional launchpad for our team's daily tools. I did that... but I also got a little carried away and built a custom physics engine, an evasion mechanic, an idle-timer API, and a rubber-band AI Tic-Tac-Toe boss battle. Management decided the "professional" version was a better fit for the office, so this glorious, chaotic masterpiece lives here in its full glory!

## ✨ Features

### 🖥️ The Core UI
* **Glass-Morphism Design:** Clean, modern tiles with soft shadows and animated dropdown descriptions.
* **Smart Theme Toggling:** A custom Light/Dark mode switch that checks the user's system preferences (`prefers-color-scheme`) on load and saves their choice via `localStorage`.
* **Staggered Animations:** CSS keyframes are used to create a smooth, staggered entrance for the central tiles when the page loads.

### 🏃‍♂️ The "Pet" Engine (JavaScript)
* **Custom Wandering Physics:** A digital pet (GIF) continuously calculates random `(x, y)` coordinates within the window bounds and travels to them using dynamically injected CSS transitions.
* **Directional Awareness:** The script calculates the vector of the next move and applies a 3D `rotateY()` transform so the GIF always faces the direction it's running.
* **Idle System:** If the user doesn't interact with the page for a set amount of time, a `setTimeout` loop triggers the pet to share a random fun fact via a glass-morphism speech bubble.
* **Contextual Data:** The fun facts are theme-aware! Light mode shares local trivia about Central Otago, NZ. Dark mode shares deep-cut Batman lore.

### 🎮 The Chase Mechanics & Boss Battles
* **Evasion:** When the user attempts to hover or click the pet, it aborts its current path, calculates a new random location, and sprints away at high speed.
* **The HUD:** A real-time tracker counts your "misses" and pulses in the corner of the screen.
* **Tic-Tac-Toe Interception:** Every 50 missed attempts, the pet stops, and an inline Tic-Tac-Toe board slides out. 
* **"Smart but Fallible" AI:** The Tic-Tac-Toe AI uses a priority checklist (Win > Block > Center > Random). However, to prevent it from being unbeatable, every 5th game triggers a "dumb" mode where the AI intentionally makes random moves, giving the player a chance to win.
* **Progressive Fatigue Math:** If the player wins the mini-game, the pet's base evasion speed permanently drops by a mathematical factor. If they lose, the pet mocks them and maintains its high speed.

## 🛠️ Tech Stack
* **HTML5:** Semantic structure and layout.
* **CSS3:** Heavy use of CSS Grid, Flexbox, Keyframe Animations, Backdrop Filters (Glass-morphism), and CSS Variables for theme management.
* **Vanilla JavaScript:** 100% pure JS. No external libraries or frameworks. Handled DOM manipulation, event bubbling, state management, and math logic.

## 🚀 How to Run
There is no build step or package manager required.
1. Clone this repository.
2. Ensure you have the required images (the logo and the two GIFs) in the same directory.
3. Open `index.html` in your favorite web browser.
4. Try to click the GIF. I dare you.

## 💡 What I Learned
Building this was an incredible deep dive into Vanilla JavaScript. I learned how to manage complex `setTimeout` loops without memory leaks, how to calculate distance/speed for dynamic CSS transitions, how to prevent Event Bubbling when nesting interactive elements, and how to build a priority-based AI for a classic grid game.

---
*Built with logic, math, and just a little bit of spite for boring UI.*
