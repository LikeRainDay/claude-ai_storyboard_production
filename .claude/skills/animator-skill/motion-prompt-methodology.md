# 📖 动态提示词方法论（仅供参考）

> **注意**: 这是参考指南。仅在复杂运动场景或有疑问时查阅。
> 不要自动加载此文件 - 仅在需要时参考。

# Motion Prompt Methodology

AI 视频生成模型的动态 motion prompts 创建专业指南。

**说明**: 本方法论内容保持英文，因为包含专业运动术语和示例，保持英文便于理解标准视频制作术语。

## Core Philosophy

**Video generation is fundamentally different from static image generation**:

- Static image prompts emphasize **composition** and **detail**
- Motion prompts emphasize **action** and **temporal dynamics**

A good motion prompt is:

- **Simpler** than a static prompt (less exhaustive detail)
- **Motion-focused** (what moves and how)
- **Directionally clear** (where the motion goes)
- **Temporally realistic** (action fits the duration)

---

## The Five Pillars of Motion Prompts

### 1. Simplicity

**Principle**: AI video models perform better with focused instructions. Avoid over-description.

**Static Image Prompt** (100+ words):

```
Medium shot, eye-level. A young woman in her 20s with long wavy brown hair wearing
a flowing blue sundress walks across a sunlit meadow filled with wildflowers, butterflies
fluttering around her, tall grass swaying gently, mountains visible in the distant
background under a clear blue sky with wispy clouds, warm golden afternoon light
creating soft shadows, serene and peaceful atmosphere. Cinematic composition,
photorealistic style, high detail.
```

**Motion Prompt** (60 words):

```
A young woman in a flowing blue dress walks from left to right across a sunlit meadow,
tall grass swaying around her. Camera static, following her motion with a slow pan.
Golden afternoon light, serene atmosphere. Slow, graceful movement. 4 seconds.
```

**Notice the reduction**:

- Fewer descriptive details (no exhaustive flower/butterfly/mountain description)
- Focus on the motion (walks left to right, grass sways)
- Camera specified (static with slow pan)
- Duration noted (4 seconds)

### 2. One Primary Motion

**Principle**: Describe ONE clear action. Multiple competing motions confuse the model.

**❌ Too Many Motions**:

```
Character runs forward, jumps over a log, spins in mid-air, lands in a roll,
pulls out a weapon, and aims at a target while the camera zooms in and pans right.
```

_(Character has 6 actions, camera has 2 movements — too much)_

**✓ Focused**:

```
Character runs forward and jumps over a log, landing in a crouch. Camera dollies
backward to keep character in frame. Fast, athletic motion. 3 seconds.
```

_(Character has 1 primary action: run and jump. Camera has 1 movement: dolly. Clear.)_

**Guideline**:

- 1 primary motion for the subject
- 0-1 camera movements
- Simple environmental motion (e.g., "leaves blow in wind") is okay as secondary

### 3. Directionality

**Principle**: Always specify WHERE the motion goes. Direction eliminates ambiguity.

**Lateral Motion** (horizontal):

- left to right
- right to left
- side to side

**Depth Motion** (z-axis):

- toward camera / forward
- away from camera / backward
- approaching / receding

**Vertical Motion**:

- upward / rising / ascending
- downward / falling / descending

**Rotational Motion**:

- clockwise / counterclockwise
- spinning / turning
- rotating

**❌ Vague**:

```
"Character moves across the room"
```

_(Which direction? Toward camera? Left to right?)_

**✓ Clear**:

```
"Character walks from left to right across the room, moving toward the background"
```

_(Lateral: left to right. Depth: toward background. Unambiguous.)_

### 4. Speed and Pacing

**Principle**: Indicate the tempo of motion. Speed affects mood and physical plausibility.

**Slow Motion Vocabulary**:

- slowly, gently, gradually
- drifts, floats, glides
- leisurely, unhurried
- "slow pan", "gentle movement"

**Medium Pace Vocabulary**:

- walks, moves, shifts
- steady, even pacing
- "normal speed", "natural motion"

**Fast Motion Vocabulary**:

- quickly, rapidly, swiftly
- darts, rushes, dashes
- "fast pan", "quick zoom"
- energetic, dynamic

**Example**:

```
"Character slowly turns their head from left to right, gradual and deliberate. 3 seconds."
```

_(Slow, deliberate pacing indicated. 3 seconds is appropriate for a slow head turn.)_

### 5. Subject vs Camera Motion

**Principle**: Clearly distinguish what moves — the subject, the camera, or both.

**Subject Motion Only**:

```
"A cat walks from left to right across a windowsill. Camera static. Slow, deliberate motion. 4 seconds."
```

_(Cat moves. Camera doesn't. Clear.)_

**Camera Motion Only**:

```
"Close-up of a flower in a garden. Camera slowly pans right, revealing more flowers in the background. Subject static. Smooth pan. 5 seconds."
```

_(Flower doesn't move. Camera pans. Clear.)_

**Combined Motion**:

```
"An athlete runs toward the camera while the camera dollies backward at matching speed,
keeping the athlete in frame. Fast, energetic motion. 4 seconds."
```

_(Both athlete and camera move. Relationship specified.)_

**Camera Movement Vocabulary**:

- **Pan**: Camera rotates horizontally (left/right)
- **Tilt**: Camera rotates vertically (up/down)
- **Dolly**: Camera moves forward/backward on a track
- **Truck**: Camera moves left/right horizontally
- **Zoom**: Focal length changes (camera doesn't move, but framing changes)
- **Orbit**: Camera circles around the subject
- **Handheld**: Camera shakes/moves naturalistically (simulates handheld camera)

---

## Temporal Realism

**Critical**: The described motion must be physically possible in the stated duration.

### Duration Guidelines

**3-Second Clip** (Short, Focused):

- Simple action: head turn, pick up object, take a step, open door
- Subtle motion: facial expression change, slight camera push-in
- Example: "Character turns head from left to right, eyes widening. 3 seconds."

**4-5 Second Clip** (Moderate Action):

- Moderate action: walk across small room, sit down, stand up, reach for object
- Slow camera movement: gentle pan, slow dolly
- Example: "Character walks 3 steps forward and kneels down. 5 seconds."

**6-8 Second Clip** (Extended Action):

- Complex action: pick up object and examine it, open door and step through
- Continuous motion: walk from one side of room to other
- Example: "Character walks from background to foreground, picks up a book from a table, and opens it. 7 seconds."

### Physical Plausibility Check

**❌ Impossible**:

```
"Character sprints 100 meters, climbs a ladder, and opens a door. 3 seconds."
```

_(Even an Olympic sprinter can't run 100m in 3 seconds, let alone also climb and interact)_

**✓ Plausible**:

```
"Character sprints 5 meters forward toward camera. 3 seconds."
```

_(Average running speed ~5 m/s, so 15 meters in 3 seconds is plausible, 5 meters is conservative and achievable)_

**✓ Plausible**:

```
"Character slowly climbs 3 rungs of a ladder, pausing briefly at each step. 6 seconds."
```

_(~2 seconds per rung, realistic pacing)_

---

## Motion Prompt Structure

### Template

```
[Subject Description] [Primary Motion] [Direction] [+ Camera Movement] [+ Secondary Elements].
[Camera specification]. [Pacing descriptors]. [Duration].
```

### Component Breakdown

#### 1. Subject Description (Brief)

Unlike static image prompts, motion prompts use simplified subject descriptions:

- Inherit key identifiers from the sequence board (hair, clothing, distinguishing features)
- Don't need exhaustive detail — focus is on motion, not composition

**Sequence Board Subject**:

```
"A woman in her late 20s with waist-length straight platinum blonde hair, pale porcelain skin,
bright violet eyes, wearing a long black coat over a white high-neck shirt and black pants"
```

**Motion Prompt Subject** (Simplified):

```
"A woman with platinum blonde hair in a long black coat"
```

_(Key identifiers maintained, but condensed for focus)_

#### 2. Primary Motion

The main action. Use active, specific verbs:

- walks, runs, jumps, turns, reaches, kneels, stands, sits, opens, closes, picks up, sets down
- floats, drifts, falls, rises, spins, rotates
- leans, tilts, sways, bends

#### 3. Direction

Where the motion goes (see Pillar 3: Directionality):

- Lateral: left to right, right to left
- Depth: toward camera, away from camera
- Vertical: upward, downward
- Rotational: clockwise, counterclockwise

#### 4. Camera Movement (Optional)

If the camera moves:

- Specify type (pan, tilt, dolly, truck, zoom, orbit)
- Specify direction (left, right, up, down, in, out)
- Specify speed (slow, fast, smooth, gradual)

**Examples**:

```
"Camera slowly pans right"
"Camera dollies forward while tilting up"
"Camera orbits clockwise around the subject"
"Camera static" (explicitly noting no camera movement)
```

#### 5. Secondary Elements (Optional)

Minor environmental motion that supports the scene:

```
"Leaves blow gently in the wind"
"Curtains sway in the breeze"
"Rain falls in the background"
```

Keep secondary elements minimal and non-competing with the primary motion.

#### 6. Pacing Descriptors

Speed and style of motion:

```
"Slow, deliberate motion"
"Fast, energetic movement"
"Smooth, graceful pacing"
"Sudden, abrupt motion"
```

#### 7. Duration

Target video length:

```
"3 seconds"
"5 seconds"
"4-5 seconds"
```

---

## Complete Example Prompts

### Example 1: Character Motion, Static Camera

```
A young warrior with braided red hair in leather armor draws a sword from a sheath at her side,
blade glinting as it emerges. Camera static. Slow, deliberate motion emphasizing the sword reveal.
4 seconds.
```

**Analysis**:

- Subject: Young warrior (key identifiers: braided red hair, leather armor)
- Motion: Draws sword from sheath
- Direction: Implied (from side/hip upward to reveal)
- Camera: Static (no movement)
- Pacing: Slow, deliberate
- Duration: 4 seconds

### Example 2: Camera Motion, Static Subject

```
Close-up of an ancient book lying open on a wooden table, candlelight illuminating the pages.
Camera slowly pushes in (dolly forward) toward the book, revealing intricate handwritten text.
Subject static. Smooth, slow dolly. 5 seconds.
```

**Analysis**:

- Subject: Ancient book (static, doesn't move)
- Motion: Camera moves (dolly forward)
- Direction: Forward/inward (toward the book)
- Camera: Dolly forward, slow and smooth
- Pacing: Slow
- Duration: 5 seconds

### Example 3: Combined Subject and Camera Motion

```
A detective in a trench coat walks from left to right through a rain-soaked alley, neon signs
reflecting in puddles. Camera trucks right at matching speed, keeping the detective centered in
frame. Steady walking pace, atmospheric rain. 5 seconds.
```

**Analysis**:

- Subject: Detective (trench coat for identification)
- Motion: Walks left to right
- Direction: Lateral (left to right)
- Camera: Trucks right (matches subject motion to keep centered)
- Pacing: Steady walking pace
- Duration: 5 seconds

### Example 4: Subtle Motion (Close-Up)

```
Extreme close-up of a woman's face, her eyes shifting from looking straight ahead to glancing
left, expression changing from neutral to concerned. Camera static. Subtle, slow motion. 3 seconds.
```

**Analysis**:

- Subject: Woman's face (eyes emphasized)
- Motion: Eyes shift direction, expression changes
- Direction: Straight ahead → left
- Camera: Static
- Pacing: Subtle, slow
- Duration: 3 seconds (appropriate for subtle eye/expression change)

### Example 5: Environmental Motion

```
Wide shot of a wheat field under a cloudy sky, tall wheat stalks swaying in waves from left to right
as wind blows across the field. Camera static. Gentle, rhythmic motion. 6 seconds.
```

**Analysis**:

- Subject: Wheat field
- Motion: Swaying (wind-driven)
- Direction: Left to right (wind direction)
- Camera: Static
- Pacing: Gentle, rhythmic
- Duration: 6 seconds (allows multiple sway cycles)

---

## Video Model Optimization

### Target Models

Motion prompts created with this methodology are optimized for:

- **Runway Gen-3**: High-quality cinematic video
- **Pika 1.5**: Creative effects and motion control
- **Stable Video Diffusion**: Open-source image-to-video
- **AnimateDiff**: Animation from static images
- **Luma Dream Machine**: Realistic video generation

### General Best Practices for AI Video Models

1. **Shorter is better**: 40-80 words (vs 80-150 for static)
2. **Motion clarity**: Models struggle with ambiguous motion, excel with clear direction
3. **Avoid complexity**: Simple motions generate more consistent results
4. **Physics matter**: Unrealistic motion produces artifacts
5. **Camera stability**: Static or smooth camera movements work better than complex handheld

### Model-Specific Notes

**Runway Gen-3**:

- Excellent with camera motion (dolly, pan, orbit)
- Handles 5-10 second clips well
- Strong with realistic human motion

**Pika 1.5**:

- Creative effects (inflate, explode, melt, etc.)
- Shorter clips (3-5 seconds) yield best results
- Good with exaggerated stylized motion

**Stable Video Diffusion**:

- Primarily image-to-video (uses first frame as reference)
- Simple motions work best
- Limited duration (typically 2-4 seconds)

**AnimateDiff**:

- Converts static keyframes to animation
- Works well with character animation
- Simpler motions, moderate duration (3-5 seconds)

---

## Common Pitfalls and Solutions

### Pitfall 1: Too Verbose

**❌ Problem** (120 words):

```
In a dark, moody forest with towering ancient oak trees, their gnarled branches reaching
toward an overcast sky, moss covering the trunks, ferns and fallen leaves scattered across
the forest floor, a lone figure in a hooded cloak walks slowly from the left side of the
frame toward the right, their footsteps quiet on the soft earth, mist swirling around their
ankles, birds occasionally visible in the canopy above, shafts of dim light filtering through
the leaves creating a mysterious and atmospheric scene. Cinematic lighting, fantasy aesthetic,
detailed environment.
```

**✓ Solution** (52 words):

```
A hooded figure walks slowly from left to right through a dark misty forest, moss-covered
trees in the background. Camera static. Mist swirls around the figure's feet as they move.
Slow, deliberate motion. Atmospheric lighting. 5 seconds.
```

### Pitfall 2: Multiple Competing Motions

**❌ Problem**:

```
Character runs forward, jumps, spins in mid-air, draws a sword, slashes at an enemy,
lands and rolls, while the camera zooms in, pans left, and tilts up.
```

**✓ Solution**:

```
Character runs forward, jumps, and lands in a combat stance. Camera dollies backward
to keep character in frame. Fast, dynamic motion. 4 seconds.
```

### Pitfall 3: Vague Motion Direction

**❌ Problem**:

```
"Character moves around the room"
```

**✓ Solution**:

```
"Character walks from the background toward the camera, approaching a table in the foreground"
```

### Pitfall 4: Physically Impossible Timing

**❌ Problem**:

```
"Character sprints across a football field, climbs a fence, and opens a door. 3 seconds."
```

**✓ Solution**:

```
"Character sprints 10 meters forward toward a fence. 3 seconds."
```

---

## Inheritance from Sequence Board

Motion prompts must maintain subject consistency from their source 4-panel sequence.

### Example Inheritance

**Sequence Board, Panel 1**:

```
Medium shot, eye-level. A woman in her late 20s with straight silver hair and a long
crimson coat stands at a train platform, wind blowing her hair back, her expression tense.
Dark cloudy sky in the background, platform lights casting cool blue tones. Cinematic
lighting, anime style.
```

**Motion Prompt** (Derived from Sequence):

```
A woman with silver hair in a crimson coat walks from left to right along a train platform,
wind blowing her hair and coat. Camera pans right to follow her motion. Steady walking pace,
tense atmosphere. 5 seconds.
```

**Notice**:

- **Inherited**: Silver hair, crimson coat, train platform, wind, tense mood
- **Simplified**: Don't need "late 20s", "straight hair", "dark cloudy sky", "cool blue tones" — focus is motion
- **Added**: Motion direction (left to right), camera movement (pan), duration (5 seconds)

---

## Quality Self-Check

Before submitting a motion prompt, verify:

- [ ] Length is 40-80 words (concise, motion-focused)
- [ ] ONE primary motion described (not multiple competing actions)
- [ ] Motion direction is clear (left to right, toward camera, etc.)
- [ ] Speed/pacing indicated (slow, fast, deliberate, etc.)
- [ ] Subject vs camera motion distinguished
- [ ] If camera moves, type and direction specified
- [ ] Motion is physically plausible for the duration
- [ ] Subject description matches source sequence board
- [ ] Duration specified (3-8 seconds typical)
- [ ] No excessive detail (simplified compared to static prompts)

---

## Advanced Animation Principles

### The 12 Principles of Animation (Adapted for AI Video)

**Note**: These principles from traditional animation can guide better motion prompts for AI video generation.

#### 1. Squash and Stretch (挤压与拉伸)

**Principle**: Objects deform to show impact, weight, or flexibility.

**In Motion Prompts**:

```
Ball bounces, compressing on impact with ground, then stretching as it rebounds
upward. Emphasize elastic deformation.
```

**When to use**:

- Bouncing objects
- Characters jumping or landing
- Flexible/organic materials

#### 2. Anticipation (预备动作)

**Principle**: Small preparatory movement before main action makes motion feel natural.

**In Motion Prompts**:

```
Character crouches down slightly, then jumps upward. Clear windup before the leap.
```

**Examples**:

- Wind-up before throwing
- Crouch before jump
- Lean back before punch

#### 3. Staging (演出布局)

**Principle**: Present action clearly so viewer knows where to look.

**In Motion Prompts**:

```
Character enters from left, walks to center of frame where spotlight focuses attention.
Background elements static. Clear focal point.
```

**Key**: One clear action, unambiguous staging.

#### 4. Follow Through & Overlapping Action (跟随与重叠动作)

**Principle**: Different parts move at different rates; motion doesn't stop instantly.

**In Motion Prompts**:

```
Character stops walking abruptly. Hair and coat continue swaying for a moment after.
Overlapping motion, cloth settles last.
```

**Examples**:

- Hair continues after head stops
- Loose clothing trails movement
- Pendulum swings after stopping

#### 5. Ease In / Ease Out (缓入缓出)

**Principle**: Motion starts slowly (ease in), accelerates, then slows (ease out). Natural acceleration curves.

**In Motion Prompts**:

```
Car starts slowly, gradually accelerates, then decelerates smoothly before stopping.
Ease-in-out motion curve. 5 seconds.
```

**Visual cue**: "Gradual acceleration and deceleration" or "smooth ease-in ease-out"

#### 6. Arcs (弧形运动)

**Principle**: Most natural motion follows curved paths, not straight lines.

**In Motion Prompts**:

```
Character's hand swings in smooth arc from hip to overhead. Arc motion path, not linear.
```

**Examples**:

- Arm/leg swings (pendulum arcs)
- Head turns (circular path)
- Thrown objects (parabolic arc)

#### 7. Secondary Action (次要动作)

**Principle**: Supporting action emphasizes main action without distracting.

**In Motion Prompts**:

```
Character walks forward (primary). Simultaneously, hand adjusts hat (secondary).
Both actions visible but walking is primary focus.
```

**Balance**: Secondary shouldn't overpower primary.

#### 8. Weight (重量感)

**Principle**: Motion should convey object's mass and density.

**In Motion Prompts**:

```
Heavy crate slides slowly across floor, friction evident. Slow, labored movement
conveying substantial weight. 6 seconds.
```

vs.

```
Feather drifts gently through air, floating and swaying. Light, weightless motion.
```

**Key terms**: Heavy, labored, slow / Light, quick, effortless

### Additional Useful Principles

#### 9. Timing (时机掌握)

**Principle**: Number of frames determines speed and weight perception.

**In Motion Prompts**: Specify precise duration and pace.

```
3 seconds: Quick, energetic action
5 seconds: Moderate, deliberate action
8 seconds: Slow, contemplative action
```

#### 10. Exaggeration (夸张)

**Principle**: Push beyond reality for emphasis (use sparingly for AI video).

**In Motion Prompts**:

```
Character's jaw drops comically low in shock, exaggerated surprise reaction.
```

**Caution**: Can look uncanny in realistic styles. Better for stylized content.

---

## Easing and Motion Curves

### Understanding Easing Functions

**Definition**: How motion accelerates/decelerates over time. Critical for natural movement.

#### Linear (线性)

**Characteristic**: Constant speed throughout.

**Feel**: Robotic, mechanical, unnatural.

**Use**: Mechanical objects, conveyor belts, artificial motion.

**Prompt indicator**:

```
"Constant speed, linear motion"
```

#### Ease-In (渐快/加速)

**Characteristic**: Starts slow, accelerates to full speed.

**Feel**: Building momentum, launching.

**Use**: Objects starting to move, beginning of motion.

**Prompt indicator**:

```
"Starts slowly, gradually accelerates, building speed"
```

**Example**:

```
Train starts slowly, gradually accelerating as it leaves station. Ease-in curve.
```

#### Ease-Out (渐慢/减速)

**Characteristic**: Full speed, decelerates to stop.

**Feel**: Coming to rest, settling.

**Use**: Objects stopping, end of motion.

**Prompt indicator**:

```
"Moving quickly, gradually decelerates, comes to gentle stop"
```

**Example**:

```
Door swings open quickly then slows smoothly before stopping. Ease-out curve.
```

#### Ease-In-Out (慢-快-慢)

**Characteristic**: Slow start, accelerate, full speed, decelerate, slow stop.

**Feel**: Natural, organic, human-like.

**Use**: Most natural motions (walking, arm movements, camera pans).

**Prompt indicator**:

```
"Smooth acceleration and deceleration, ease-in-out curve"
```

**Example**:

```
Camera pans left to right, starting slowly, accelerating through middle, slowing
smoothly at end. Natural ease-in-out.
```

#### Bounce (弹跳)

**Characteristic**: Overshoots target, bounces back, settles.

**Feel**: Elastic, playful, energetic.

**Use**: Bouncing balls, elastic materials, playful UI-like motion.

**Prompt indicator**:

```
"Bounces slightly past target, rebounds, settles with diminishing bounces"
```

#### Elastic (弹性)

**Characteristic**: Extreme overshoot and oscillation before settling.

**Feel**: Spring-like, exaggerated bounce.

**Use**: Very elastic materials, stylized cartoon motion.

**Prompt indicator**:

```
"Springs back and forth like elastic band before settling"
```

**Caution**: Can look unnatural in realistic styles.

### Spacing (间距/节奏控制)

**Definition**: Distance between positions in successive frames. Closer spacing = slower, wider spacing = faster.

**In AI video prompts**, describe spacing variation:

**Even spacing** (constant speed):

```
"Moves at steady, constant pace"
```

**Accelerating** (increasing spacing):

```
"Starts slow, each moment covering more distance, accelerating"
```

**Decelerating** (decreasing spacing):

```
"Moves fast initially, covering less distance each moment, slowing down"
```

---

## Advanced Camera Work

### Handheld vs Stabilized

#### Handheld Camera

**Characteristics**: Natural shake, imperfect framing, human feel.

**When to use**:

- Documentary style
- Urgent/chaotic scenes
- Intimate, personal moments
- Gritty realism

**In Motion Prompts**:

```
Handheld camera with subtle natural shake follows character through crowded street.
Slightly imperfect framing, documentary feel.
```

**Intensity levels**:

- **Minimal shake**: "Subtle handheld movement"
- **Moderate shake**: "Noticeable handheld camera shake"
- **Intense shake**: "Strong handheld shake, chaotic feel"

#### Stabilized Camera

**Characteristics**: Smooth, professional, no shake.

**When to use**:

- Cinematic scenes
- Calm moments
- Establishing shots
- Professional quality

**In Motion Prompts**:

```
Smooth dolly shot, camera glides forward on perfectly stable track. Professional,
cinematic stability.
```

### Dynamic Camera Techniques

#### Whip Pan (快速摇镜)

**Definition**: Extremely fast horizontal pan creating motion blur transition.

**Effect**: Energetic, dynamic, jarring.

**In Motion Prompts**:

```
Camera whip pans rapidly from left to right, creating motion blur, sudden dynamic
movement. 1 second.
```

**Use**: Transitions, following fast action, shock moments.

#### Crash Zoom (冲击变焦)

**Definition**: Rapid zoom in or out.

**Effect**: Dramatic emphasis, sudden revelation, comedic.

**In Motion Prompts**:

```
Camera rapidly zooms in on character's shocked face, crash zoom effect for dramatic
emphasis. 0.5 seconds.
```

**Variants**:

- **Zoom in**: Emphasis, revelation
- **Zoom out**: Context reveal, surprise

#### Focus Pull / Rack Focus (焦点转移)

**Definition**: Shift focus from foreground to background (or vice versa) mid-shot.

**Effect**: Directs viewer attention, cinematic depth.

**In Motion Prompts**:

```
Camera static. Focus starts on coffee cup in foreground (sharp), background blurred.
Focus shifts smoothly to character in background (now sharp), cup blurs out. Rack focus transition.
```

**Note**: AI video models vary in depth-of-field capability. This may work better in some models.

#### Push-In (推进镜头)

**Definition**: Camera moves steadily forward toward subject.

**Effect**: Intensifying, drawing viewer in, building tension.

**In Motion Prompts**:

```
Camera slowly pushes forward toward character's face, steady forward dolly, building
intensity. 4 seconds.
```

**Variants**:

- **Slow push-in**: Contemplative, building
- **Fast push-in**: Urgent, intense

#### Pull-Out (拉出镜头)

**Definition**: Camera moves steadily backward from subject.

**Effect**: Revealing context, isolation, distance.

**In Motion Prompts**:

```
Camera pulls back from character, gradually revealing the vast empty warehouse around
them. Slow dolly out, establishing isolation. 5 seconds.
```

### Tracking Shots

#### Following Shot

**Definition**: Camera follows moving subject at constant distance.

**In Motion Prompts**:

```
Camera tracks alongside character as they walk left to right, maintaining distance.
Smooth tracking shot. 5 seconds.
```

#### Leading Shot

**Definition**: Camera moves ahead of subject.

**In Motion Prompts**:

```
Camera dollies backward, facing character who walks forward toward camera. Character
follows camera, leading shot.
```

---

## Special Effects Motion

### Motion Blur

**Definition**: Blur created by rapid movement. Enhances sense of speed.

####描述 Motion Blur 强度

**Subtle blur**:

```
"Light motion blur on moving elements"
```

**Moderate blur**:

```
"Noticeable motion blur, emphasizing speed"
```

**Extreme blur**:

```
"Extreme motion blur, high-speed movement, streaking effect"
```

**Example**:

```
Car speeds past camera left to right, extreme motion blur creating streaking effect,
emphasizing velocity. 2 seconds.
```

### Impact Frames (冲击帧)

**Definition**: Brief frame emphasizing impact moment, often with distortion or white flash.

**In Motion Prompts**:

```
Character's fist hits wall. Brief bright flash on impact, emphasizing collision force.
Impact frame effect.
```

**Use**: Punches, collisions, explosions.

### Smear Frames (拖影帧)

**Definition**: Exaggerated motion blur for very fast movements, stretching shape.

**In Motion Prompts**:

```
Character swings sword in wide arc, blade creates elongated smear trail during fast
motion. Stylized smear effect.
```

**Use**: Fast swings, rapid movements, stylized action.

**Note**: Works better in stylized/animated aesthetics than photorealism.

### Hold Frames (停顿帧)

**Definition**: Motion freezes for brief moment, then continues.

**In Motion Prompts**:

```
Character jumps, freezes mid-air for 1 second (freeze frame), then lands. Hold frame
for emphasis.
```

**Use**: Emphasis, dramatic pause, slow-motion effect.

### Particle Effects Motion

**Definition**: Small elements (dust, sparks, water droplets) enhance main motion.

**In Motion Prompts**:

```
Character runs through shallow water, droplets spray up and outward with each footstep.
Particle spray emphasizes motion.
```

**Examples**:

- Dust kicked up by movement
- Sparks flying from impact
- Leaves swirling in wind
- Snow disturbed by passage

---

## Camera Movement Expressiveness

### Emotional Camera Language

**Stable** = Calm, professional, objective

```
"Camera perfectly stable, objective viewpoint"
```

**Handheld** = Intimate, urgent, subjective

```
"Handheld camera following closely, personal feel"
```

**Rising** = Hope, revelation, empowerment

```
"Camera slowly rises upward, hopeful ascending movement"
```

**Falling** = Despair, defeat, collapse

```
"Camera descends downward, falling with character"
```

**Spinning** = Disorientation, chaos, loss of control

```
"Camera rotates around subject, disorienting spin"
```

**Circling** = Observation, isolation, showcasing

```
"Camera orbits around character, observing from all angles"
```

### Speed and Emotion Pairing

**Very slow** (6-8 sec) = Contemplative, melancholy, dread
**Slow** (4-5 sec) = Deliberate, careful, building
**Medium** (2-3 sec) = Natural, conversational, neutral
**Fast** (1-2 sec) = Energetic, dynamic, urgent
**Very fast** (<1 sec) = Shocking, chaotic, impact

---

This methodology is designed as reference material. Animator should internalize these principles and apply them selectively based on the specific motion being described.
onsistency with the storyboard production pipeline.
