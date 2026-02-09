# Little Jimmy Hollywood Scorecard

A sophisticated web app for tracking Hollywood-style gin rummy scores with monetary tracking, multiple pages, and fun visual indicators.

## Features

### Core Scoring System
- **Hollywood Scoring**: Each player's wins progress through three simultaneous games
  - 1st win → Game 1 only
  - 2nd win → Games 1 and 2
  - 3rd+ wins → All three games
- **"Kids on the Freeway" Rule**: Players must score in lower-numbered games before unlocking higher ones
  - Must score in Game 1 before Game 2 opens
  - Must score in Games 1 & 2 before Game 3 opens
  - Completed games automatically unlock the next game (prevents shutout deadlock)

### Turn the Page
- **Multi-Page Gameplay**: When Games 1 & 2 are complete on the current page, turn to a new page
- **Continuous Play**: Game 3 from previous pages continues while new pages start fresh
- **Unlimited Pages**: Turn to Page 3, 4, 5... as games complete
- **Tab Navigation**: Switch between pages with tabs or swipe gestures on mobile

### Visual Indicators
- 🟢 **Green "💪 Crushed it!"** - Won game
- 🔵 **Blue "🏈 Field goal range!"** - At 75%+ of winning score
- 🔴 **Red "🚗 Kids on freeway!"** - No score yet in this game
- **"Kids out of the freeway!" popup** - Celebration when getting on the board

### Money Tracking
- **Session Balance**: Running totals across all pages and rounds
- **Game Value**: Customizable base payout per game won
- **Box Bonus**: Bonus per hand difference between winner and loser
- **Shutout Doubling**: All payouts doubled when opponent scores zero
- **Persistent Balances**: Money carries over when starting new rounds

### Customization
- **Player Names**: Edit names for personalization
- **Adjustable Starting Balances**: Set initial money positions
- **Configurable Values**: 
  - Winning score (default: 100 points)
  - Game value (default: $5.00)
  - Box value (default: $1.00 per hand)

### User Experience
- **Progressive Web App**: Install on iPhone home screen
- **Works Offline**: No internet required after installation
- **Auto-Save**: All data persists automatically
- **Undo Function**: Correct mistakes easily
- **Mobile-Optimized**: Swipe between pages, touch-friendly interface

## How to Use

### Installation on iPhone
1. Visit the app URL in Safari
2. Tap the Share button (square with arrow)
3. Select "Add to Home Screen"
4. Tap "Add"

### Basic Gameplay
1. Select which player won the hand
2. Enter their points
3. Click "Add" to record the score
4. Scores automatically distribute to eligible games based on Hollywood rules

### Turn the Page
1. Play until Games 1 & 2 are complete on the current page
2. Click "Turn the Page" button when it appears
3. Continue playing with Game 3 from the previous page still active
4. New page starts with fresh Games 1, 2, and 3

### Starting a New Round
- **New Round**: Clears all games but preserves player balances
- **Reset All**: Clears everything including balances

## Scoring Rules

### Hollywood Progression
- Each player's wins cascade through games independently
- Player must "get on the board" (score at least once) in lower games to unlock higher games
- Once a game is complete, it automatically unlocks the next game for both players

### Money Calculations
- **Base Game Value**: Set in settings (default $5.00)
- **Box Bonus**: (Winner's hands - Loser's hands) × Box Value
- **Shutout Bonus**: If opponent scores zero, all values are doubled
- **Example**: Win a game 105-0 with 8 hands vs 5 hands
  - Game Value: $5.00
  - Box Bonus: (8-5) × $1.00 = $3.00
  - Subtotal: $8.00
  - Shutout Doubling: $8.00 × 2 = **$16.00**

## Default Settings

- **Winning Score**: 100 points
- **Game Value**: $5.00 per game
- **Box Value**: $1.00 per hand difference

All settings can be customized via the settings (⚙️) menu.

## Technical Details

- Built with vanilla JavaScript (no framework dependencies)
- Styled with Tailwind CSS
- Data persistence via localStorage
- Progressive Web App (PWA) compatible
- Mobile-responsive design
- Touch gesture support for page navigation

## License

Free to use for personal purposes.

---

**Little Jimmy Hollywood Scorecard** - For serious card players who want professional scorekeeping with personality. 🃏💰🚗
