# Editit for Claude

Plan a motion graphics video with Claude and open it straight in Editit. Claude helps you shape the brief; Editit saves it as a draft in your account and gives you a link to the studio, where you add your logo, screenshots or voiceover, pick the style and generate. Generating uses your Editit credits as usual.

You need an Editit account: https://editit.in

## Claude (web, desktop and mobile)
1. Open **Settings → Connectors → Add custom connector**.
2. Name: `Editit`. URL: `https://editit.in/mcp`.
3. Click **Connect**, sign in to Editit and click **Allow**.
4. In a chat, ask: "Help me plan a 15-second Saas video for my app and start it in Editit".

## Claude Code
Install the plugin (adds the connector and the Editit skill):
```
/plugin marketplace add ncryptmedia-lgtm/editit-plugin
/plugin install editit@editit
```
Then run `/mcp`, choose **editit** and sign in.

Or add only the connector:
```
claude mcp add --transport http editit https://editit.in/mcp
```
