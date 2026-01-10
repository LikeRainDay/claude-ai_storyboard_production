---
name: breakdown
description: Generate beat breakdown (9 key narrative moments) from script
trigger: /breakdown
---

# Beat Breakdown Generator

Analyzes the script and generates a structured beat breakdown with 9 key narrative anchor points.

## Usage

```
/breakdown ep01
```

## What This Does

1. **Loads the script** from `script/ep{XX}-*.md`
2. **Calls Storyboard Artist** to analyze and select 9 key beats
3. **Director reviews** the breakdown for quality
4. **Saves output** to `outputs/beat-breakdown-ep{XX}.md`
5. **Updates state** in `.agent-state.json`

## Prerequisites

- Script file exists in `script/` directory (e.g., `ep01-awakening.md`)
- Visual style configured (will prompt if not set)

## Output

Creates `outputs/beat-breakdown-ep{XX}.md` with:

- 9 key narrative beats spanning the full story arc
- Scene references and timestamps
- Narrative purpose for each beat
- Character and location tracking

## Next Step

After approval: `/beatboard ep01`
