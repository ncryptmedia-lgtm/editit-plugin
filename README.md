# Editit for Claude

Make motion graphics videos with Editit inside Claude. Ask for a video and the Editit panel opens in the chat: write the brief, pick a style, format and length, add your logo and images and press Generate. Claude then makes the video with Editit's house style, checks it with preview frames and renders the MP4 into your Editit account. Generating uses your Editit credits, and videos made in Claude cost less than in the Editit app:

| Length | Credits |
|---|---|
| up to 15 s | 30 |
| up to 30 s | 40 |
| up to 60 s | 70 |
| each change after a render | 15 |

You need an Editit account: https://editit.in

## Claude (web, desktop and mobile)
1. Open **Settings → Connectors → Add custom connector**.
2. Name: `Editit`. URL: `https://editit.in/mcp`.
3. Click **Connect**, sign in to Editit and click **Allow**.
4. In a chat, ask: "Make a 15-second Saas video for my app with Editit".

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
