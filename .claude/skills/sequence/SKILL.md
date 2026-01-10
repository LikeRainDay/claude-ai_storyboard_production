---
name: sequence
description: Generate 4-panel sequence board prompts
trigger: /sequence
---

# Sequence Board Generator (4-Panel)

Generates 4-panel continuous sequence prompts that expand key beats into detailed action.

## Usage

```
/sequence ep01
```

## What This Does

1. **Reads approved beat board** from `outputs/beat-board-prompt-ep{XX}.md`
2. **Calls Storyboard Artist** to create 4-panel sequences
3. **Director reviews** for inheritance, continuity, and cinematography
4. **Saves output** to `outputs/sequence-board-prompt-ep{XX}.md`

## Prerequisites

- Beat board exists and is approved

## Output

Creates `outputs/sequence-board-prompt-ep{XX}.md` with:

- 2-3 sequences, each with exactly 4 panels
- Each sequence inherits character/setting/lighting from source beat
- Continuous motion and camera work
- Screen direction and cut safety maintained

## Critical Rules

- **Inheritance**: 4-panel sequences MUST inherit character appearance, setting, and lighting from the source 9-panel beat
- **Continuity**: Motion flows logically across all 4 panels
- **Cinematography**: Follows 180-degree rule, no jump cuts

## Next Step

After approval: `/motion ep01`
