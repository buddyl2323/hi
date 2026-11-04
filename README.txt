TIDAL FRONTIER — VOID ABYSS UPDATE

Upload index.html and server.js to the existing GitHub repository, then redeploy Render. Keep .gitignore.

New island: Void Abyss, southeast corner of the world (near x=2990,y=1900). Ten new extremely difficult fish. The rarest fish, The Uncatchable, has an extremely low bite chance and a very difficult fishing minigame.

Fish Index: 70 total species. Completing the index awards the permanent rod loganiskingthats (Power 65). This is stronger than the shop rods (max 24) but not the temporary Buddy Big Stick (9999). Existing saved index reward flags are preserved.

All other gameplay and account/chat systems remain. Progress persistence on Render still requires persistent server storage; default ephemeral storage can reset accounts.

BALANCE UPDATE: When a player defeats another with the Raider Blade, the victim loses 10% of their current wallet and the attacker receives that amount. The victim respawns at Starter Cove and has 8 seconds of protection. Death event IDs prevent the same death from charging the victim repeatedly during network polling. The existing 15-second attack cooldown remains. Note: money is still reported by clients; fully cheat-proof economy requires server-authoritative balances and persistent storage.

ECONOMY SINK UPDATE: On PvP death, victim loses 20% of their current wallet. The attacker gets 10%, and the other 10% is destroyed (not credited to any player). Rounding down to whole dollars.
