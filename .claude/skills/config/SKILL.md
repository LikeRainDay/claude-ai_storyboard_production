---
name: config
description: Configure visual style for an episode
trigger: /config
---

# Visual Style Configuration

Set or update visual style configuration for an episode.

## Usage

```
/config ep01
```

Or simply:

```
/config
```

(Will prompt for episode number)

## What This Does

Prompts for and saves visual configuration:

### 1. Visual Style Keywords

Examples:

- `"anime style, cinematic lighting, vibrant colors, dramatic shadows"`
- `"photorealistic, natural lighting, muted earth tones"`
- `"watercolor illustration, soft pastels, dreamy atmosphere"`
- `"cyberpunk aesthetic, neon lighting, high contrast"`

### 2. Aspect Ratio

Options:

- **16:9** - Cinematic widescreen (recommended)
- **9:16** - Mobile/vertical video
- **1:1** - Square (Instagram)
- **4:3** - Classic TV
- **21:9** - Ultra-wide cinematic

### 3. Target AI Model

Options:

- **Gemini Imagen 3** (recommended for this system)
- Midjourney v6
- DALL-E 3
- Stable Diffusion XL
- Custom (specify)

## Output

Saves configuration to `.agent-state.json`:

```json
{
  "episodes": {
    "ep01": {
      "visual_style": "anime style, cinematic lighting, vibrant colors",
      "aspect_ratio": "16:9",
      "target_model": "Gemini Imagen 3",
      "configured_at": "2026-01-10T20:45:00+08:00"
    }
  }
}
```

## When to Use

- **Before starting**: Configure style before running `/breakdown`
- **Style change**: Update style if you want to regenerate with different aesthetic
- **Per episode**: Each episode can have its own unique visual style

## Next Step

After configuration:

- If no beat breakdown exists: `/breakdown ep01`
- If breakdown exists but not beat board: `/beatboard ep01`
