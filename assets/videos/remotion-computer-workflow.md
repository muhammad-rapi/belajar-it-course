# Remotion Video Script: Computer Workflow

**Duration**: 60 seconds  
**Lesson**: Module 1, Lesson 1 - Apa itu Komputer  
**Concept**: Input → Process → Output workflow

## Scene Breakdown

### Scene 1: Input (0-15s)

**Visual**:
- Keyboard icon (kiri layar)
- Mouse icon (kanan layar)
- User typing animation

**Animation**:
- Keyboard keys press down
- Text "google.com" muncul
- Arrow dari keyboard ke center screen

**Text Overlay**:
```
INPUT
User ketik "google.com"
```

---

### Scene 2: Process (15-40s)

**Visual**:
- CPU icon (pulsating)
- RAM bars (loading animation)
- Data packets flying
- Server icon (di cloud)

**Animation**:
- Data flows: Keyboard → RAM → CPU
- CPU processes (spinning/glowing)
- Network packet animasi ke server
- Server responds (glow)
- Packet balik ke CPU

**Text Overlay**:
```
PROCESS
1. Browser load dari storage → RAM
2. CPU kirim HTTP request
3. Server Google responds
4. CPU render HTML/CSS/JS
```

**Timeline**:
- 15-20s: Data ke RAM
- 20-25s: CPU processes
- 25-30s: Network request
- 30-35s: Server response
- 35-40s: Render

---

### Scene 3: Output (40-60s)

**Visual**:
- Monitor icon center
- Google homepage rendered
- User happy (checkmark)

**Animation**:
- Pixels drawing Google logo
- Search box appears
- Page fully loaded (progress bar 100%)

**Text Overlay**:
```
OUTPUT
Google homepage ditampilkan di monitor
Total waktu: < 1 detik
```

---

## Assets Needed

**Icons** (search free icons di flaticon.com atau use emoji):
- ⌨️ Keyboard
- 🖱️ Mouse
- 💻 CPU chip
- 🧠 RAM
- 🖥️ Monitor
- ☁️ Server/cloud
- 📦 Data packet

**Colors**:
- Background: `#1a1a1a` (dark)
- Accent: `#00bfff` (cyan/blue for data flow)
- Highlight: `#ff6b6b` (red for active processing)
- Text: `#ffffff` (white)

---

## Implementation Notes

**Remotion Components**:
```tsx
// File: remotion/ComputerWorkflow.tsx

import {useCurrentFrame, interpolate, spring} from 'remotion';

export const ComputerWorkflow = () => {
  const frame = useCurrentFrame();
  
  // Scene 1: Input (0-15s = 0-900 frames at 60fps)
  const inputOpacity = interpolate(frame, [0, 60], [0, 1], {
    extrapolateLeft: 'clamp',
    extrapolateRight: 'clamp'
  });
  
  // Scene 2: Process (15-40s = 900-2400 frames)
  const processStart = 900;
  const cpuGlow = spring({
    frame: frame - processStart,
    fps: 60,
    config: {damping: 10}
  });
  
  // ... (rest of animation logic)
  
  return (
    <AbsoluteFill style={{backgroundColor: '#1a1a1a'}}>
      {/* Render scenes based on frame */}
    </AbsoluteFill>
  );
};
```

---

**Fallback**: Kalau Remotion terlalu complex, bisa pakai **static diagram** (Excalidraw) + screenshot.
