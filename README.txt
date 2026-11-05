TIDAL FRONTIER — MEGA UPDATE

Upload index.html, server.js, package.json and .gitignore to your existing GitHub repository.
Deploy as a Render WEB SERVICE (Node.js), not GitHub Pages static hosting.
Build command: npm install
Start command: npm start

FEATURES: Leaderboards, Kraken boss battle, Golden/Rainbow/Shadow fish, daily rewards, money trading, bounties, arena wagering, 5 extra boats, full cooler inventory, rotating ocean weather, quests, upgradeable player bases. Open MEGA UPDATE in-game.

LOGIN FIX: usernames are trimmed and case-insensitive, passwords can be 3+ characters, and sessions are persisted to a JSON file. New errors distinguish missing accounts from incorrect passwords. Login test passed locally.

IMPORTANT: Render's ephemeral filesystem is NOT permanent. Set ACCOUNT_DATA_FILE=/var/data/accounts.json, SESSION_DATA_FILE=/var/data/sessions.json, GAME_DATA_FILE=/var/data/world.json and attach a persistent disk mounted at /var/data. If your Render plan does not support persistent disks, you must use a database or a persistent host instead. Previously deleted accounts cannot be recovered without a backup. Don't create new accounts until persistent storage is configured if you need progress to survive redeploys.

Trade system currently supports money gifts held in escrow, not fish/rod swaps. Arena is a wagered random showdown, not a separate movement map. Boss is a cooperative server health bar. Bases are upgradeable levels, not yet editable 3D houses. Weather changes water appearance, not movement physics. Client-reported money remains susceptible to cheating; a fully secure economy requires server-authoritative progression.

Existing chat, codes, fish index, islands, PvP 20% death penalty, and Buddy Big Stick are retained. Test live multiplayer before publishing broadly.

CHROMEBOOK PERFORMANCE UPDATE: low graphics by default; quality button; culling, frame-time movement, non-overlapping multiplayer sync.
