# Latent Space YouTube Plugin

A Claude Cowork / Claude Code plugin for the end-to-end pipeline of downloading Zoom cloud recordings and publishing them to YouTube — with auto-generated titles, descriptions, timestamps, playlists, and AI-generated thumbnails.

Built for the [Latent Space](https://latent.space) community's "AI in Action" weekly jam and Paper Club recordings, but the patterns are adaptable to any Zoom-to-YouTube workflow.

## Skills

| Skill | What it does |
|---|---|
| **zoom-to-youtube** | Orchestrator — runs the full pipeline with checkpoint stages between each phase |
| **zoom-download** | Download Zoom cloud recordings, pick the right file type, extract frames for analysis |
| **youtube-publish** | Upload to YouTube Studio, set titles/descriptions/timestamps/playlists, publish |
| **youtube-thumbnails** | Generate custom thumbnails via Google Gemini (Pro mode), compress, upload |

Each skill works standalone or as part of the orchestrated pipeline.

## Pipeline Flow

```
Stage 0: Pre-Flight Scan     → scan Zoom + YouTube, cross-reference, present plan
Stage 1: Download             → grab recordings, extract frames, propose titles
  ↓ checkpoint (confirm titles & playlists)
Stage 2: Publish              → upload, set metadata, assign playlists, publish
  ↓ checkpoint (confirm URLs & status)
Stage 3: Thumbnails           → generate via Gemini, compress, upload
  ↓ checkpoint (confirm thumbnails set)
Stage 4: Cleanup              → optionally delete Zoom recordings & local files
```

## Requirements

- **Zoom account** with cloud recording enabled
- **YouTube channel** with Studio access
- **Google Gemini** account (for thumbnail generation, Pro mode recommended)
- **ffmpeg** (for frame extraction / content analysis)
- **ImageMagick** (for thumbnail compression)
- A browser automation tool (Claude in Chrome, Cowork browser tools, etc.)

## Usage

In Claude Cowork or Claude Code, the skills are available after installing the plugin. Use them by asking naturally:

- *"Download the latest Zoom recordings and upload them to YouTube"* → triggers `zoom-to-youtube`
- *"Grab the new Zoom recordings"* → triggers `zoom-download`
- *"Set up titles and publish these videos"* → triggers `youtube-publish`
- *"Generate thumbnails for the videos I just uploaded"* → triggers `youtube-thumbnails`

## License

MIT
