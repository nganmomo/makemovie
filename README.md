# Framecraft — YouTube Maker

A buildless, responsive video-planning application. Open `dist/index.html` or serve `dist` with a static server. No build dependencies or AI API keys are required.

Users configure a title, audience, format, language, and style; add, duplicate, reorder, and remove scenes; upload images, video, and audio; describe image generation and edits; specify narration, music, sound effects, and transitions; and download a Markdown AI production brief or an editable JSON project.

Project settings save in localStorage. Media files save in IndexedDB on the current browser/device. The scene preview displays text, a background, and the first uploaded image; it is a layout guide, not a rendered video. Exports include file references, not embedded media. Supply original files alongside exports. AI generation and YouTube publishing are downstream steps, not connected services in this project.

To run a local server: `node server.cjs`. Visit http://localhost:4173.

AI clip revisions: upload returned video under “Reload AI-generated or modified clips.” Revision numbers and next-edit instructions are included in Markdown and JSON exports. Requested container, resolution, and frame rate are instructions for the downstream AI/editor; the app does not transcode media. JSON import preserves scene IDs and revision metadata. MP4, WebM, and MOV may be uploaded; browser playback depends on codec support.
