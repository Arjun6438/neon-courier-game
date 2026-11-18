# Neon Courier â€” Game Design Document

## 1. Overview
**Title:** Neon Courier  
**Genre:** 2D arcade action / collection game  
**Platform:** Web browser  
**Target audience:** Casual players and beginners learning game development  
**Core experience:** Move through a neon arena, collect energy cores, avoid patrol drones, and reach the exit before time expires.

## 2. Game Objective
The player controls a courier drone. The goal is to collect all five energy cores and then reach the cyan exit portal. The player has 60 seconds. Touching a red security drone or allowing the timer to reach zero causes a loss.

## 3. Core Gameplay Loop
1. Start the mission with 60 seconds.
2. Explore the arena using keyboard or touch controls.
3. Collect five gold energy cores.
4. Avoid moving red security drones.
5. Reach the exit after all cores are collected.
6. Earn points for cores and receive a time bonus for completing the mission quickly.

## 4. Controls
- **Arrow keys or WASD:** Move the courier.
- **Mobile controls:** On-screen directional buttons.
- **Restart button:** Reset the mission.

## 5. Game Rules and Scoring
- Each energy core: **100 points**.
- Completion bonus: **10 points for every second remaining**.
- The exit remains inactive until all cores are collected.
- Collision with a security drone ends the game.
- The game ends when the timer reaches zero.

## 6. Entities
| Entity | Description |
|---|---|
| Courier | Blue player character controlled by the user |
| Energy core | Gold collectible; five are placed in the arena |
| Security drone | Red moving hazard; collision causes failure |
| Exit portal | Cyan destination; activates after all cores are collected |

## 7. Visual and Audio Direction
The prototype uses a dark navy sci-fi arena with cyan, gold, and pink accents. The visual language communicates the game state clearly: gold indicates objectives, red indicates danger, and cyan indicates the player and successful exit. Audio can be added in a future iteration with a collection sound, warning sound, and completion theme.

## 8. Level Design
The first level is a single-screen arena. Collectibles are distributed across corners and central areas so the player must move through the whole map. Drones patrol horizontally and vertically, creating timing challenges without making the prototype too difficult.

## 9. Technical Implementation
- HTML5 Canvas for rendering.
- JavaScript for game state, input, collision detection, timer, scoring, and animation.
- Responsive layout for desktop and mobile browsers.
- No external libraries or installation required.

## 10. Success Criteria
The prototype is successful when:
- The player can move in four directions.
- Five collectibles can be collected.
- Drones move continuously.
- Collision and timer failure states work.
- The exit activates only after all collectibles are obtained.
- A successful completion screen and score are shown.
- The game works in a modern browser.

## 11. Future Improvements
- Add sound effects and background music.
- Add multiple levels with different maps.
- Add walls and obstacles.
- Add a difficulty selector.
- Save best score using browser local storage.
- Add a title screen and tutorial.
- Add more enemy types and power-ups.

## 12. Proof of Work
**Playable prototype:** `neon-courier-playable-prototype.html`  
Open the HTML file in a browser to play. For submission, upload this file and this design document to a public GitHub repository or public Google Drive folder, then submit that shareable link on Edvyro.


## Milestone 3: Game State, Progression, and Persistence

The prototype now includes a complete game-state system with start, playing, paused, transition, game-over, and victory states. Players can start, pause, resume, restart, and complete the game through the interface or keyboard controls.

The game includes three progressive levels. Each level increases the number of energy cores, adds more security drones, increases enemy speed, and reduces the available time. After completing a level, the player automatically advances to the next level. The final level produces a complete victory state.

A scoring system awards points for collecting cores and provides a time bonus for finishing levels quickly. The highest score is stored in the browser using `localStorage`, so it remains available after refreshing the page. The highest unlocked level is also saved and can be used as evidence of progression and persistence.

### Milestone 3 Checklist

- Start state and start button implemented.
- Active gameplay state implemented.
- Pause and resume state implemented.
- Game-over state implemented for collisions and timeout.
- Victory state implemented after completing all levels.
- Three-level progression implemented.
- Increasing enemy count and speed implemented.
- Score and time bonus implemented.
- Best score saved with `localStorage`.
- Highest unlocked level saved with `localStorage`.
- Restart functionality implemented.