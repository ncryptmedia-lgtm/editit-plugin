---
name: editit-video
description: Make a motion graphics video with Editit (explainers, SaaS product videos, kinetic typography, documentary and map videos) and render it to MP4. Use when the user asks to make, animate or render a video, reel or motion graphic with Editit.
---

# Making a video with Editit

1. **Open Editit.** Call `open_editit`, passing anything the user already said (brief, style, format, length). The Editit panel appears: the user writes the brief, picks the style, format and length, adds their logo and images and presses Generate, which uses their Editit credits.
2. **Read the guide.** When the panel sends the video id, call `get_video_guide` with it and read every part (`part: 2`, `3`, … until it says "last part"). The guide is the authority on the look and the technical rules.
3. **Write the file.** Write the complete video file the guide describes. Keep it out of the chat unless the user asks to see it.
4. **Preview and fix.** Call `preview_frames` with the file. Fix every error and quality note, compare the frames with the guide, and preview again until it looks right.
5. **Finish.** Call `finish_video` with the final file, then `render_status` every 30–60 seconds until it is done. Give the user the MP4 link and the project link.

If the panel says the user is out of credits or over their plan's length limit, point them to https://editit.in/pricing.
