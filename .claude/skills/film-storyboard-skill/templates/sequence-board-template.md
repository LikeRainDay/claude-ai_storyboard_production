# Sequence Board - 4-Panel Continuous Prompts

---

**Episode**: ep{XX}
**Title**: [Episode Title]
**Generated**: [Date/Time]
**Visual Style**: [Style keywords]
**Aspect Ratio**: [e.g., 16:9, 9:16, 1:1]
**Target Model**: [e.g., Gemini Imagen 3]

---

## Purpose

This sequence board expands selected beats from the beat board into **continuous 4-panel sequences**. Each sequence shows:

- Progressive action across 4 consecutive shots
- Motion and camera continuity
- Smooth transitions between panels

These sequences are designed for image-to-image generation or as reference for motion prompts.

**Inheritance Rule**: All panels must inherit character appearance, setting, and lighting from their source beat in the beat board.

---

## Sequence 1: [Sequence Name/Title]

**Source Beat**: Beat [X] from beat-board-ep{XX}.md
**Narrative Context**: [What happens across these 4 panels]
**Duration**: [Estimated real-time duration, e.g., "8-10 seconds"]

### Panel 1

**Shot**: [Shot type], [camera angle]
**Transition from previous**: [N/A for first panel] | [e.g., "Cut from previous sequence" or "Continues from Beat X"]

**Image Prompt**:

```
[Shot type], [camera angle]. [Subject description - INHERITED from source beat] [action/pose] [setting - INHERITED]. [Lighting - INHERITED]. [Style keywords].

[Full prompt, 80-150 words, maintaining character, setting, lighting from source beat]
```

### Panel 2

**Shot**: [Shot type], [camera angle]
**Transition from Panel 1**: [e.g., "Camera pans right" or "Cut to different angle" or "Continuous action"]

**Image Prompt**:

```
[Full prompt, 80-150 words]
```

**Continuity Notes**: [e.g., "Character moved from left to center", "Camera followed motion"]

### Panel 3

**Shot**: [Shot type], [camera angle]
**Transition from Panel 2**: [e.g., "Camera pushes in" or "Character continues movement"]

**Image Prompt**:

```
[Full prompt, 80-150 words]
```

**Continuity Notes**:

### Panel 4

**Shot**: [Shot type], [camera angle]
**Transition from Panel 3**:

**Image Prompt**:

```
[Full prompt, 80-150 words]
```

**Continuity Notes**:

---

### Sequence Continuity Check

- [ ] Character appearance consistent across all 4 panels
- [ ] Character appearance matches source Beat [X]
- [ ] Setting consistent or logically transitions
- [ ] Screen direction maintained (180-degree rule)
- [ ] Motion is physically plausible within duration
- [ ] No jump cuts (same shot, slightly different angle)
- [ ] Smooth transitions between panels
- [ ] Camera movement clearly described if present

---

## Sequence 2: [Sequence Name/Title]

**Source Beat**: Beat [Y]
**Narrative Context**:
**Duration**:

### Panel 1

[Same structure as Sequence 1]

### Panel 2

[...]

### Panel 3

[...]

### Panel 4

[...]

---

### Sequence Continuity Check

[Same checklist as Sequence 1]

---

## Sequence 3: [Sequence Name/Title]

**Source Beat**: Beat [Z]
**Narrative Context**:
**Duration**:

[Same structure as above]

---

## Overall Continuity Summary

### Character Consistency Across All Sequences

**[Character Name 1]**:

- Source Beat Description: [Canonical from beat board]
- Appears in: Sequence [#], Panels [#]
- Inheritance Check: ✓/✗ [All panels maintain identical physical descriptors]

**[Character Name 2]**:

- Source Beat Description:
- Appears in:
- Inheritance Check: ✓/✗

### Cinematography Notes

- **Screen Direction**: [e.g., "Character moving left-to-right maintained in Seq 1 and 3"]
- **Camera Approach**: [e.g., "Mix of static shots and slow pans, no handheld"]
- **Transitions**: [e.g., "Mostly cuts, one camera pan in Seq 2"]

### Lighting Consistency

- [e.g., "All sequences use soft natural window light from left, maintaining beat board lighting"]
- [e.g., "Seq 3 transitions from day to night, motivating lighting change"]

---

## Production Notes

[Any special considerations for image generation, known challenges, creative decisions]

---

**Status**: ✓ Ready for Image Generation or Motion Prompt Creation
**Next Steps**:

1. Option A: Generate 4-panel sequences as static images
2. Option B: Use `/motion ep{XX}` to create motion prompts for video generation
3. Option C: Use these as reference for image-to-video generation
