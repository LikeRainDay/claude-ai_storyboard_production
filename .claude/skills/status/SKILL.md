---
name: status
description: Show progress for all episodes
trigger: /status
---

# Project Status Viewer

Displays current progress for all episodes in the project.

## Usage

```
/status
```

## What This Does

1. **Scans** `script/` directory for episodes
2. **Checks** `outputs/` for generated files
3. **Reads** `.agent-state.json` for approval status
4. **Displays** comprehensive status table

## Output Format

For each episode:

```
Episode ep01: 觉醒 (Awakening)
├─ Script: ✓ script/ep01-awakening.md
├─ Stage 1: Beat Breakdown
│  ├─ File: [✓/✗] outputs/beat-breakdown-ep01.md
│  └─ Status: [✓ Approved / ✗ Not Approved / ⏸ In Progress]
├─ Stage 2: Beat Board (9-Panel)
│  ├─ File: [✓/✗] outputs/beat-board-prompt-ep01.md
│  └─ Status: [✓ Approved / ✗ Not Approved / ⏸ In Progress]
├─ Stage 3: Sequence Board (4-Panel)
│  ├─ File: [✓/✗] outputs/sequence-board-prompt-ep01.md
│  └─ Status: [✓ Approved / ✗ Not Approved / ⏸ In Progress]
└─ Stage 4: Motion Prompts
   ├─ File: [✓/✗] outputs/motion-prompt-ep01.md
   └─ Status: [✓ Approved / ✗ Not Approved / ⏸ In Progress]

Visual Style: anime, cinematic lighting, vibrant colors
Aspect Ratio: 16:9
```

## Suggested Next Steps

Based on current status, suggests what to do next:

- If no beat breakdown: `/breakdown ep01`
- If breakdown approved: `/beatboard ep01`
- If beat board approved: `/sequence ep01`
- If sequence approved: `/motion ep01`
- If all complete: Ready for AI generation!
