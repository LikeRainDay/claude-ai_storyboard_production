# Storyboard Methodology Playbook

This playbook defines the professional methodology for creating film and animation storyboards optimized for AI image generation workflows.

## Core Philosophy: The Four Pillars

### 1. Clear

Every storyboard element must be unambiguous and immediately understandable.

**Shot Specifications**:

- Always include shot type: wide shot, medium shot, close-up, extreme close-up, over-the-shoulder, point-of-view
- Specify camera angle: eye-level, low angle, high angle, Dutch angle (tilted), bird's eye, worm's eye
- Define framing: headroom, look space, rule of thirds composition

**Subject Descriptions**:

- Use concrete, specific language
- ✓ "A woman in her 30s with shoulder-length curly black hair, wearing a leather jacket"
- ✗ "A person in dark clothes"

**Environment Descriptions**:

- Specify location type and key features
- ✓ "A narrow cobblestone alley between brick buildings, trash cans on the left, fire escape on the right"
- ✗ "An alley"

### 2. Concise

Storyboards should be detailed without being bloated.

**Optimal Prompt Length**:

- Static image prompts: 80-150 words
- Motion prompts: 40-80 words

**What to Include**:

- Visual essentials: subject, action, setting, lighting, style
- Shot specifications: type, angle, framing
- Mood indicators: atmosphere, emotion, tone

**What to Exclude**:

- Backstory or narrative exposition
- Redundant descriptions
- Non-visual information (unless it affects visuals)

**Example of Proper Conciseness**:

```
Tight close-up, low angle. A rugged detective with a scarred face and grey stubble
leans forward into dim lamplight, his intense eyes fixed on something off-camera.
Dark office background blurred. Film noir aesthetic, high contrast lighting, moody shadows.
(62 words)
```

### 3. Consistent

Maintain visual continuity across all prompts in a project.

**Character Consistency**:

- Establish a canonical description in the first prompt
- Reuse identical physical descriptors in all subsequent prompts
- Track character "identity tokens": clothing, hairstyle, distinguishing features
- Only change appearance when story requires (costume change, injury, etc.)

**Character Identity Example**:

```
Canonical form: "A young woman in her mid-20s with waist-length straight silver hair,
pale skin, bright amber eyes, wearing a long crimson coat over black clothing"

Use in every prompt: "The silver-haired woman in the crimson coat..."
```

**Setting Consistency**:

- Maintain architectural details (if a room has 3 windows, it always has 3 windows)
- Consistent props and furniture placement
- Stable environmental features (weather, time of day unless story changes it)

**Style Consistency**:

- Apply the same style keywords to every prompt
- Maintain lighting approach (e.g., if cinematic lighting is established, maintain it)
- Consistent color palette (warm, cool, saturated, desaturated)

### 4. Progressive Refinement

Each stage builds on the previous, adding detail without contradicting.

**Stage Hierarchy**:

1. **Beat Breakdown**: Establishes narrative structure (9 key moments)
2. **Beat Board (9-panel)**: Establishes visual baseline (what characters/settings look like)
3. **Sequence Board (4-panel)**: Expands specific beats into continuous action
4. **Motion Prompts**: Adds temporal dimension to sequences

**The Inheritance Principle**:

- 4-panel sequences **must inherit** from their source 9-panel beat
- Character appearance: identical
- Setting: same or logically connected
- Lighting: consistent unless story motivates change

**Example of Inheritance**:

_Beat 5 (9-panel):_

```
Medium shot, eye-level. Detective Carter, a woman in her 40s with short grey hair
and a tan trench coat, stands in a rain-soaked street at night, neon signs
reflected in puddles. Cinematic lighting, film noir aesthetic.
```

_Sequence from Beat 5, Panel 1 (4-panel):_

```
Wide shot, eye-level. Detective Carter in her tan trench coat walks toward camera
down the rain-soaked street, neon signs glowing in the background. Same cinematic
lighting, film noir aesthetic.
```

**Notice**: Panel 1 inherits "Detective Carter", "tan trench coat", "rain-soaked street", "neon signs", and "cinematic lighting, film noir aesthetic" from Beat 5.

---

## Beat Breakdown Methodology

### Purpose

Identify the 9 most critical narrative moments that, together, tell the complete story.

### Beat Selection Criteria

A good beat is:

1. **A Turning Point**: Something changes (character learns something, makes a decision, encounters obstacle)
2. **Visually Distinct**: Can be represented in a single compelling image
3. **Story-Essential**: Removing it would create a narrative gap
4. **Emotionally Significant**: Heightened emotion or tension

### Coverage Requirements

The 9 beats must span:

- **Beginning** (Beats 1-3): Setup, character introduction, inciting incident
- **Middle** (Beats 4-6): Rising action, obstacles, complications
- **End** (Beats 7-9): Climax, resolution, denouement

### Distribution Strategy

**Even Distribution** (preferred for episodic content):

- Beats roughly evenly spaced across the script timeline
- Example for 30-page script: Beats at pages 3, 7, 11, 15, 19, 23, 26, 28, 30

**Weighted Distribution** (for dramatic arcs):

- More beats in high-intensity sections
- Example: Beats 1-2 (setup), 3-4 (conflict), 5-7 (climax), 8-9 (resolution)

### Beat Description Format

Each beat must include:

- **Beat Number**: 1-9
- **Timestamp/Scene Reference**: Page number, scene number, or timecode
- **Description**: What happens (1-2 sentences, specific)
- **Narrative Purpose**: Why this beat matters (1 sentence)

**Example**:

```
**Beat 4**
- Scene: Page 15, Warehouse confrontation
- Description: Maya discovers the stolen artifact hidden in a crate, but hears footsteps approaching
- Purpose: First major obstacle - hero has the MacGuffin but is now in immediate danger
```

### Common Beat Selection Mistakes

❌ **Too vague**: "Something bad happens"
✓ **Specific**: "The spaceship's life support fails"

❌ **Trivial moments**: "Character eats breakfast"
✓ **Story-crucial**: "Character discovers poison in the breakfast"

❌ **Clustered**: All 9 beats in the climax sequence
✓ **Distributed**: Beats across setup, development, and resolution

---

## Shot Composition & Cinematography

### Shot Types

**Wide Shot (WS)**: Shows full environment, establishes location

- Use for: Establishing shots, showing spatial relationships
- Character size: Small to full body visible

**Medium Shot (MS)**: Shows character from waist up

- Use for: Dialogue, character interaction
- Most common shot type in storyboards

**Close-Up (CU)**: Shows face or object filling frame

- Use for: Emotional moments, important details
- Creates intimacy and focus

**Extreme Close-Up (ECU)**: Shows eyes, mouth, or tiny object detail

- Use for: Peak emotional moments, critical clues
- Maximum intensity and attention

**Over-the-Shoulder (OTS)**: Shows from behind one character toward another

- Use for: Conversations, establishing POV
- Creates involvement

### Camera Angles

**Eye-Level**: Camera at subject's eye height

- Neutral, natural perspective
- Use for: Most shots

**Low Angle**: Camera below subject, looking up

- Makes subject appear powerful, imposing, threatening
- Use for: Hero moments, antagonist reveals

**High Angle**: Camera above subject, looking down

- Makes subject appear vulnerable, weak, small
- Use for: Moments of defeat, danger, isolation

**Dutch Angle**: Camera tilted off horizontal axis

- Creates unease, disorientation, tension
- Use for: Psychological distress, supernatural elements, action

### The 180-Degree Rule (Screen Direction)

**Rule**: Imagine a line between two characters. Keep the camera on one side of this line throughout a scene.

**Why**: Maintains spatial consistency. If Character A is on the left and Character B is on the right in Shot 1, they should remain on those sides in Shot 2.

**Violations**: Cause "crossing the line" — characters suddenly switch sides, disorienting the audience.

**Example**:

```
✓ Correct:
Shot 1: Wide shot - Character A (left) talks to Character B (right)
Shot 2: Close-up of A - camera still on same side, A still on left
Shot 3: Close-up of B - camera still on same side, B still on right

✗ Violation:
Shot 1: Character A on left
Shot 2: Character A suddenly on right (camera jumped to other side of the line)
```

**Exceptions**: You can cross the line if you show the camera movement (pan across) or insert a neutral shot (facing straight on).

### Composition Rules

**Rule of Thirds**:

- Divide frame into 9 equal parts with 2 horizontal and 2 vertical lines
- Place key subjects and horizon lines on these lines or their intersections
- Creates balanced, pleasing composition

**Lead Room** (Look Space):

- Leave empty space in the direction a character is looking or moving
- ✓ Character on left, looking right → leave space on right
- ✗ Character on left, looking left → feels cramped

**Headroom**:

- Space between top of subject's head and top of frame
- Too much: subject feels small and lost
- Too little: feels cramped
- Just right: varies by shot type (less in close-ups, more in wide shots)

---

## Continuity Management

### Continuity Errors to Avoid

1. **Character Appearance Changes**:

   - Hair length, color, style
   - Clothing, accessories
   - Physical features (eye color, build, scars)

2. **Prop Discontinuity**:

   - Object disappears between shots
   - Object changes (coffee cup becomes water glass)
   - Object position jumps

3. **Environmental Continuity**:

   - Lighting changes without motivation
   - Weather changes mid-scene
   - Time of day inconsistency

4. **Screen Direction Violations**:
   - Character switches sides without motivation
   - Movement direction reverses

### Continuity Maintenance Strategies

**Character Anchor Description**:
Create a reference description and reuse it verbatim.

```
Reference: "Marcus, a tall man in his 50s with salt-and-pepper hair combed back,
wearing a navy blue suit and red tie"

Reuse in Prompt 1: "Marcus in his navy blue suit leans against the desk..."
Reuse in Prompt 5: "Marcus in his navy blue suit stands at the window..."
```

**Setting Anchor Points**:
Establish key features that must appear in all shots.

```
Reference: "A Victorian study with dark wood paneling, a red leather chair,
a globe by the window, and floor-to-ceiling bookshelves"

Ensure all shots in this location include these elements or logically explain their absence
(e.g., "facing the door, bookshelves visible behind" vs "facing the window, door behind").
```

**Lighting Continuity**:
Define the lighting approach and maintain it.

```
Lighting Scheme: "Warm practical lighting from desk lamp, cool moonlight through window,
creating split lighting on character's face"

Maintain this scheme in all shots in this scene, adjusting intensity but not direction or color.
```

---

## Special Techniques for AI Image Generation

### Narrative Descriptive Style

AI image models (especially Gemini Imagen 3) perform better with flowing narrative descriptions than keyword lists.

**Keyword Style (Less Effective)**:

```
detective, trench coat, rain, night, neon, film noir, dramatic lighting, close-up
```

**Narrative Style (More Effective)**:

```
Close-up of a detective in a trench coat, rain dripping from his hat brim,
neon signs reflected in his eyes. Film noir aesthetic with dramatic lighting.
```

### Optimal Prompt Structure

**Template**:

```
[Shot Type + Angle]. [Subject Description] [Action/Pose] [in/at/near] [Setting Description].
[Lighting Description]. [Style Keywords].
```

**Example**:

```
Medium shot, low angle. A young warrior with braided red hair and leather armor
raises a glowing sword overhead, standing atop a rocky cliff. Golden sunset light
from behind creates a silhouette effect. Fantasy illustration style, epic composition.
```

### Avoiding AI Generation Artifacts

**Common Issues and Solutions**:

1. **Extra limbs or distorted anatomy**:

   - Use specific pose descriptions: "arms at sides", "right hand on hip, left hand holding phone"
   - Avoid: "multiple arms", "many hands"

2. **Inconsistent character appearance**:

   - Reuse exact descriptor phrases
   - Include distinctive features: "scar over left eyebrow", "tattoo on right forearm"

3. **Text gibberish** (AI adds fake text):

   - If you need readable text, specify: "blank billboard", "sign with no text"
   - Or accept that text will be garbled (common AI limitation)

4. **Background blending**:
   - Clearly separate subject and background: "in the foreground", "background shows..."
   - Use depth cues: "blurred background", "shallow depth of field"

### Style Consistency Tokens

Use the same style keywords in every prompt:

**Example Style Set**:

```
"anime style, soft shading, vibrant colors, cinematic composition"
```

Apply to all prompts:

```
Prompt 1: [description]. Anime style, soft shading, vibrant colors, cinematic composition.
Prompt 2: [description]. Anime style, soft shading, vibrant colors, cinematic composition.
...
Prompt 9: [description]. Anime style, soft shading, vibrant colors, cinematic composition.
```

---

## Quality Self-Check

Before submitting work, verify:

### Beat Breakdown:

- [ ] Exactly 9 beats selected
- [ ] All beats have number, timestamp, description, purpose
- [ ] Beats span beginning, middle, end
- [ ] Each beat is a turning point or crucial moment
- [ ] Descriptions are specific, not vague

### Beat Board (9-panel):

- [ ] Exactly 9 prompts
- [ ] Each prompt 80-150 words
- [ ] Narrative descriptive style (not keyword lists)
- [ ] Character appearance identical across all prompts
- [ ] Setting details consistent
- [ ] Shot type and angle specified for each
- [ ] Style keywords applied uniformly

### Sequence Board (4-panel):

- [ ] Each sequence has exactly 4 panels
- [ ] Panels inherit character, setting, lighting from source 9-panel
- [ ] Motion is continuous and logical
- [ ] Screen direction maintained (180-degree rule)
- [ ] Transitions are smooth (no jump cuts)
- [ ] Physical actions are plausible

---

This methodology is the foundation of all storyboard work in this system. The Storyboard Artist must apply these principles, and the Director will enforce them during review.
