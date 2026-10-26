LPA WEEKLY PROGRESS EMAILER — NETLIFY SETUP

DEPLOY
1. Deploy index.html and _headers to your Netlify site (publish directory).
2. In Google Cloud Console, configure an OAuth 2.0 Client ID for a Web application.
3. Add your exact HTTPS Netlify origin to Authorized JavaScript origins.
4. Enable the Gmail API for the Google Cloud project and configure the OAuth consent screen/test users as appropriate.
5. Paste the Client ID into the app, connect Gmail, upload the CSV, review each email, and send.

CSV
Required columns: Name, Email, Course. Recommended: Overall Progress, Actual Grade, Status (used as Pacing %).
Multiple course rows with the same email are grouped into one individual email.

SECURITY / LIMITATIONS
- No OAuth client secret belongs in this static app.
- The OAuth access token is held in memory only and cleared when disconnected/reloaded.
- This app requests the gmail.send scope and sends through the Gmail API.
- If your Google Workspace administrator restricts OAuth apps or Gmail API access, an admin may need to approve the app.
- Verify the CSV mapping and every email before sending. Emails cannot be recalled by this app once sent.
