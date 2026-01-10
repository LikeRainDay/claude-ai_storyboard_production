---
name: breakdown
description: Generate beat breakdown (9 key narrative moments) from script
trigger: /breakdown {episode}
parameters:
  - name: episode
    description: Episode identifier (e.g., ep01, ep02)
    required: true
    type: string
    pattern: "^ep\\d{2}$"
---

# Beat Breakdown

Analyzes script and generates 9 key narrative anchor points.

**Usage**: `/breakdown ep01`

**Process**:

1. Load script from `script/ep{XX}-*.md`
2. Storyboard Artist selects 9 beats
3. Director reviews
4. Save to `outputs/beat-breakdown-ep{XX}.md`

**Next**: `/beatboard ep01`
