⚜ POLYCIAL - The Political Property Game
"Acquire land, wield power, dominate the nation."

Polycial is a fully featured, browser-based property trading board game inspired by Monopoly, reimagined through the lens of political power. Buy districts, build influence, negotiate deals, and bankrupt your rivals  all in a single self-contained HTML file with zero dependencies.

Start Screen
Start Screen The animated title screen with per-player name editing, AI toggle, and game settings.

Game Board
Game Board The full 40-space political board with token sprites, ownership dots, and live sidebar panels.

Mid-Game  Properties & Houses
Mid-Game Twelve turns in: houses on orange properties, ownership panel active, net worth chart updating live.

Property Purchase Modal
Modal Clicking any property opens a detailed card showing the full rent schedule, mortgage value, and buy/decline actions.

Settings Panel
Settings The full settings screen: gameplay rules, board themes, turn timer, pass-and-play mode, and house rules.

Mid-Game Stats
Stats The 📊 STATS popup shows cash, net worth, monopolies, rent paid, and visual bar charts per player.

🎮 Features

Core Gameplay
40-space political board — all 8 color groups (Brown → Navy), 4 railroads, 2 utilities, Chance, Community Chest, taxes, Jail, Free Parking, and Go To Jail
Politically themed properties — Capitol Ave, Embassy Row, Filibuster Rd, The Palace, and more
Full rent engine — monopoly bonuses, railroad scaling (25/50/100/200), utility dice multipliers
Houses & Hotels — build up to 4 houses then upgrade to a hotel; configurable max via settings
Mortgaging & Unmortgaging — mortgage at face value, redeem at 110%
Jail mechanics — roll doubles to escape, pay $50 bail, use Get Out of Jail Free cards

Trading System
Full trade UI — select multiple properties from both sides, add cash offers
Counter-offers — human players can accept, decline, or counter any trade
AI trade logic — AI evaluates trades by comparative value and accepts fair deals
AI trade offers — aggressive AI proactively offers cash for properties that would complete a monopoly

Artificial Intelligence
3 AI personality tiers — Aggressive, Balanced, Conservative
Smart buying — each tier reserves different cash buffers and targets different price ranges
Strategic building — aggressive AI builds to hotels, conservative caps at 2 houses
Auto-unmortgage — AI redeems properties when cash is comfortable
Configurable per player — click the 👤 HUM button on any player row to cycle through AI tiers

Political Events
Random Political Event Cards fire every 3–7 rounds with real game-state effects:
🗳️ Campaign Finance Reform — all players pay $30 to the Treasury
📰 Scandal! — richest player loses $200 in legal fees
🏗️ Infrastructure Bill — railroad owners collect $50 per railroad
💰 Economic Stimulus — every player collects $50
🏛️ Eminent Domain — random unowned property goes to immediate auction
👑 Election Results — net-worth leader pays a popularity tax

Bankruptcy Auctions
When a player goes bankrupt, their assets are liquidated intelligently: 1. All houses sold at 50% value 2. All unmortgaged properties auto-mortgaged 3. If still insolvent, every remaining property goes to a competitive auction among surviving players

Visual & UX
Animated token sprites — smooth cubic-bezier movement across the board
Board hover highlights — hover a player card to glow all their properties on the board
Gold outline on the active player's properties at all times
4 board themes — Classic, Night, Parchment, Ocean
Net Worth live chart — sidebar bar chart updates every transaction
Turn counter and turn-by-turn game log

Sound Effects (Web Audio API)
All sounds are generated in-browser — no audio files required:

Event	Sound
Dice roll	Double square-wave click
Passing GO	Rising three-note fanfare
Buying property	Two-tone chime
Paying rent	Low sawtooth sting
Going to Jail	Descending square bass
Political Event	Triple triangle tone
Victory	Four-note ascending fanfare
Toggle sound on/off with the 🔊 button in the bottom-right corner at any time.

Turn Timer
Set 15–120 second limits per turn in Settings (or OFF)
Gold progress bar under the turn indicator counts down
Turns red below 25% remaining
Auto-rolls dice if time expires before rolling; auto-ends turn if already rolled

Pass & Play Mode
Enable in Settings for shared-device play. Between every turn, a full-screen handoff card appears showing the next player's name and token, with an "I'M READY" button — so no one accidentally sees the board mid-turn.

Save & Resume
Manual save via the 💾 SAVE header button
Auto-save every 3 turns silently in the background
Resume badge on the start screen shows "Turn X (saved 2m ago)"
Full game state persisted: positions, money, properties, houses, stats, event counter

Statistics
Mid-game 📊 STATS popup accessible any time from the header
Per-player data: Cash, Net Worth, Properties, Monopolies, Rent Paid, GO Passes
Visual bar charts for Net Worth and Rent Paid
End-game win screen shows Rent Paid chart + Final Net Worth chart for all players

🕹️ Controls
Start Screen
Control	Action
2 / 3 / 4 buttons	Set number of players
Name input field	Edit player name
👤 HUM button	Toggle player to AI (cycles: Human → Balanced AI → Aggressive AI → Conservative AI)
▶ BEGIN SESSION	Start the game
⚙ SETTINGS	Open settings panel
Resume badge (if shown)	Load last saved game

In-Game Actions
Button	When Available	Action
🎲 ROLL	Start of turn	Roll both dice and move
💰 BAIL	In Jail, before rolling	Pay $50 or use Jail Free card to escape
🏠 BUILD	After rolling, own a monopoly	Buy houses or hotels on your properties
📜 MORT	After rolling, own unmortgaged props	Mortgage a property for cash
🔓 UNMORT	After rolling, own mortgaged props	Redeem a mortgaged property (+10% fee)
🤝 TRADE	After rolling, own any property	Open trade UI with another player
→ END	After rolling	End your turn and pass to next player

Header Buttons
Button	Action
💾 SAVE	Manually save current game state
📊 STATS	Open mid-game statistics popup
⚙	Quick settings (toggle jackpot, view current config)
✕	Return to main menu (with save prompt)
🔊 / 🔇	Toggle all sound effects (bottom-right corner)

Board Interaction
Action	Result
Click any cell	Open property info card with rent schedule and current owner
Click own property (after rolling)	Info card includes quick Mortgage / Unmortgage buttons
Hover player card	Highlights all properties owned by that player on the board
Click player card	Opens detailed player profile with full property list

Settings Reference
Setting	Default	Description
Starting Money	$1,500	Cash each player begins with ($500–$5,000)
GO Salary	$200	Collected each time you pass GO ($100–$500)
Free Parking Jackpot	OFF	Taxes go to a pot; landing on Free Parking wins it
Auction on Decline	ON	Declined properties go to competitive auction
Double Salary on GO	OFF	Landing exactly on GO pays double salary
No Rent in Jail	OFF	Jailed players cannot collect rent
Max Houses	4	Houses needed before hotel upgrade (1–4)
Pass & Play Mode	OFF	Shows handoff screen between human turns
Turn Timer	OFF	Countdown per turn in seconds (15–120)
Board Theme	Classic	Classic / Night / Parchment / Ocean
Animation Speed	Normal	Normal / Fast / Slow / Off
Show Property Prices	ON	Display price labels on board cells

Railroads & Utilities
Space	Type	Cost	Rent
Ballot Rail (5)	Railroad	$200	$25 × 2ⁿ (n = railroads owned)
Reform Rail (15)	Railroad	$200	$50 / $100 / $200
Vote Rail (25)	Railroad	$200	(same formula)
Tycoon Rail (35)	Railroad	$200	up to $200 for all 4
Power Co. (12)	Utility	$150	4× dice (one owned), 10× dice (both)
Water Works (28)	Utility	$150	same as above

🃏 Card Decks

Chance Cards (9)
Advance to GO — collect salary
Advance to nearest railroad
Elected Chairman — pay $50 to each player
Bank dividend — collect $50
Consulting fee — collect $25
Filibuster succeeded — collect $150
Speeding fine — pay $15
Get Out of Jail Free
Go to Jail

Community Chest (8)
Advance to GO — collect salary
Tax refund — collect $100
Life insurance matures — collect $100
Consulting fee — collect $25
Doctor's fees — pay $50
School fees — pay $50
Get Out of Jail Free
Go to Jail

Political Events (6, trigger every 3–7 rounds)
Campaign Finance Reform
Election Results
Infrastructure Bill
Scandal!
Economic Stimulus
Eminent Domain


🛠️ Technical Notes
Zero dependencies — no frameworks, no CDN, no build tools
Web Audio API for all sound effects — procedurally generated, no audio files
CSS custom properties for consistent theming across all 4 board themes
localStorage for save/resume — data persists across browser sessions
Token sprites positioned absolutely over the board using getBoundingClientRect() for pixel-perfect placement at any screen size
Playwright-compatible — all UI state is accessible via global JS variables for testing
