---
name: Film Storyboard Skill
description: Professional storyboarding methodology and AI image prompt engineering for visual storytelling
version: 1.0.0
---

# Film Storyboard Skill

This skill package equips the Storyboard Artist with professional film and animation storyboarding methodology, optimized for AI image generation workflows.

## Skill Components

### 1. **storyboard-methodology-playbook.md**

Comprehensive guide to storyboard principles:

- Clear, concise, consistent, progressive refinement methodology
- Shot composition and cinematography rules
- Character and scene continuity management
- Narrative beat selection strategies
- Visual storytelling best practices

### 2. **gemini-image-prompt-guide.md**

Specialized prompt writing guide for AI image models (Gemini Imagen 3 and similar):

- Narrative descriptive style vs keyword stuffing
- Optimal prompt structure and length
- Character consistency techniques
- Lighting and mood specification
- Common pitfalls and how to avoid them

### 3. **Templates**

Structured output formats:

- `beat-breakdown-template.md` — Format for identifying story anchor points
- `beat-board-template.md` — Format for 9-panel visual baseline prompts
- `sequence-board-template.md` — Format for 4-panel continuous sequence prompts

## When to Use This Skill

The Storyboard Artist should reference this skill when:

- Analyzing scripts for beat breakdown
- Selecting the 9 key narrative beats
- Writing image generation prompts (beat board or sequence board)
- Ensuring character and scene consistency
- Following cinematography and composition rules
- Resolving Director feedback about methodology violations

## Skill Activation

This skill is **always active** for the Storyboard Artist agent. All outputs must conform to the methodology and templates defined here.

## Key Principles

### The Four Pillars of Storyboard Quality

1. **Clear**: Every prompt should unambiguously describe what will be generated

   - Specific shot types, camera angles, and framing
   - Concrete character descriptions (not "a person")
   - Defined locations (not "somewhere")

2. **Concise**: Detailed but not bloated

   - Static prompts: 80-150 words
   - Focus on visual essentials
   - Avoid narrative exposition

3. **Consistent**: Maintain visual continuity

   - Characters look identical across prompts
   - Settings maintain architectural coherence
   - Lighting style remains stable
   - Visual style tokens (e.g., "anime", "cinematic") applied uniformly

4. **Progressive**: Build on previous work
   - Beat breakdown establishes narrative structure
   - Beat board (9-panel) establishes visual language
   - Sequence board (4-panel) inherits and expands
   - Each stage refines, never contradicts

### The Inheritance Rule

**Critical**: When creating 4-panel sequences, the Storyboard Artist must **inherit** character appearance, setting, and lighting from the corresponding 9-panel beat prompt.

**Example**:

- **Beat 3 (9-panel)**: "A young woman with long silver hair wearing a crimson coat..."
- **Sequence from Beat 3, Panel 1 (4-panel)**: "A young woman with long silver hair wearing a crimson coat turns toward..."

The inherited elements anchor consistency and reduce generation errors.

## Template Compliance

All outputs must strictly follow the template formats. The Director will reject work that deviates from template structure.

## Quality Assurance

The Director agent uses this same methodology to review the Storyboard Artist's work. Both agents share the same quality standards to ensure alignment.

## Methodology Source

The storyboard principles in this skill are based on:

- Professional film and animation pre-production practices
- AI image generation model optimization research
- Iterative testing with Gemini Imagen 3, Midjourney, and similar models
- Continuity management techniques from VFX and animation pipelines

## Customization Note

This skill package can be replaced or extended to support:

- Different visual styles (e.g., comic book, architectural visualization)
- Different AI image models (e.g., DALL-E, Midjourney with their specific syntax)
- Different narrative structures (e.g., documentary, commercial, game cinematics)

To customize, modify the methodology playbook and prompt guide while maintaining the template structures.

---

**Usage**: The Storyboard Artist agent automatically references this skill. No manual invocation required.
