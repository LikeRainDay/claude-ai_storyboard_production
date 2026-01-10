---
name: script
description: Generate a story script for an episode
trigger: /script
---

# Script Generator

Creates a complete story script for an episode, formatted for storyboarding and AI video production.

## Usage

```
/script ep02
```

Or with language specified:

```
/script ep02 --lang en-US
```

## What This Does

1. **Checks language preference** from `.agent-state.json` (default: Chinese)
2. **Prompts for story input**: concept, theme, genre, target length
3. **Calls Scriptwriter** to generate the script
4. **Saves output** to `script/ep{XX}-{title}.md`
5. **Updates state** in `.agent-state.json`

## Script Generation Process

### Step 1: Story Input

You'll be prompted for:

- **Story Concept**: Main idea or premise
- **Genre**: Fantasy, sci-fi, drama, romance, action, etc.
- **Connection**: Sequel to previous episode? Standalone? Same universe?
- **Target Length**: Short (5 scenes), Medium (10 scenes), Long (15+ scenes)

### Step 2: Outline Proposal

Scriptwriter proposes a brief scene outline for your approval.

### Step 3: Full Script Generation

After approval, generates complete script with:

- Scene headers (location, time of day)
- Visual descriptions
- Character actions and dialogue
- Character reference section
- Visual style recommendations

## Language Options

Supported languages (configurable in `.agent-state.json`):

- **zh-CN**: Chinese (Simplified) - 简体中文 [DEFAULT]
- **en-US**: English
- **ja-JP**: Japanese - 日本語
- **ko-KR**: Korean - 한국어

To change default language:

```
/config --lang en-US
```

To generate a specific episode in a different language:

```
/script ep02 --lang en-US
```

## Output

Creates `script/ep{XX}-{title}.md` with:

- Complete story script
- Scene-by-scene breakdown
- Character descriptions with visual traits
- Visual style recommendations

## Next Steps

After script generation:

1. Review the script
2. Request revisions if needed
3. When satisfied: `/breakdown ep{XX}` to start storyboarding

## Example

```
User: /script ep02

System: Language: Chinese (zh-CN)
        Episode: ep02

        Please provide:
        1. Story concept
        2. Genre
        3. Connection to ep01
        4. Target length

User: Continuation of ep01. Emma explores her powers.
      Genre: Urban fantasy. Medium length.

System: [Scriptwriter proposes outline]
        ...
        [User approves]
        ...
        ✓ Script complete: script/ep02-discovery.md
        → Ready for storyboarding: /breakdown ep02
```

## Script Format

Generated scripts follow this structure:

```markdown
# [Episode Title] - Episode {XX}

## Scene 1: [Location] ([Time])

[Visual description]
**CHARACTER**: "Dialogue"
[Actions]

---

## Scene 2: [Location] ([Time])

...

---

## Character Reference

**Character Name**

- Age: [age]
- Appearance: [detailed visual description]
- Personality: [traits]

---

## Visual Style Recommendation

- Style: [visual style keywords]
- Tone: [mood and atmosphere]
- Color Palette: [colors]
- Lighting: [lighting approach]
- Aspect Ratio: [16:9, etc.]
```

## Quality Guarantee

All scripts are:

- ✓ Visually descriptive (easy to storyboard)
- ✓ Well-structured (clear scenes)
- ✓ Character-focused (distinctive visual traits)
- ✓ Filmable (concrete actions, not abstract concepts)
- ✓ Language-appropriate (natural in target language)

## Tips for Best Results

1. **Be specific with your concept**: "A detective discovers a supernatural conspiracy" is better than "A detective story"
2. **Specify visual style early**: Helps scriptwriter tailor descriptions
3. **Provide character details**: If you have specific character visions, share them
4. **Mention inspirations**: "Like Blade Runner meets Ghost in the Shell" helps set the tone

## Workflow

Complete workflow from idea to video:

```
/script ep02 (Generate script)
    ↓
/breakdown ep02 (9 key beats)
    ↓
/beatboard ep02 (9 image prompts)
    ↓
/sequence ep02 (4-panel sequences)
    ↓
/motion ep02 (video prompts)
    ↓
AI Generation (Images & Videos)
```
