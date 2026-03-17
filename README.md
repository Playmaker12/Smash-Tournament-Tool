 Smash Tournament Tool 
 ========================================

A desktop application for Super Smash Bros. Ultimate tournament organizers.

- Manage player rankings (Elo-based) using data from start.gg.
- Generate and manually adjust seeding lists.
- Export seeding to Excel.

----------------------------------------
Quick Start
----------------------------------------
1. Run SmashTournamentTool.exe
2. Go to Settings > Set API Token and enter your start.gg API token
   (Get one from https://www.start.gg/admin/profile/developer)
3. In the Rankings tab, click "Update from start.gg" and enter the
   tournament slug and event slug (e.g., "my-weekly-42", "ultimate-singles")
   to fetch match data and update player rankings.
4. Switch to the Seeding tab to add players (auto-complete from database or
   add new), generate preliminary seeds, manually adjust, then export to Excel.

----------------------------------------
Data Storage
----------------------------------------
The application creates two files in the same folder as the executable:

- rankings.db : SQLite database containing all players, rankings, and matches.
- config.json : Stores your start.gg API token.

If you delete these files, all data will be lost (a new empty database will be
created next time you run the app). To reset everything, use:

  Settings > Reset Database

----------------------------------------
Player Names (important)
----------------------------------------
Start.gg display names can change between events (for example, adding a sponsor
tag). The app attempts to associate returning players using a more stable start.gg
identity when available, and will update the stored gamertag when the same player
changes their tag.

----------------------------------------
Requirements
----------------------------------------
- Windows (the .exe is standalone; no Python installation needed).
- Write permission in the folder where the .exe is placed (so it can create the
  database and config file).

----------------------------------------
Troubleshooting
----------------------------------------
- If updates fail, check your API token and internet connection.
- If the app doesn't start, try running it from a folder you have full write
  access to (e.g., Desktop or Documents).

Enjoy!

