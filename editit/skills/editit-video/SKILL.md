---
name: editit-video
description: Make a motion graphics video with Editit (explainers, SaaS product videos, kinetic typography, documentary and map videos) and render it to MP4. Use when the user asks to make, animate or render a video, reel or motion graphic with Editit.
---

# Making a video with Editit

Editit gives you its house style guides, checks and previews your video file, and renders the MP4 into the user's Editit account. Renders cost Editit credits; guides and previews are free.

1. **Agree the basics.** Call `list_styles`, then settle with the user: the style, the format (9:16, 16:9, 1:1 or 4:5), the length (within their plan limit) and the brief (story, key lines, names, numbers). Ask only for what is missing.
2. **Read the guide.** Call `get_style_guide` with the style, brief, format and length. Read every part (call again with `part: 2`, `3`, … until it says "last part"). The guide is the authority on the look and the technical rules.
3. **Write the file.** Write the complete video file the guide describes. Keep it out of the chat unless the user asks to see it.
4. **Preview and fix.** Call `preview_frames` with the file. Fix every error and quality note, look at the frames against the guide, and preview again until it looks right.
5. **Ask, then render.** Tell the user the credit cost (from `list_styles`) and ask before rendering. Call `render_video` with the same style, brief, format and length and the final file.
6. **Deliver.** Call `render_status` every 30–60 seconds until it is done, then give the user the MP4 link and the project link. For changes, edit the file, preview, and call `render_video` again with `project_id`; tell the user each render is charged.

If a tool says the user is out of credits or over their plan's length limit, explain it and point them to https://editit.in/pricing.
