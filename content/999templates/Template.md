---
title: Template for Quartz 4
draft: true
tags:
  - example-tag
---
If the draft box is checked, it will not be shown on the site.
The "Title" property is what will be displayed on the website, not the name of the note.

I used this YouTube video to help me set up Quartz 4: 
[Turn Your Obsidian Notes Into A Website by isak (2025-08-31)](https://www.youtube.com/watch?v=zGFroBGud7w)

To build and preview, use:
```
npx quartz build --serve
```
This will start a local web server to run your Quartz on your computer. Open a web browser and visit `http://localhost:8080/` to view it.

Use `npx quartz sync` to push changes
~~Use `npm run sync` to push changes~~