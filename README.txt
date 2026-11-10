TIDAL FRONTIER — SUPABASE + BASE + BOUNTY FIX

This ZIP includes ALL the previous base/bounty update AND the Supabase account migration.

1. In Render > Tidal Frontier > Environment, add DATABASE_URL with your Supabase Session Pooler PostgreSQL URL (replace [YOUR-PASSWORD] including brackets). Never put this URL in GitHub.
2. Upload index.html, server.js, package.json, .gitignore from this ZIP to the ROOT of the SAME GitHub repository for your Render service, replacing the old files. Do not upload the ZIP itself or upload DATABASE_URL.
3. In Render, deploy latest commit. Build command: npm install ; Start command: npm start.
4. Wait for logs to show 'Supabase connected'. The server automatically creates its own tidal_storage table and loads all accounts/sessions/world/clans from Supabase.
5. Test creating an account, catching/selling fish, logging out/in, and redeploying. Check that progress survives. Test the bounty input and MY BASE upgrades.

IMPORTANT: Accounts already deleted by Render's old ephemeral filesystem cannot be recovered without a backup. The new database begins empty. Old accounts still in the previous server's temporary JSON files are NOT automatically imported. Do not assume they have been migrated. Contact me if you have a backup of accounts.json / clans.json / world.json.

If Render logs show a Supabase connection error, check that you selected Session Pooler, your password is correct, and the DATABASE_URL is entered in Render (not GitHub). Special characters in database passwords must be URL-encoded in connection strings.

Security: Keep DATABASE_URL and your database password private. Supabase's free tier has usage limits and may pause inactive projects. This patch preserves the existing game's client-trusting money/PvP mechanics; it does not fully prevent cheating.

SMOOTH CANNON PATCH: Client animates cannonballs every frame using server velocity instead of snapping to positions at each network poll. Server now transmits velocity.
