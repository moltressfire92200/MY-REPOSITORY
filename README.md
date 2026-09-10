# MY-REPOSITORY — Free Anime Video Workspace

This repository is set up as a free GitHub-based video workspace.

## Folder structure

- `images/` — source anime images (PNG/JPG)
- `audio/` — optional narration, music and sound effects
- `clips/` — rendered scene clips
- `output/` — final MP4 files
- `scripts/` — local rendering scripts
- `.github/workflows/` — GitHub Actions automation

## Current workflow

The GitHub Actions workflow can be started manually from **Actions → Render Anime Video → Run workflow**. It uses FFmpeg on a GitHub-hosted Ubuntu runner to turn the images in `images/` into a video and optionally add audio.

GitHub Actions workflows are YAML files stored under `.github/workflows/` and can be manually triggered with `workflow_dispatch`. See the GitHub Actions documentation for details.

## Important limitation

GitHub Actions can render and assemble video for free within the available GitHub Actions usage limits, but it is **not itself a free AI image-to-video model**. This workspace currently provides the rendering/assembly pipeline. An AI animation provider would need to generate motion frames/clips first, after which those files can be placed in `clips/` or processed by the pipeline.

## Image naming

For the first scene, use names such as:

```text
images/scene01_001.png
images/scene01_002.png
images/scene01_003.png
```

The renderer sorts image files alphabetically, so numeric prefixes keep the intended order.
