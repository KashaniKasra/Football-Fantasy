
# Premier League Fantasy Football Simulator

This project is a simulation of a Premier League Fantasy Football game. It allows users to manage fantasy teams, simulate matchweeks, and track scores and player performances using real-world data.

---

## Features

- Admin panel to manage the league
- Real team simulation and weekly match results
- User fantasy team creation and management
- Simulation of red/yellow cards, goals, and player injuries
- CSV-based match and player data ingestion
- Points calculation for fantasy players
- Week-by-week progression and updates

---

## Code Structure

### `main.cpp`
Entry point that initializes the admin and starts the fantasy football simulation.

### `Admin.cpp`
Handles administrator logic, including match scheduling, user management, and score updating.

### `Futball.cpp`
Orchestrates the entire game simulation:
- Loads real data from CSV files
- Updates match results and player stats
- Coordinates user and real team logic

### `Real_Team.cpp`
Represents real football teams and tracks:
- Match outcomes
- Injured players
- Yellow/red cards
- Player performance (e.g., goals)

### `User_Team.cpp`
Handles user-created fantasy teams. Core functions include:
- Player transfers
- Weekly lineup decisions
- Calculating fantasy points

### `Player.cpp`
Encapsulates a player's performance and status (goals, injuries, cards).

### `Week.cpp`
Stores weekly simulation data (results, cards, scores) and interacts with `game_data`.

### `game.cpp`
Handles single match simulation between two real teams. Parses and stores:
- Final score
- Injuries
- Yellow and red cards
- Goal scorers

---

## Build & Run

### Requirements
- C++ compiler (GCC, Clang, etc.)
- Standard Make utility

### Build

```bash
make
```

### Run

```bash
./main
```

---

## Example Workflow

1. Admin loads real data and week data.
2. Users create and manage teams.
3. Match data is simulated via CSV inputs.
4. Player performance affects fantasy points.
5. Leaderboard and team stats are updated accordingly.

---

## Sample Fantasy Logic

- Goal scored: +5 points
- Red card: -3 points
- Yellow card: -1 point
- Injury: No points awarded

---