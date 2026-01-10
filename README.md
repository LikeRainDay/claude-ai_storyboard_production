# AI Storyboard Production System

An AI-powered storyboard artist system built with Claude Agent + Skill architecture for automating film storyboarding workflows.

## System Overview

This system coordinates a **Producer** with four specialized subagents to automatically generate structured storyboard prompts:

```
Producer Agent (CLAUDE.md)
├── Scriptwriter — Generates story scripts (multi-language support)
├── Storyboard Artist — Creates beat breakdowns, 9-panel, 4-panel prompts
├── Director — Reviews all outputs for quality control
└── Animator — Generates motion prompts for video generation
```

### Core Value

- **Efficiency Boost**: Automated workflow from concept to prompts, reducing manual work by ~80%
- **Consistency Guarantee**: Strict character/scene/lighting inheritance reduces AI generation randomness
- **Professional Standards**: Based on film storyboarding methodology with cinematography and editing principles
- **Quality Control**: Automatic director review with revision loops
- **Resumable**: Document-driven, progress can be resumed after interruption via `/status`
- **Multi-language**: Supports Chinese, English, Japanese, Korean script generation

## Complete Workflow

### Full 5-Stage Pipeline

```
0. Script Generation (Story Creation)
   Input: Story concept, genre, theme
   Output: Complete script with scenes, characters, dialogue
   Language: Configurable (Chinese, English, Japanese, Korean)

1. Beat Breakdown (9 Key Narrative Moments)
   Input: Script + visual style configuration
   Output: 9 key narrative anchor points
   Review: Director checks completeness, clarity, selection quality

2. Beat Board (9-Panel Storyboard)
   Input: Approved beat breakdown
   Output: 9 static image prompts (visual baseline)
   Review: Director checks consistency, coverage, prompt format

3. Sequence Board (4-Panel Storyboard)
   Input: Approved beat board
   Output: Continuous 4-shot sequence prompts (expanded key moments)
   Review: Director checks motion continuity, axis stability, inheritance rules

4. Motion Prompts (Video Generation)
   Input: Approved sequence board
   Output: Dynamic motion prompts for video models
   Review: Director checks conciseness, physical plausibility, focus

All stages in English for optimal AI compatibility
```

### CLI Commands (Skills)

System implements CLI commands via **Skills** with intelligent auto-completion:

```bash
/script ep02      # Generate story script (supports multi-language)
/breakdown ep01   # Generate beat breakdown
/beatboard ep01   # Generate 9-panel prompts
/sequence ep01    # Generate 4-panel prompts
/motion ep01      # Generate motion prompts
/status           # View all episode progress
/config           # Configure/update visual style
/language zh-CN   # Set language preference
```

**Command Skills** (defined in `.claude/skills/`):

- `script/` - Script generation command
- `breakdown/` - Beat breakdown command
- `beatboard/` - 9-panel generation command
- `sequence/` - 4-panel sequence command
- `motion/` - Motion prompt command
- `status/` - Progress viewer command
- `config/` - Configuration command
- `language/` - Language preference command

**Methodology Skills** (provide professional knowledge):

- `film-storyboard-skill/` - Storyboarding methodology, prompt guide, templates
- `storyboard-review-skill/` - Director review standards
- `animator-skill/` - Motion prompt methodology

## Project Structure

```
project/
├── script/                              # Script source files (user generated)
│   ├── ep01-awakening.md
│   └── ep02-revelation.md
│
├── outputs/                             # Generated artifacts (auto-created)
│   ├── beat-breakdown-ep01.md           # Beat breakdown
│   ├── beat-board-prompt-ep01.md        # 9-panel prompts
│   ├── sequence-board-prompt-ep01.md    # 4-panel prompts
│   ├── motion-prompt-ep01.md            # Motion prompts
│   └── [same files for ep02...]
│
├── .agent-state.json                    # Agent state tracking (auto-created)
│
└── .claude/                             # Claude configuration
    ├── CLAUDE.md                        # Main Agent: Producer
    │
    ├── agents/                          # Subagent configs
    │   ├── scriptwriter.md              # Scriptwriter (multi-language)
    │   ├── storyboard-artist.md         # Storyboard Artist
    │   ├── director.md                  # Director
    │   └── animator.md                  # Animator
    │
    └── skills/                          # Skill packages
        ├── script/                      # Command: /script
        │   └── SKILL.md
        ├── breakdown/                   # Command: /breakdown
        │   └── SKILL.md
        ├── beatboard/                   # Command: /beatboard
        │   └── SKILL.md
        ├── sequence/                    # Command: /sequence
        │   └── SKILL.md
        ├── motion/                      # Command: /motion
        │   └── SKILL.md
        ├── status/                      # Command: /status
        │   └── SKILL.md
        ├── config/                      # Command: /config
        │   └── SKILL.md
        ├── language/                    # Command: /language
        │   └── SKILL.md
        │
        ├── film-storyboard-skill/       # Storyboard Artist skill
        │   ├── SKILL.md
        │   ├── storyboard-methodology-playbook.md  # Methodology
        │   ├── gemini-image-prompt-guide.md        # Prompt writing guide
        │   └── templates/
        │       ├── beat-breakdown-template.md
        │       ├── beat-board-template.md
        │       └── sequence-board-template.md
        │
        ├── storyboard-review-skill/     # Director skill
        │   ├── SKILL.md
        │   └── review-checklist.md      # Review checklist
        │
        └── animator-skill/              # Animator skill
            ├── SKILL.md
            ├── motion-prompt-methodology.md  # Motion methodology
            └── templates/
                └── motion-prompt-template.md
```

## Quick Start

### 1. Set Language Preference (Optional)

Default is Chinese (zh-CN). To change:

```bash
/language en-US   # English
/language ja-JP   # Japanese
/language ko-KR   # Korean
```

### 2. Generate or Upload Script

**Option A: Generate with AI**

```bash
/script ep01
```

System will prompt for:

- Story concept/theme
- Genre
- Target length
- Character details

**Option B: Upload Manually**
Place your script in `script/` directory with naming format: `ep{XX}-{title}.md`

Example script structure:

```markdown
# Episode Title - Episode 01

## Scene 1: Location (Time of Day)

Visual description...
**CHARACTER NAME** (age, appearance): Action description.
**CHARACTER NAME**: "Dialogue."

## Scene 2: Location (Time of Day)

...

## Character Reference

**Character Name**

- Age: [age]
- Appearance: [detailed visual description]
  ...

## Visual Style Recommendation

- Style: anime, cinematic lighting
- Aspect Ratio: 16:9
```

### 3. Configure Visual Style

```bash
/config ep01
```

Set:

- **Style Keywords**: "anime, cinematic lighting, vibrant colors"
- **Aspect Ratio**: 16:9, 9:16, 1:1, etc.
- **Target Model**: Gemini Imagen 3, Midjourney v6, etc.

### 4. Run Production Pipeline

```bash
/breakdown ep01    # Generate beat breakdown
# → Director auto-reviews
# → PASS: continue; FAIL: revise + re-review

/beatboard ep01    # Generate 9-panel prompts
# → Director auto-reviews
# → PASS: continue

/sequence ep01     # Generate 4-panel prompts
# → Director auto-reviews
# → PASS: continue

/motion ep01       # Generate motion prompts
# → Director auto-reviews
# → PASS: complete
```

### 5. Use Generated Prompts

- **9-Panel Prompts** (`beat-board-prompt-ep01.md`):

  - Generate 9 key frame images
  - Copy directly to Gemini Imagen 3, Midjourney, etc.

- **4-Panel Prompts** (`sequence-board-prompt-ep01.md`):

  - Generate continuous shot sequences
  - Use for image-to-image or as reference

- **Motion Prompts** (`motion-prompt-ep01.md`):
  - Use with Runway Gen-3, Pika, Stable Video Diffusion
  - Recommended: image-to-video mode (use 4-panel Panel 1 as reference)

## Language Support

### Supported Languages

- **zh-CN**: Chinese (Simplified) - 简体中文 [DEFAULT]
- **en-US**: English (United States)
- **ja-JP**: Japanese - 日本語
- **ko-KR**: Korean - 한국어

### Language Scope

**Scripts and Narrative Content**: Use your selected language

- Story scripts
- Character dialogue
- Scene descriptions
- Character reference notes

**Image and Video Prompts**: Always English

- Beat board (9-panel) prompts
- Sequence board (4-panel) prompts
- Motion prompts
- All visual generation prompts use English for optimal AI model compatibility

### Example Multi-Language Workflow

```bash
# Set global language to English
/language en-US

# Generate English script
/script ep01
# → Script generated in English

# Generate storyboard prompts (auto in English)
/breakdown ep01
/beatboard ep01
# → All visual prompts in English for AI models

# Create episode 2 in Japanese
/script ep02 --lang ja-JP
# → Script in Japanese, but prompts still in English
```

## Core Features

### 1. Agent + Skill Decoupling

- **Agents handle coordination**: Producer manages workflow, Scriptwriter generates scripts, Storyboard Artist generates prompts, Director reviews
- **Skills provide knowledge**: Methodology, templates, writing guides
- **Advantage**: Can replace methodology or style without changing Agent configs

### 2. Progressive Refinement Logic

```
Script Generation (Story foundation)
  ↓ Inherits narrative structure
Beat Breakdown (9 anchor points)
  ↓ Inherits narrative structure
9-Panel Board (9 key frames) — Establishes visual baseline (character, scene, lighting)
  ↓ Inherits visual elements
4-Panel Board (continuous shots) — Expands action sequences, maintains consistency
  ↓ Inherits subject and motion
Motion Prompts — Optimized for video generation
```

### 3. Director Review Loop

After each stage, Director reviews against `review-checklist.md`:

- **PASS**: Meets standards, proceed to next stage
- **FAIL**: Lists specific issues, revision required, re-review

Loops until approved, or escalates to user after 3 failures.

### 4. Resumable Subagents (Context Continuity)

- Producer maintains each subagent's `agentId` in `.agent-state.json`
- Subsequent calls use `resume` to restore context
- Storyboard Artist remembers 9-panel when creating 4-panel

### 5. Inheritance Mechanism

**Critical Rule**: 4-panel must inherit character appearance, scene, lighting from 9-panel

**Example**:

```
9-Panel Beat 3: "A woman with silver hair wearing a red coat..."
4-Panel Sequence from Beat 3, Panel 1: "The woman with silver hair in the red coat turns..."
```

Strict inheritance dramatically reduces character appearance variation in AI generation.

### 6. Multi-Episode Support

- Independent state tracking per episode
- File naming uses episode identifier: `ep01`, `ep02`, `ep15`
- Can work on multiple episodes in parallel

## Core Methodology

### 4C Framework

1. **Clear**: Every prompt is unambiguous and immediately understandable

   - Specific shot types, camera angles, framing
   - Concrete character and scene descriptions

2. **Concise**: Detailed but not bloated

   - Static prompts: 80-150 words
   - Motion prompts: 40-80 words

3. **Consistent**: Maintains visual continuity

   - Identical character appearance
   - Stable scene details
   - Unified lighting style

4. **Progressive**: Layer-by-layer refinement without contradiction
   - 9-panel establishes visual language
   - 4-panel inherits and expands
   - Motion prompts add temporal dimension

### Narrative Descriptive Style

**❌ Keyword Stuffing**:

```
woman, red dress, beach, sunset, 8k, detailed, cinematic
```

**✓ Narrative Description**:

```
A woman in a flowing red dress stands on a sandy beach at sunset,
warm golden light illuminating her profile. Soft romantic lighting,
cinematic composition.
```

Modern AI models (Gemini Imagen 3, etc.) understand natural language better than keyword lists.

### Character Consistency Pattern

**Canonical Definition** (Beat Breakdown):

```
Emma: 25-year-old woman, long silver hair, usually wears deep red coat, introverted but resilient
```

**9-Panel Usage** (All 9 panels):

```
Panel 1: "A 25-year-old woman with long silver hair wearing a deep red coat..."
Panel 5: "A 25-year-old woman with long silver hair wearing a deep red coat..."
Panel 9: "A 25-year-old woman with long silver hair wearing a deep red coat..."
```

**4-Panel Inheritance**:

```
Sequence from Beat 3, Panel 1: "The woman with silver hair in the deep red coat..."
```

## Usage Recommendations

### Model Selection

This system runs in **Claude Code**, can be configured with different LLMs:

- **Recommended**: Claude Opus / Sonnet (strong comprehension, long context)
- **Alternative**: Gemini 3 Pro, Kimi K2, GLM 4.7, etc. (requires API configuration)

**Note**: Model capability directly affects output quality. Test with a short script before full production.

### Image Generation Models

Prompts optimized for:

- **Static Images**: Gemini Imagen 3, Midjourney v6, DALL-E 3
- **Video**: Runway Gen-3, Pika 1.5, Stable Video Diffusion, AnimateDiff

### Best Practices

1. **Start with short script**: Test 1 episode to validate workflow and quality
2. **Clear visual style**: Configure specific style keywords (anime, realistic, cyberpunk, etc.)
3. **Check inheritance**: Verify 4-panel correctly inherits 9-panel character appearance
4. **Iterate and optimize**: Generated prompts are starting points, adjust based on actual generation results
5. **Save intermediate artifacts**: All `outputs/` files are editable, can manually refine before generation

## FAQ

### Q: Why 9 key frames?

A: 9 balances coverage and manageability. Enough to show complete story arc (beginning, development, end), not too overwhelming.

### Q: Can I customize templates or methodology?

A: Yes! Replace files in `skills/`. For example:

- Switch to comic storyboarding → modify `storyboard-methodology-playbook.md`
- Support Midjourney syntax → modify `gemini-image-prompt-guide.md`

### Q: What if Director keeps rejecting?

A: After 3 failures, escalates to user. Possible causes:

- Insufficient script details
- Unclear visual style configuration
- Model comprehension limitations

Manual intervention recommended with additional context.

### Q: Generated images have inconsistent characters?

A: Check:

1. Are 9-panel character descriptions identical?
2. Do 4-panel correctly inherit 9-panel character descriptions?
3. Does AI model support long prompts?
4. Emphasize distinctive features: "with distinctive silver hair and amber eyes"

### Q: Can I skip a stage?

A: Not recommended. Progressive refinement is core methodology. Skipping loses inheritance information and consistency guarantees.

### Q: Can I generate scripts in different languages?

A: Yes! Use `/language` to set default, or specify per-episode:

```bash
/language zh-CN        # Set default to Chinese
/script ep01           # Generates in Chinese
/script ep02 --lang en-US  # Generate ep02 in English
```

All image/video prompts remain in English for AI compatibility.

## Technical Implementation

### Resumable Subagents Mechanism

`.agent-state.json` structure:

```json
{
  "scriptwriter_id": "agent_abc123",
  "storyboard_artist_id": "agent_def456",
  "director_id": "agent_ghi789",
  "animator_id": "agent_jkl012",
  "language": "zh-CN",
  "episodes": {
    "ep01": {
      "current_stage": "beatboard",
      "breakdown_approved": true,
      "beatboard_approved": false,
      "visual_style": "anime, cinematic lighting, vibrant colors",
      "language": "zh-CN"
    }
  }
}
```

### Review Loop Pseudocode

```
function generate_stage(episode, stage):
    output = call_subagent(storyboard_artist, task)

    while True:
        review = call_subagent(director, output)

        if review.verdict == "PASS":
            save_state(stage, approved=True)
            break
        else:
            output = call_subagent(storyboard_artist, revise_with_feedback)
            attempt_count += 1

            if attempt_count >= 3:
                escalate_to_user(review.feedback)
                break
```

## Extension Possibilities

This system's architecture supports various extensions:

- **Other Media**: Advertising, game cinematics, architectural visualization
- **Other Styles**: Photorealistic, watercolor, pixel art
- **Other Languages**: Any language (currently supports zh-CN, en-US, ja-JP, ko-KR)
- **Auto-generation**: Integrate Gemini/Midjourney API for automatic image generation
- **Video Assembly**: Automatically stitch generated video clips into complete sequences

## License and Attribution

Built on professional film storyboarding methodology and AI image/video generation best practices.

Suitable for any structured, consistency-focused AI visual content production scenario.

---

**Get Started**: Generate or upload script to `script/`, run `/script ep01` or `/breakdown ep01`

**Need Help**: Check `.claude/skills/` for methodology documentation, or use `/status` to check current progress

**Documentation**: 20,000+ words of professional methodology and guides included
