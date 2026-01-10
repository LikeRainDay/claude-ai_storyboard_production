---
name: motion
description: Generate motion prompts for video generation
trigger: /motion {episode}
parameters:
  - name: episode
    description: Episode identifier (e.g., ep01, ep02)
    required: true
    type: string
    pattern: "^ep\\d{2}$"
---

# Motion Prompts

Creates concise motion prompts for AI video generation.

**Usage**: `/motion ep01`

**Prerequisites**: Sequence board approved

**Process**:

1. Load `sequence-board-prompt-ep{XX}.md`
2. Animator creates motion prompts (40-80 words each)
3. Director reviews
4. Save to `outputs/motion-prompt-ep{XX}.md`

**Output**: 2-3 motion prompts for video models (Runway, Pika, etc.)

**Next**: Generate videos with output prompts
