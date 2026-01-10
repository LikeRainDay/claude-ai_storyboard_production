# Storyboard Review Checklist

Comprehensive quality criteria for reviewing outputs at each production stage.

---

## Stage 1: Beat Breakdown Review

**Artifact**: `beat-breakdown-ep{XX}.md`

### Count and Completeness

- [ ] **Exactly 9 beats selected** (not 8, not 10, exactly 9)
- [ ] All 9 beats have **beat number** (1-9)
- [ ] All 9 beats have **scene reference** (page, scene number, or timestamp)
- [ ] All 9 beats have **description** (not blank or placeholder)
- [ ] All 9 beats have **narrative purpose** (explains why this beat matters)

### Coverage and Distribution

- [ ] **Beginning covered**: Beats 1-3 include setup and inciting incident
- [ ] **Middle covered**: Beats 4-6 include rising action and complications
- [ ] **End covered**: Beats 7-9 include climax and resolution
- [ ] **Reasonable spacing**: Beats distributed across timeline (not all clustered)
- [ ] **Complete arc**: Together, the 9 beats tell the full story

### Clarity and Specificity

- [ ] **No vague descriptions**: Each beat describes a specific event
  - ❌ Fail: "Something happens to the character"
  - ✓ Pass: "Maya discovers the hidden map in her grandmother's journal"
- [ ] **Concrete actions**: Descriptions use active, tangible events
- [ ] **Understandable standalone**: Each beat makes sense without extensive context

### Selection Quality

- [ ] **Turning points**: Beats are narrative pivots, not filler moments
- [ ] **Visual potential**: Each beat can be represented in a compelling image
- [ ] **Story-essential**: Removing a beat would create a gap in narrative understanding
- [ ] **Emotional significance**: Beats capture moments of heightened emotion or tension

### Character and Location Tracking

- [ ] **Key characters listed**: All recurring characters identified with canonical descriptions
- [ ] **Key locations listed**: All recurring settings identified
- [ ] **Consistency foundation**: Information provided is sufficient for maintaining continuity in later stages

### Common Failure Patterns

- ❌ Wrong beat count (7, 10, 12 beats instead of exactly 9)
- ❌ Vague descriptions ("a scene", "something happens", "character does stuff")
- ❌ Missing sections (e.g., no climax beats, no setup beats)
- ❌ Trivial moments (beats describe unimportant actions)
- ❌ Clustered beats (all 9 beats in the first third of the story)

---

## Stage 2: Beat Board (9-Panel) Review

**Artifact**: `beat-board-prompt-ep{XX}.md`

### Count and Structure

- [ ] **Exactly 9 prompts** (one per beat from breakdown)
- [ ] Each prompt has **beat reference** (references corresponding beat from breakdown)
- [ ] Each prompt has **narrative context** (explains what's happening)

### Prompt Format and Style

- [ ] **Narrative descriptive style**: Flowing sentences, not keyword lists
  - ❌ Fail: "woman, red dress, beach, sunset, 8k, detailed"
  - ✓ Pass: "A woman in a red dress stands on a beach at sunset..."
- [ ] **Appropriate length**: Each prompt 80-150 words
  - Too short (<60 words) → lacks detail
  - Too long (>180 words) → bloated, unfocused
- [ ] **Shot specifications**: Each prompt includes shot type and camera angle
  - Required: "Medium shot, eye-level" or similar

### Clarity (C1 of 4C Framework)

- [ ] **Subject clearly defined**: No ambiguity about who/what the main subject is
- [ ] **Action/pose specified**: Subject's positioning and action described
- [ ] **Setting detailed**: Location includes 2-4 distinct features
- [ ] **Lighting described**: Direction, quality, and mood of lighting specified
- [ ] **No contradictions**: Elements don't conflict (e.g., "bright sunny day in dark room")

### Consistency (C3 of 4C Framework)

- [ ] **Character appearance identical**: Same character described identically across all prompts
  - Example check: If Prompt 1 says "long silver hair", Prompt 5 must also say "long silver hair"
  - Look for: hair, eyes, clothing, distinguishing marks
- [ ] **Setting consistency**: If a location appears in multiple prompts, details align
- [ ] **Style keywords uniform**: Same style tokens in all prompts
  - Example: If Prompt 1 uses "anime style, cinematic lighting", all prompts should use this
- [ ] **Lighting approach coherent**: Overall lighting philosophy maintained (unless story requires change)

### Coverage and Alignment

- [ ] **Beats match breakdown**: Each panel corresponds to the correct beat from Stage 1
- [ ] **Visual storytelling**: Together, the 9 panels tell the episode's story visually
- [ ] **Diversity of shots**: Mix of wide, medium, close-up (not all the same shot type)

### Style Token Application

- [ ] **Project style applied**: Visual style from project configuration used in all prompts
- [ ] **Aspect ratio noted**: Specified in metadata (e.g., 16:9, 1:1)
- [ ] **Target model noted**: AI model identified (e.g., Gemini Imagen 3)

### Common Failure Patterns

- ❌ Wrong prompt count (8 or 10 prompts instead of 9)
- ❌ Keyword stuffing ("detective, noir, rain, night, trench coat, fedora, 8k, detailed")
- ❌ Character inconsistency (Prompt 2 has "short black hair" but Prompt 7 has "long blonde hair")
- ❌ Missing shot specs (no shot type or camera angle mentioned)
- ❌ Vague descriptions ("a person in a place")
- ❌ Style keywords missing or inconsistent across prompts

---

## Stage 3: Sequence Board (4-Panel) Review

**Artifact**: `sequence-board-prompt-ep{XX}.md`

### Structure and Count

- [ ] **Each sequence has exactly 4 panels** (not 3, not 5)
- [ ] **Source beat identified**: Each sequence references its source from the beat board
- [ ] **Narrative context provided**: What happens across the 4 panels explained
- [ ] **Duration estimated**: Real-time duration noted (e.g., "8 seconds")

### Inheritance (Critical)

- [ ] **Character appearance inherited**: Panels use same character description as source beat
  - Cross-check: Does Panel 1 character description match Beat X description?
  - Example: If Beat 5 says "woman with curly red hair in blue jacket", all 4 panels must maintain this
- [ ] **Setting inherited**: Location matches or logically extends from source beat
- [ ] **Lighting inherited**: Lighting approach consistent with source beat (unless story motivates change)

### Motion Continuity

- [ ] **Logical progression**: Action flows naturally from Panel 1 → 2 → 3 → 4
- [ ] **Physically plausible**: Actions can occur in the estimated duration
  - ❌ Fail: "Character runs 100 meters" in 3 seconds
  - ✓ Pass: "Character takes 3 steps forward" in 3 seconds
- [ ] **No teleportation**: Characters/objects move through space, don't jump positions
- [ ] **Clear transitions**: Panel-to-panel transitions specified (cut, pan, dolly, etc.)

### Cinematography (180-Degree Rule)

- [ ] **Screen direction maintained**: Characters don't flip sides without reason
  - Example: If Character A is on left in Panel 1, they should remain on left in Panels 2-4 unless they physically move
- [ ] **Axis stability**: Imaginary line between subjects maintained
- [ ] **Justified crossings**: If the 180-degree line is crossed, it's shown (not a jump)

### Cut Safety (Avoiding Jump Cuts)

- [ ] **No jump cuts**: Same shot from slightly different angle avoided
  - ❌ Fail: Panel 1: "Medium shot of character", Panel 2: "Medium shot of character, camera slightly closer"
  - ✓ Pass: Panel 1: "Medium shot", Panel 2: "Close-up of character's face" (clear change)
- [ ] **Distinct shot changes**: When cutting, shot type or angle changes significantly
- [ ] **Smooth transitions**: Cuts are motivated and clear, not jarring

### Panel Prompt Quality

- [ ] **Each panel 80-150 words**: Appropriate length maintained
- [ ] **Narrative descriptive style**: Not keyword lists
- [ ] **Shot specs included**: Shot type, camera angle, transition type

### Sequence Pacing

- [ ] **Action fits duration**: Motion described can realistically complete in time
- [ ] **Pacing variety**: Not all sequences are the same speed (some slow, some fast)
- [ ] **Camera movement clear**: If camera moves, direction and type specified

### Common Failure Patterns

- ❌ Wrong panel count per sequence (3 or 5 panels instead of 4)
- ❌ Character appearance differs from source beat (inheritance violation)
- ❌ Screen direction violation (character switches from left to right without movement)
- ❌ Jump cuts (Panel 1 medium shot, Panel 2 slightly different medium shot)
- ❌ Impossible actions (character flies across room in 1 second without superpowers)
- ❌ Unclear transitions (no indication of how Panel 1 connects to Panel 2)
- ❌ Setting changes unexpectedly (Panel 1 in office, Panel 3 suddenly in forest with no explanation)

---

## Stage 4: Motion Prompt Review

**Artifact**: `motion-prompt-ep{XX}.md`

### Structure and Count

- [ ] **One prompt per sequence**: Each 4-panel sequence gets one motion prompt
- [ ] **Source sequence identified**: References which sequence it's based on
- [ ] **Duration specified**: Target video duration noted (typically 3-5 seconds)

### Conciseness (Critical for Video Models)

- [ ] **Appropriate length**: 40-80 words (significantly shorter than static prompts)
  - Too long (>100 words) → model may ignore parts
  - Too short (<30 words) → lacks necessary detail
- [ ] **Focused description**: Describes motion, not exhaustive scene detail
  - ❌ Fail: "In a beautifully lit Victorian room with ornate furniture, tall windows, red velvet curtains..."
  - ✓ Pass: "In a Victorian room,..."

### Motion Clarity

- [ ] **Primary motion defined**: ONE clear main action described
  - ❌ Fail: "Character runs, jumps, spins, and waves while camera zooms and pans"
  - ✓ Pass: "Character runs forward while camera pans left to follow"
- [ ] **Direction specified**: Motion direction is unambiguous
  - Required: "left to right", "toward camera", "clockwise", etc.
  - ❌ Fail: "Character moves"
  - ✓ Pass: "Character moves from left to right"
- [ ] **Speed indicated**: Tempo of motion clear
  - Use: "slowly", "quickly", "drifts", "rushes", etc.

### Subject vs Camera Motion

- [ ] **Motion source clear**: Specify what moves (subject, camera, or both)
  - "Character walks forward" (subject moves)
  - "Camera dollies backward" (camera moves)
  - "Character runs left while camera pans right" (both move)
- [ ] **Camera movement specified**: If camera moves, type is clear
  - Pan, tilt, dolly, truck, zoom, orbit

### Physical Plausibility

- [ ] **Realistic for duration**: Motion can complete in stated time
  - 3 seconds: Simple action (head turn, pick up object, take a step)
  - 5 seconds: Moderate action (cross a small room, sit down, open door)
  - ❌ Fail: "Character sprints marathon" in 3 seconds
- [ ] **Physics obeyed**: No impossible movements (unless supernatural/justified)

### Subject Consistency

- [ ] **Character description matches source**: Subject described as in sequence board
  - Don't need full exhaustive description, but key identifiers maintained
  - Example: If sequence has "woman with silver hair in red coat", motion prompt should include these identifiers

### Focus and Simplicity

- [ ] **Single primary action**: Not multiple competing motions
- [ ] **Essential details only**: Background simplified compared to static prompts
- [ ] **Motion-centric**: Emphasis on the movement, not static composition

### Common Failure Patterns

- ❌ Too verbose (120+ words, reads like static image prompt)
- ❌ Multiple competing motions ("runs, jumps, spins, waves, and turns")
- ❌ Vague direction ("character moves around")
- ❌ Impossible timing ("character sprints across city" in 3 seconds)
- ❌ Character description doesn't match sequence board
- ❌ No motion direction specified
- ❌ Unclear what moves (subject? camera? both?)

---

## Review Output Format

When conducting a review, the Director should structure feedback as:

```markdown
## Review: [Artifact Name]

**Stage**: [1, 2, 3, or 4]
**Verdict**: PASS | FAIL

### Quality Check Results:

- [ ] Criterion 1: PASS/FAIL - [brief note]
- [ ] Criterion 2: PASS/FAIL - [brief note]
- [ ] Criterion 3: PASS/FAIL - [brief note]
      [...continue for all relevant criteria...]

### Issues Found:

[If FAIL, list specific problems with references to beats/prompts/panels]

1. **Issue**: [Description]

   - **Location**: [Beat 5, Prompt 3, Panel 2, etc.]
   - **Problem**: [Specific explanation]
   - **Required Fix**: [What needs to change]

2. **Issue**: [...]

### Recommended Actions:

[If FAIL, provide step-by-step revision guidance]

### Approval Notes:

[If PASS, optionally note exemplary aspects or minor suggestions]
```

---

## Decision Matrix

### When to PASS:

- ✓ All **major criteria** met
- ✓ Minor issues are cosmetic only (e.g., typo in a word that doesn't affect generation)
- ✓ Work is production-ready for AI generation
- ✓ Methodology principles (Clear, Concise, Consistent, Progressive) demonstrated

### When to FAIL:

- ✗ Any **major criterion** violated
- ✗ Consistency issues (character appearance changes, screen direction violations)
- ✗ Missing required elements (no shot specs, no lighting description)
- ✗ Methodology violations (keyword format instead of narrative, wrong lengths)
- ✗ Safety issues (continuity errors, jump cuts in sequences)
- ✗ Inheritance failures (4-panel doesn't match source 9-panel)

**Important**: When in doubt, FAIL and request clarification. It's better to ensure quality now than to waste generation resources on flawed prompts.

---

## Revision Loop Limits

- **Normal flow**: FAIL → Revise → Review → PASS
- **After 3 consecutive FAILs** on the same artifact: Escalate to Producer for user intervention
  - May indicate: unclear requirements, technical misunderstanding, or need for user input

---

This checklist is the foundation of quality control for the entire storyboard production system.
