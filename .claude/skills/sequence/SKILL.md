---
name: sequence
description: Generate 4-panel sequence boards from selected beats
trigger: /sequence {episode}
parameters:
  - name: episode
    description: Episode identifier (e.g., ep01, ep02)
    required: true
    type: string
    pattern: "^ep\\d{2}$"
---

# Sequence Board (4-Panel)

Expands selected beats into continuous 4-panel sequences.

**Usage**: `/sequence ep01`

**Prerequisites**: Beat board approved

**Process**:

1. Load `beat-board-prompt-ep{XX}.md`
2. Storyboard Artist expands 2-3 beats into 4-panel sequences
3. Director reviews
4. Save to `outputs/sequence-board-prompt-ep{XX}.md`

**Output**: 2-3 sequences, each with 4 continuous panels

**Next**: `/motion ep01`
