---
name: beatboard
description: Generate 9-panel beat board image prompts
trigger: /beatboard
---

# Beat Board Generator (9-Panel)

Generates 9 image prompts that establish the visual baseline for the episode.

## Usage

```
/beatboard ep01
```

## What This Does

1. **Reads approved beat breakdown** from `outputs/beat-breakdown-ep{XX}.md`
2. **Calls Storyboard Artist** to create 9 image prompts
3. **Director reviews** for character consistency and format
4. **Saves output** to `outputs/beat-board-prompt-ep{XX}.md`

## Prerequisites

- Beat breakdown exists and is approved
- Visual style configured

## Output

Creates `outputs/beat-board-prompt-ep{XX}.md` with:

- 9 detailed image prompts (one per beat)
- Narrative descriptive style (80-150 words each)
- Character consistency across all prompts
- Unified visual style

## Next Step

After approval: `/sequence ep01`

## Generation Targets

Use these prompts with:

- Gemini Imagen 3
- Midjourney v6
- DALL-E 3
- Stable Diffusion XL
