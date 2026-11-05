---
name: editit-video
description: Start a motion graphics video in Editit (explainers, SaaS product videos, kinetic typography, documentary and map videos). Use when the user asks to make or plan a video, reel or motion graphic with Editit.
---

# Starting a video with Editit

Editit makes the video in its own studio app. Your job is to help the user shape a strong brief and hand it to Editit.

1. **Shape the brief.** Ask what the video is about: the story, the key lines, names and numbers, who it is for. Call `list_styles` and suggest a style, a format (9:16, 16:9, 1:1 or 4:5) and a length within their plan limit. Ask only for what is missing.
2. **Start it.** Call `start_video` with the brief, a project name and your suggested style, format and length.
3. **Hand over.** Give the user the link. In Editit they add their logo, screenshots, photos or voiceover, confirm the style and generate. Generating uses their Editit credits.

`my_videos` lists their recent Editit projects with links. Plans and credits: https://editit.in/pricing.
