---
name: beatboard
description: Generate 9-panel beat board prompts (3x3 grid)
trigger: /beatboard {episode}
parameters:
  - name: episode
    description: Episode identifier (e.g., ep01, ep02)
    required: true
    type: string
    pattern: "^ep\\d{2}$"
---

# Beat Board (9-Panel Grid)

Generates 9 image prompts in 3x3 grid layout.

**Usage**: `/beatboard ep01`

**Prerequisites**: Beat breakdown approved

**Process**:

1. Load `beat-breakdown-ep{XX}.md`
2. Storyboard Artist creates 9 prompts
3. Director reviews
4. Save to `outputs/beat-board-prompt-ep{XX}.md`

**Output**: 9 prompts with grid positions (Row X, Column Y)

**Next**: `/sequence ep01`
