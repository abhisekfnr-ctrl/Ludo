ROYAL LUDO v25 - ONLINE MULTIPLAYER + ADMIN

Features:
- User register/login
- Separate rooms for separate games
- 2 or 4 players per room
- Same room can be played from different devices/networks
- Player device is bound to its room slot
- Admin dashboard: users, online presence, rooms, live status, game history
- Block/unblock users
- Next-roll dice control

Run:
1. Node.js 18+
2. npm start
3. Local: http://SERVER-IP:3000/
4. Admin: http://SERVER-IP:3000/admin.html

IMPORTANT SECURITY:
Set ADMIN_PASSWORD before deployment. Example:
Linux/macOS: ADMIN_PASSWORD="your-strong-password" npm start
Windows PowerShell: $env:ADMIN_PASSWORD="your-strong-password"; npm start
Default admin password is change-me-123 and MUST be changed for internet deployment.

For public internet, deploy the folder on a Node.js hosting/server with HTTPS. The app stores users, rooms and history in data.json. For production scale, move this data to PostgreSQL/Redis and add Socket.IO/WebSockets.


v25 checks/fixes:
- Room-scoped admin dice control is the primary control; each player's forced value is consumed once.
- Admin can open a room's live board, pause/resume, reset, close, kick players, clear forced dice, and force the active turn.
- Admin-only protection added to the settings write endpoint.
- Room filter added to the admin dashboard for easier multi-room control.
- Guest mode remains supported by the game UI.
- The game still uses data.json; for large public deployment, PostgreSQL/Redis + WebSocket is recommended.
