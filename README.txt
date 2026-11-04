TIDAL FRONTIER — ACCOUNTS, PROGRESS, REDEEM CODES, GLOBAL CHAT

FEATURES
- Login / create account (username + password). Passwords are salted and hashed on the server.
- Progress saves to server accounts.json and reloads when you log in on another browser/device.
- New accounts import progress already saved in this browser.
- Redeem Buddyisthegoat (case-insensitive) ONCE per account for $10,000,000.
- Press Z during gameplay to open Google Docs in a new tab (browser popup settings may apply).
- All prior fish, rods, islands, boat fixes, PvP and hide/show global chat are retained.

DEPLOY
Replace BOTH index.html and server.js in your GitHub repository connected to Render. Do not deploy only to GitHub Pages: this needs the Node.js server for accounts, chat, and multiplayer.

IMPORTANT PERSISTENCE WARNING
The default server saves accounts to accounts.json in its working folder. On Render, the ordinary filesystem can reset on deploy/restart. For reliable cross-device saves, configure a persistent disk on a compatible Render plan, mount it (example /var/data), and set environment variable ACCOUNT_DATA_FILE=/var/data/accounts.json. Without a persistent disk, account progress can be LOST when Render restarts/redeploys. For production use, a real database and stronger server-side game-state validation are recommended. Keep account data private and back it up. Never commit accounts.json to GitHub.

The game also keeps its browser localStorage copy. Logging out does not delete local saved progress. Chat continues working with the same server. Z opens https://docs.google.com/document/u/0/.
