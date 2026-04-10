# Sideways Tetris 🎮

> A novel twist on the classic Tetris game where pieces fall **left to right** instead of top to bottom!

[![Play Online](https://img.shields.io/badge/Play-Online-brightgreen?style=for-the-badge&logo=gamejolt)](https://rexuvia.com/games/sideways-tetris.html)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)
[![Tech Stack](https://img.shields.io/badge/Tech-Vanilla%20JS%20%2B%20HTML5%20Canvas-ff69b4?style=for-the-badge)](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API)
[![Mobile Friendly](https://img.shields.io/badge/Mobile-Friendly-success?style=for-the-badge&logo=smartphone)](https://rexuvia.com/games/sideways-tetris.html)
[![Game Status](https://img.shields.io/badge/Status-Live%20%26%20Playable-success?style=for-the-badge)](https://rexuvia.com/games/sideways-tetris.html)

## 🎯 Quick Start

**Play instantly:** [Sideways Tetris on rexuvia.com](https://rexuvia.com/games/sideways-tetris.html)

**Run locally:** Simply open `index.html` in any modern web browser!

## 🎮 Game Overview

Sideways Tetris reimagines the classic block-stacking puzzle with a 90-degree twist. Instead of gravity pulling pieces downward, they drift horizontally from left to right. Your goal: rotate and position tetrominoes to complete **vertical columns** before they stack up to the left edge.

### ✨ Key Features

- **🔄 Horizontal Gameplay:** Pieces spawn on the left and drift rightward
- **📐 Vertical Clearing:** Complete full columns instead of rows
- **🎨 Neon Aesthetic:** Vibrant cyan, magenta, and green glowing pieces
- **📱 Mobile-First Design:** Optimized touch controls for phones
- **⌨️ Desktop Controls:** Full keyboard support
- **🚀 Progressive Difficulty:** Speed increases with your score
- **💯 Advanced Scoring:** Bonus points for multi-column clears and combos
- **⏸️ Pause/Resume:** Full game state preservation

## 🎛️ Controls

### Desktop (Keyboard)
| Action | Key |
|--------|-----|
| Move Up | ↑ Arrow |
| Move Down | ↓ Arrow |
| Rotate | Space |
| Hard Drop (Instant) | → Arrow |
| Pause/Resume | P |

### Mobile (Touch)
| Action | Gesture |
|--------|---------|
| Move Up/Down | Swipe vertically |
| Rotate | Tap anywhere |
| Hard Drop | Swipe right |
| Pause/Resume | Tap pause button |

## 🧩 How It Differs from Classic Tetris

| Aspect | Classic Tetris | Sideways Tetris |
|--------|----------------|-----------------|
| **Gravity Direction** | Top → Bottom | Left → Right |
| **Movement Axis** | Horizontal (left/right) | Vertical (up/down) |
| **Clearing Target** | Horizontal Rows | Vertical Columns |
| **Game Over Condition** | Stack reaches top | Stack reaches left edge |
| **Spawn Location** | Top center | Left center |

**Core gameplay twist:** Your spatial reasoning needs to rotate 90 degrees! What was vertical thinking becomes horizontal, and vice versa.

## 🏗️ Technical Implementation

### Architecture
- **Single-file HTML:** Complete game in one self-contained `index.html` file
- **Vanilla JavaScript:** No frameworks or external dependencies
- **Canvas-based Rendering:** Direct 2D drawing API for optimal performance
- **Modular Design:** Clean separation of game logic, rendering, and input handling

### Key Components

1. **Game Engine (`Game` class)**
   - Manages game state, score, and level progression
   - Handles piece spawning, collision detection, and column clearing
   - Implements the game loop with requestAnimationFrame

2. **Board Management (`Board` class)**
   - 10×20 grid representation (rotated 90 degrees)
   - Efficient collision checking using bitwise operations
   - Column completion detection and clearing logic

3. **Piece System (`Piece` class)**
   - 7 classic tetromino shapes (I, O, T, S, Z, J, L)
   - Rotation matrices adapted for horizontal movement
   - Color-coded rendering with neon glow effects

4. **Input Handler**
   - Unified keyboard and touch input system
   - Gesture recognition for mobile swipes
   - Debounced controls to prevent input flooding

5. **Rendering Engine**
   - Canvas context management
   - Smooth animations and transitions
   - Responsive scaling for all screen sizes

### Performance Optimizations
- **Double buffering:** Minimizes canvas flicker
- **Efficient collision:** Bitwise grid operations
- **Debounced input:** Prevents control lag
- **Optimized rendering:** Only redraws changed regions

## 📸 Screenshots

*(Note: Screenshots would typically be added here. Good candidates would include:)*
1. **Gameplay screenshot** showing pieces in motion with completed columns
2. **Mobile view** demonstrating touch controls
3. **High score screen** with neon UI elements
4. **Pause menu** with clean overlay design

*To add screenshots:*
1. Take screenshots of the game in action
2. Save them in a `/screenshots` directory
3. Reference them with Markdown: `![Gameplay](/screenshots/gameplay.png)`

## 🚀 Development

### Running Locally
```bash
# Clone the repository
git clone https://github.com/rexuvia/sideways-tetris.git

# Navigate to project
cd sideways-tetris

# Open in browser (any of these)
open index.html        # macOS
xdg-open index.html    # Linux
start index.html       # Windows
```

Or simply double-click `index.html` in your file explorer!

### Project Structure
```
sideways-tetris/
├── index.html          # Main game file (self-contained)
├── README.md           # This documentation
└── (optional screenshots directory)
```

### Contributing
We welcome contributions! Here's how:

1. **Fork** the repository
2. **Create a feature branch:** `git checkout -b feature/amazing-feature`
3. **Make your changes** and test thoroughly
4. **Commit:** `git commit -m 'Add amazing feature'`
5. **Push:** `git push origin feature/amazing-feature`
6. **Open a Pull Request**

**Development Guidelines:**
- Keep the game self-contained in a single HTML file
- Maintain mobile-first responsive design
- Preserve the neon aesthetic and futuristic vibe
- Add comments for complex logic
- Test on both desktop and mobile devices

### Future Enhancements
Potential areas for improvement:
- [ ] Local storage for high scores
- [ ] Sound effects and background music
- [ ] Additional game modes (timed, marathon, etc.)
- [ ] Piece preview (next piece display)
- [ ] Accessibility improvements (colorblind mode)
- [ ] Leaderboard integration

## 🏆 Scoring System

| Action | Points | Multiplier |
|--------|--------|------------|
| Single Column Clear | 100 × Level | 1× |
| Double Column Clear | 300 × Level | 1.5× |
| Triple Column Clear | 500 × Level | 2× |
| Tetris (4 Columns) | 800 × Level | 2.5× |
| Combo (consecutive clears) | +50 per piece | Stacking |
| Hard Drop | +2 per cell dropped | - |

**Level progression:** Speed increases every 10,000 points.

## 🌐 Integration with Rexuvia

Sideways Tetris is part of the **[Rexuvia](https://rexuvia.com)** experimental games collection - a playground for novel gameplay mechanics and interactive experiences.

All Rexuvia projects:
- Are open source and MIT licensed
- Prioritize creative gameplay over commercial polish
- Serve as technical experiments and learning tools
- Welcome community involvement and remixing

## 👥 Credits & Acknowledgments

**Created by:** Rexuvia (autonomous agent swarm powered by OpenClaw)

**Inspired by:** The classic Tetris game by Alexey Pajitnov

**Special Thanks:**
- The open source game development community
- MDN Web Docs for excellent Canvas API documentation
- Players who provide feedback and suggestions

## 📄 License

**MIT License**

Copyright © 2024 Rexuvia

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

---

<div align="center">

**Enjoy the game?** ⭐ Star the repository to show your support!

[![Star History Chart](https://api.star-history.com/svg?repos=rexuvia/sideways-tetris&type=Date)](https://star-history.com/#rexuvia/sideways-tetris&Date)

**Found a bug or have a suggestion?** [Open an issue](https://github.com/rexuvia/sideways-tetris/issues)

**Want more experimental games?** Visit [rexuvia.com](https://rexuvia.com)

</div>