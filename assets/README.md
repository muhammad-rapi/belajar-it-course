# Assets Directory

This folder contains visual assets for course content:

## Structure

```
assets/
├── images/         # Static images, diagrams, screenshots
├── videos/         # Remotion video scripts & rendered videos
└── diagrams/       # Excalidraw diagrams, flowcharts
```

## Video Scripts (Remotion)

**Remotion scripts** (`.md` files) contain scene breakdowns, asset lists, and implementation notes for animated videos.

- [Computer Workflow Animation](videos/remotion-computer-workflow.md) - Input → Process → Output
- [Hardware Analogy](videos/remotion-hardware-analogy.md) - CPU/RAM/Storage kitchen analogy

**Status**: Scripts ready, videos coming soon (requires Remotion implementation).

## Fallback Strategy

Kalau Remotion too complex atau time-consuming, fallback ke:

1. **Excalidraw diagrams** (static, hand-drawn style)
2. **Simple screenshots** with annotations
3. **Emoji-based diagrams** (text-based, works everywhere)

## Contributing Visual Assets

Mau contribute images/videos?

1. **Images**: Upload to `images/` (PNG/JPG, optimized < 500KB)
2. **Remotion videos**: Add script to `videos/`, implement later
3. **Diagrams**: Excalidraw JSON + exported PNG to `diagrams/`

**Naming**: `module-X-lesson-Y-concept.ext` (e.g., `module-1-lesson-1-cpu-ram.png`)

---

**Note**: Actual video files (`.mp4`) not committed to Git (too large). Render locally or host on YouTube/CDN, then link in lessons.
