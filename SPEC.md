# Candy Crush Clone - Specification Document

## 1. Project Overview

**Project Name:** Crystal Crush  
**Type:** Mobile Match-3 Puzzle Game (Android)  
**Core Functionality:** A Candy Crush-style match-3 game with cascading rocks, special rocks, boosters, levels, and progression system.

---

## 2. Visual & Rendering Specification

### Scene Setup
- **Camera:** Orthographic 2D camera, fixed top-down view
- **Background:** Animated gradient with floating candy motifs
- **Grid:** 9x9 game board with subtle grid lines

### Materials & Effects
- **Rocks:** 6 basic types (Red Ruby, Orange Amber, Yellow Topaz, Green Emerald, Blue Sapphire, Purple Amethyst)
- **Special Rocks:**
  - Striped (4-match): Clears row/column
  - Wrapped (L-shape): 3x3 explosion
  - Rainbow (5-match): Clears all of one color
- **Particles:** Sparkle effects on matches, fall physics
- **UI:** Candy-style fonts, bubble buttons, smooth animations

### Color Palette
- Primary: Vibrant candy colors
- Background: Soft pink to purple gradient
- UI: White with colored accents

---

## 3. Game Mechanics Specification

### Core Gameplay
- **Grid Size:** 9x9 tiles
- **Matching:** Swap adjacent rocks to match 3+ in row/column
- **Cascading:** Rocks fall after matches, new rocks spawn from top
- **Scoring:**
  - 3-match: 50 points
  - 4-match: 100 points + Striped rock
  - 5-match: 200 points + Rainbow rock
  - L/T-shape: 150 points + Wrapped rock

### Level System
- **Target Types:**
  - Reach score target
  - Clear specific rock count
  - Collect order pieces
- **Moves Limit:** 15-30 moves per level
- **Star System:** 1-3 stars based on score

### Boosters (from shop)
- Hammer: Removes one rock
- Color Bomb: Changes rock colors
- Striped Rock: Creates striped rock

---

## 4. Interaction Specification

### Controls
- **Touch/Drag:** Swap candies by dragging
- **Tap:** Select booster, activate power-ups

### UI Elements
- **Main Menu:** Play button, Settings, Shop
- **Level Select:** Grid of levels with stars
- **In-Game:** Score, Moves remaining, Target display
- **Shop:** Buy boosters with collected coins

---

## 5. Audio Specification

- **Background:** Happy, loopable music
- **SFX:** Match sounds, cascade sounds, special candy activate

---

## 6. Technical Architecture

### Game Engine
- Unity-based architecture (simulated in HTML5/Canvas for web)

### Data Persistence
- **PlayerPrefs:** Level progress, coins, unlocked boosters
- **JSON:** Level configurations

---

## 7. Acceptance Criteria

1. ✅ 9x9 grid with 6 rock types renders correctly
2. ✅ Swapping two rocks works (only valid swaps allowed)
3. ✅ 3+ matches detected and removed
4. ✅ Cascading gravity works (rocks fall down)
5. ✅ Special rocks spawn on 4/5 matches
6. ✅ Special rock effects work (striped, wrapped, rainbow)
7. ✅ Score tracks correctly
8. ✅ Level completion with star rating
9. ✅ At least 10 playable levels
10. ✅ Shop system with coins
11. ✅ Basic animations and polish