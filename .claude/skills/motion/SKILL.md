---
name: motion
description: Generate motion prompts for video generation
trigger: /motion
---

# Motion Prompt Generator

Generates motion prompts optimized for AI video generation models.

## Usage

```
/motion ep01
```

## What This Does

1. **Reads approved sequence board** from `outputs/sequence-board-prompt-ep{XX}.md`
2. **Calls Animator** to create motion prompts
3. **Director reviews** for clarity and physical plausibility
4. **Saves output** to `outputs/motion-prompt-ep{XX}.md`

## Prerequisites

- Sequence board exists and is approved

## Output

Creates `outputs/motion-prompt-ep{XX}.md` with:

- One motion prompt per sequence (40-80 words each)
- Clear direction and speed specifications
- Subject vs camera motion distinguished
- Physically realistic for 3-5 second duration

## Generation Targets

Use these prompts with:

- **Runway Gen-3**: High-quality cinematic video
- **Pika 1.5**: Creative motion effects
- **Stable Video Diffusion**: Open-source image-to-video
- **AnimateDiff**: Animation from static frames

## Recommended Workflow

1. Use Panel 1 from each sequence as reference image
2. Input motion prompt to video model
3. Generate 3-5 second video clip
4. Stitch clips together for final sequence

## Completion

This is the final stage. After approval, all storyboard prompts are ready for AI generation!
