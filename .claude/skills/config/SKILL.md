---
name: config
description: Configure visual style for episode
trigger: /config {episode}
parameters:
  - name: episode
    description: Episode identifier (e.g., ep01, ep02)
    required: true
    type: string
    pattern: "^ep\\d{2}$"
---

# Visual Style Config

Configure visual style parameters for an episode.

**Usage**: `/config ep01`

**Configures**:

- Style keywords (e.g., "anime, cinematic")
- Aspect ratio (16:9, 9:16, 1:1)
- Target model (Gemini Imagen 3, Midjourney, etc.)
- Language (zh-CN, en-US, ja-JP, ko-KR)

**Saves to**: `.agent-state.json` under episode config
