# Motion Prompts for Video Generation

---

**Episode**: ep{XX}
**Title**: [Episode Title]
**Generated**: [Date/Time]
**Source**: sequence-board-prompt-ep{XX}.md
**Target Models**: [e.g., Runway Gen-3, Pika 1.5, Stable Video Diffusion]
**Typical Duration**: 3-5 seconds per clip

---

## Purpose

Motion prompts transform static 4-panel sequences into dynamic descriptions for AI video generation models. Each prompt describes:

- **Primary motion**: The main action or movement
- **Direction**: Where the motion goes
- **Camera movement**: How the camera behaves (if it moves)
- **Pacing**: Speed and style of motion
- **Duration**: Target video length

These prompts are optimized for brevity and clarity — video models perform better with focused instructions than exhaustive descriptions.

---

## Motion Prompt 1: [Sequence Name/Title]

**Source Sequence**: Sequence 1 from sequence-board-ep{XX}.md
**Narrative Context**: [Brief description of what happens in this sequence]
**Target Duration**: [e.g., 4 seconds]

**Motion Prompt**:

```
[Subject description - simplified] [primary motion] [direction] [+ camera movement if any].
[Camera specification]. [Pacing descriptors]. [Duration].

[Full motion prompt, 40-80 words, focused on motion rather than exhaustive scene description]
```

**Motion Breakdown**:

- **Primary Motion**: [e.g., "Character walks forward"]
- **Direction**: [e.g., "Left to right across frame"]
- **Camera**: [e.g., "Static" or "Pans right to follow"]
- **Pacing**: [e.g., "Slow, deliberate"]

**Technical Notes**: [Optional: specific considerations for generation, e.g., "Use first panel of sequence as reference frame for image-to-video"]

---

## Motion Prompt 2: [Sequence Name/Title]

**Source Sequence**: Sequence 2
**Narrative Context**:
**Target Duration**:

**Motion Prompt**:

```
[Full prompt, 40-80 words]
```

**Motion Breakdown**:

- **Primary Motion**:
- **Direction**:
- **Camera**:
- **Pacing**:

**Technical Notes**:

---

## Motion Prompt 3: [Sequence Name/Title]

**Source Sequence**: Sequence 3
**Narrative Context**:
**Target Duration**:

**Motion Prompt**:

```
[Full prompt, 40-80 words]
```

**Motion Breakdown**:

- **Primary Motion**:
- **Direction**:
- **Camera**:
- **Pacing**:

**Technical Notes**:

---

## Subject Consistency Check

**[Character Name 1]**:

- **Source Description** (from sequence board): [Full canonical description]
- **Motion Prompt Usage**: [Simplified identifiers used, e.g., "silver-haired woman in crimson coat"]
- **Appears in**: Motion Prompt [#]
- **Consistency**: ✓/✗ [Key identifiers maintained]

**[Character Name 2]**:

- **Source Description**:
- **Motion Prompt Usage**:
- **Appears in**:
- **Consistency**: ✓/✗

---

## Motion Quality Check

- [ ] Each prompt is 40-80 words (concise, motion-focused)
- [ ] ONE primary motion per prompt (not multiple competing actions)
- [ ] Motion direction clearly specified (left to right, toward camera, etc.)
- [ ] Speed/pacing indicated (slow, fast, gradual, etc.)
- [ ] Subject vs camera motion distinguished
- [ ] Camera movement type specified if camera moves (pan, dolly, static, etc.)
- [ ] Motion is physically plausible for stated duration
- [ ] Subject descriptions match source sequence board
- [ ] Duration specified for each prompt

---

## Video Generation Workflow

### Option A: Text-to-Video (Direct)

1. Input motion prompt directly into video generation model
2. Model generates video from text description
3. Review output for quality and consistency

### Option B: Image-to-Video (Reference Frame)

1. Use first panel from corresponding sequence as reference image
2. Input motion prompt to guide motion from that starting frame
3. Model generates video that evolves from the reference image
4. Typically yields more consistent results with storyboard aesthetic

**Recommended**: Option B (Image-to-Video) for better visual consistency with your storyboard style.

---

## Generation Settings (Model-Specific)

### Runway Gen-3

- **Duration**: 5-10 seconds per prompt
- **Motion Strength**: Medium (adjust if motion too subtle or exaggerated)
- **Reference Frame**: Use Panel 1 of sequence for image-to-video mode

### Pika 1.5

- **Duration**: 3-5 seconds per prompt
- **Motion Parameter**: 1-3 (start conservative, increase if needed)
- **Camera Control**: Enable for prompts with specific camera movements

### Stable Video Diffusion

- **Duration**: 2-4 seconds (model limitation)
- **Motion Bucket**: Medium-High
- **Frames**: 25 FPS recommended
- **Reference Frame**: Required (use Panel 1 of sequence)

### AnimateDiff

- **Duration**: 3-5 seconds
- **Motion Module**: Use appropriate motion LoRA for style
- **Reference Frames**: Use multiple panels from sequence as keyframes

---

## Post-Generation Review

After generating videos, check for:

- [ ] **Motion matches prompt**: Action performed as described
- [ ] **Direction correct**: Movement goes the specified direction
- [ ] **Pacing appropriate**: Speed matches descriptors (slow, fast, etc.)
- [ ] **No artifacts**: Clean motion, no warping or distortion
- [ ] **Character consistency**: Subject appearance stable throughout clip
- [ ] **Physical plausibility**: Motion looks realistic (unless stylized intentionally)

If issues found:

1. **Adjust prompt**: Simplify or clarify motion description
2. **Adjust settings**: Change motion strength, duration, or reference frame
3. **Regenerate**: Try again with refined prompt/settings
4. **Escalate**: If persistent issues, may need to revise source sequence board

---

## Notes

[Any creative decisions, generation challenges encountered, or recommendations for future iterations]

---

**Status**: ✓ Ready for Video Generation
**Next Steps**:

1. Generate videos using motion prompts
2. Review output quality
3. Refine prompts if needed and regenerate
4. Assemble final video sequence
