# 📖 影视分镜方法论手册（仅供参考）

> **注意**: 这是参考指南。仅在遇到方法论问题时查阅。
> 不要自动加载此文件 - 仅在困惑或需要时参考。

# Film Storyboard Methodology Playbook

专业的影视和动画分镜方法论，优化用于 AI 图像生成工作流。

**说明**: 本手册内容保持英文，因为包含大量专业术语和示例，保持英文便于理解标准摄影和分镜术语。

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

## Advanced Film Techniques

### Montage (蒙太奇)

**Definition**: A sequence of short shots edited together to condense time, convey ideas, or create emotional impact.

#### When to Use Montage

- **Compress time**: Show a lengthy process (training, journey, construction) in seconds
- **Thematic connection**: Link disparate elements to convey a concept or theme
- **Parallel action**: Show multiple events happening simultaneously
- **Build rhythm**: Create emotional momentum through editing pace

#### Montage Types

**Narrative Montage** (叙事蒙太奇):

Compress time by showing key moments of a process.

**Structure for 9-panel beat board**:

- Beat 4: Process begins
- Beat 5: [MONTAGE IMPLIED] - Single representative image from montage
  - Visual Description should note: "Montage sequence - multiple training moments"
- Beat 6: Process complete, character transformed

**Example**:

```
Beat 4: Training Begins
Visual Description: Wide shot. The protagonist in workout clothes stands in
an empty gym, looking at a punching bag with determination. Early morning
light through windows. Cinematic composition.

Beat 5: Training Montage
Visual Description: Medium shot. The protagonist mid-punch, sweat flying,
intense focus. This image represents a montage of training moments - running,
lifting, sparring. Gritty, high-contrast lighting showing effort and struggle.
[NOTE: In actual production, this becomes 5-10 quick shots]

Beat 6: Mastery Achieved
Visual Description: Medium shot from low angle. The protagonist, now muscular
and confident, wraps hands in tape before a championship fight. Professional
gym setting. Powerful, heroic lighting.
```

**Thematic Montage** (主题蒙太奇):

Juxtapose contrasting or related images to convey a theme.

**Example Theme: Inequality**

- Shot 1: Lavish banquet, rich guests in formal wear
- Shot 2: Homeless person digging through trash
- Shot 3: Luxury car driving past
- Shot 4: Child begging on street corner
- Alternating creates thematic contrast

**In beat board**: Choose one representative moment from each "side" of the theme.

**Parallel Montage** (平行蒙太奇):

Cross-cut between two or more simultaneous actions to build tension.

**Structure**:

- Beat 6: Character A discovers danger
- Beat 7: [PARALLEL] Character B unaware, walking into trap
- Beat 8: Both storylines converge

**Visual cue**: Note in prompt: "Parallel action - Character B simultaneously..."

#### Montage Pacing

**Fast cuts** (1-2 seconds each):

- High energy, urgency
- Action sequences
- Frenetic emotion

**Medium cuts** (2-4 seconds each):

- Progress over time
- Training sequences
- Building momentum

**Slow cuts** (4-6 seconds each):

- Melancholy, reflection
- Loss or grief
- Contemplative moments

### Transitions Between Scenes (场景转场)

**Definition**: How one scene connects to the next. Choice of transition affects pacing and meaning.

#### Cut (直切)

**Most common**: Direct cut from one shot to the next.

**When to use**:

- Continuous time/space
- Maintain forward momentum
- Standard narrative flow

**In sequence board**:

```
Panel 3: Character closes laptop, stands up
Panel 4: [CUT] Character walks down street
```

#### Match Cut (匹配剪辑)

**Definition**: Transition using visual or thematic similarity.

**Types**:

**Graphic Match** - Similar shapes:

```
Panel 3: Close-up of character's eye, wide with fear
Panel 4: [MATCH CUT] Full moon in night sky, same circular composition
```

**Action Match** - Continues motion:

```
Panel 3: Character's hand reaches for door handle
Panel 4: [MATCH CUT] Hand pulls open car door (different location, continuous motion)
```

**Conceptual Match** - Thematic link:

```
Panel 3: Child's toy spinning on floor
Panel 4: [MATCH CUT] Roulette wheel in casino (years later)
```

**How to note in prompts**: Add descriptor like "Match cut - circular composition continues"

#### Dissolve / Cross-fade (叠化)

**Definition**: One image gradually fades into another, briefly overlapping.

**When to use**:

- Time passage
- Dream sequences
- Memories/flashbacks
- Gentle, contemplative transitions

**Visual indicator in prompt**:
"Soft edges, slightly dreamy quality - dissolve transition to next beat"

**In sequence board**:

```
Panel 3: Character closes eyes in hospital bed, exhausted
Panel 4: [DISSOLVE] Character wakes in same position, but room now sunny
         (days later). Lighting shift indicates time passage.
```

#### Fade to Black (淡至黑)

**Definition**: Image fades to complete black screen.

**When to use**:

- Chapter/act breaks
- Dramatic endings
- Major time jumps
- Death or loss

**In beat board**: Note after beat - "Fade to black before next beat"

#### Smash Cut (冲击切)

**Definition**: Abrupt, jarring transition for shock effect.

**When to use**:

- Sudden revelations
- Startling interruptions
- Contrast quiet moment with loud/shocking scene

**Example**:

```
Panel 3: Character sleeps peacefully, serene quiet bedroom
Panel 4: [SMASH CUT] Explosion fills frame, chaos, fire
```

#### Wipe (划变)

**Definition**: One image "pushes" another off screen (less common, stylistic).

**When to use**:

- Stylized sequences (Star Wars style)
- Playful tone
- Retro/homage aesthetics

**Note**: Rarely needed for AI storyboarding, mentioned for completeness.

### Time and Space Manipulation (时空处理)

#### Flashback (闪回)

**Definition**: Interrupts present timeline to show past events.

**Visual Indicators**:

- Desaturated colors or sepia tone
- Soft vignette edges
- Slightly blurred or dreamy quality
- Different aspect ratio (optional)

**Structure in 9-panel beat board**:

```
Beat 4: Present - Character sees old photograph
Visual Description: ...triggers memory...

Beat 5: [FLASHBACK] Past - The moment in the photograph
Visual Description: Same scene but 20 years earlier. Desaturated colors,
soft vignette edges, nostalgic atmosphere. [Flashback sequence]
Lighting & Mood: Warm, faded colors like an old photograph. Dreamy,
nostalgic mood.

Beat 6: Return to Present - Character sets photo down
Visual Description: Back to full color saturation...
```

**Transition cues**:

- INTO flashback: Dissolve with desaturation
- OUT of flashback: Dissolve back to full color

#### Flash-forward (闪前)

**Definition**: Jump forward to show future events.

**Visual Indicators**:

- Oversaturated or stark lighting
- Sharp, cold color temperature
- High contrast
- Optional: Different visual style (grittier, more digital)

**Use sparingly**: Can confuse narrative if overused.

#### Dream Sequence (梦境序列)

**Visual Indicators**:

- Surreal elements (defying physics)
- Soft focus or ethereal glow
- Unstable framing (Dutch angles)
- Unexpected color shifts
- Logic violations (A transforms into B)

**Example**:

```
Beat 6: [DREAM] Character walks through impossible architecture
Visual Description: Wide shot, Dutch angle. Character walks up stairs that
transform into waterfalls mid-step. Walls shift and breathe. Soft glowing
edges around everything. Physics-defying, Escher-like architecture.
Lighting & Mood: Diffuse, directionless glow. Ethereal and unsettling.
Blue-purple otherworldly color palette. Dream logic.
```

**Transition in/out**: Usually fade to black or dissolve.

#### Slow Motion (慢动作)

**When to use**:

- Emotional peaks (tears falling, embrace)
- Emphasize critical action (bullet dodged, glass shattering)
- Beauty/grace (athlete's perfect form)
- Dramatic impact (explosion, fall)

**In motion prompts**:

```
Glass shatters in extreme slow motion, fragments suspended in air catching
light. 6 seconds.
```

**In static beat board**: Implies weight and importance.

```
Visual Description: ...water droplets frozen mid-splash, crystalline and
detailed. [Slow motion aesthetic]
```

#### Fast Motion / Time Lapse (快动作/延时)

**When to use**:

- Show long time passage quickly (sun crossing sky, city bustling)
- Comedic effect
- Convey frantic energy

**Example**:

```
Beat 3: Time Lapse - City Awakening
Visual Description: Wide shot of city skyline. Blurred motion of clouds
racing overhead, traffic streaks of light, sun arcing across sky.
[Time lapse effect]. Represents dawn to dusk in seconds.
```

#### Freeze Frame (定格)

**Definition**: Motion stops, becomes still image.

**When to use**:

- Emphasize moment of realization
- Ending on character's expression
- Pause for dramatic effect

**In motion prompt**: "Motion continues until character's expression shifts
to shock, then freeze frame. 4 seconds total, last 2 seconds frozen."

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
