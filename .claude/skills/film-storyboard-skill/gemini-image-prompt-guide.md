# Gemini Image Prompt Guide

Optimized prompt writing guide for AI image generation models, with focus on Gemini Imagen 3 and similar models (Midjourney, DALL-E, Stable Diffusion).

## Core Principle: Narrative Descriptive Style

Unlike search queries or tags, image generation prompts work best as flowing narrative descriptions.

### Comparison

**❌ Keyword Style** (Less Effective):

```
woman, red dress, beach, sunset, golden hour, romantic, soft lighting, 8k, detailed
```

**✅ Narrative Style** (More Effective):

```
A woman in a flowing red dress stands on a sandy beach at sunset, warm golden light
illuminating her profile, gentle waves in the background. Soft romantic lighting,
cinematic composition.
```

**Why Narrative Works Better**:

- Models understand relationships between elements
- Context improves coherence
- Reduces ambiguous interpretations
- More natural language = better semantic understanding

---

## Universal Prompt Structure

### Template

```
[Shot Specification] + [Subject Description] + [Action/Pose] + [Setting] + [Lighting] + [Style]
```

### Component Breakdown

#### 1. Shot Specification (Shot Type + Camera Angle)

**Shot Types**:

- **Wide shot** / **Establishing shot**: Shows full environment
- **Full shot**: Subject head to toe
- **Medium shot**: Subject from waist up
- **Close-up**: Head and shoulders / face
- **Extreme close-up**: Eyes, mouth, or detail
- **Over-the-shoulder**: From behind one subject toward another
- **Point of view (POV)**: Camera as character's eyes

**Camera Angles**:

- **Eye-level**: Neutral perspective
- **Low angle**: Camera looking up (subject appears powerful)
- **High angle**: Camera looking down (subject appears vulnerable)
- **Dutch angle**: Tilted camera (creates tension, unease)
- **Bird's eye**: Directly overhead
- **Worm's eye**: Directly below looking up

**Example**:

```
Medium shot, low angle.
```

#### 2. Subject Description

**Key Principles**:

- Be specific, not generic
- Include age range, gender (if relevant)
- Physical features (hair, eyes, build)
- Clothing and accessories
- Distinguishing marks (scars, tattoos, etc.)

**Generic → Specific Evolution**:

```
❌ "A person"
→ "A woman"
→ "A young woman in her 20s"
→ "A young woman in her 20s with short black hair"
→ "A young woman in her 20s with short black hair and round glasses, wearing a leather jacket"
```

**Character Consistency**:
When creating multiple prompts for the same character, use **identical physical descriptors**:

```
Reference: "A man in his 40s with a thick grey beard, shaved head, wearing a plaid shirt"

Prompt 1: "A man in his 40s with a thick grey beard, shaved head, wearing a plaid shirt..."
Prompt 5: "A man in his 40s with a thick grey beard, shaved head, wearing a plaid shirt..."
```

#### 3. Action/Pose

Describe what the subject is doing:

- **Static**: standing, sitting, leaning, kneeling
- **Dynamic**: running, jumping, reaching, falling
- **Interacting**: holding object, pushing door, touching face
- **Expressive**: laughing, crying, shouting, whispering

**Examples**:

```
"stands with arms crossed, gazing off into the distance"
"runs toward the camera, arms pumping"
"kneels on one knee, head bowed"
"reaches out with one hand toward a glowing object"
```

#### 4. Setting/Environment

**Structure**: [Location Type] + [Key Features] + [Spatial Relationships]

**Location Types**:

- Interiors: office, bedroom, warehouse, cathedral
- Exteriors: street, forest, beach, rooftop
- Abstract: void, gradient background, dreamscape

**Key Features**:
List 2-4 distinctive elements:

```
"A Victorian library with floor-to-ceiling bookshelves, a rolling ladder, and a
fireplace with ornate mantelpiece"
```

**Spatial Relationships**:
Where is the subject relative to setting features?

```
"standing in the center of a circular room, ancient runes carved into the stone floor around her"
```

**Depth Control**:

- "in the foreground" / "in the background"
- "blurred background" (for subject focus)
- "shallow depth of field"

#### 5. Lighting

**Lighting Direction**:

- Front lighting: from camera direction (flat, even)
- Back lighting: from behind subject (silhouette, rim light)
- Side lighting: from left or right (dramatic, sculptural)
- Top lighting: from above (mysterious, dramatic)
- Bottom lighting: from below (eerie, unsettling)

**Lighting Quality**:

- **Hard light**: Direct, strong shadows (sunlight, spotlight)
- **Soft light**: Diffused, gentle shadows (overcast, softbox)
- **Practical lights**: Sources visible in scene (lamps, candles, neon)

**Lighting Mood**:

- Golden hour: warm, soft, nostalgic
- Blue hour: cool, melancholic, mysterious
- High contrast: dramatic, film noir
- Low contrast: dreamy, ethereal
- Rim lighting: subject outlined by backlight

**Examples**:

```
"warm golden hour sunlight streaming through a window, creating long shadows"
"cool blue moonlight illuminating the scene, high contrast with deep shadows"
"soft diffused lighting from above, gentle and even"
"dramatic side lighting from a single desk lamp in an otherwise dark room"
```

#### 6. Style Keywords

**Visual Style**:

- photorealistic
- anime / manga
- oil painting / watercolor / digital art
- film noir / cyberpunk / fantasy
- sketch / line art / concept art

**Technical Quality** (use sparingly):

- cinematic composition
- detailed
- high resolution
- professional photography

**Mood/Atmosphere**:

- moody, ethereal, vibrant, muted, dramatic, serene, chaotic

**Example Style Combinations**:

```
"Anime style, soft cel shading, vibrant colors, cinematic composition"
"Photorealistic, professional photography, cinematic lighting, high detail"
"Digital concept art, painterly style, dramatic atmosphere, muted color palette"
```

---

## Complete Example Prompts

### Example 1: Character Introduction

```
Medium shot, eye-level. A detective in his 50s with greying hair slicked back and a
weathered face stands in a dimly lit office, arms crossed, looking directly at the camera
with a skeptical expression. Behind him, a wall of evidence photos and string connecting
clues, a single desk lamp providing warm amber light. Film noir aesthetic, high contrast
lighting, moody atmosphere.
```

### Example 2: Action Scene

```
Wide shot, low angle. A young archer with long braided blonde hair and green leather
armor draws her bow while running across a stone bridge, an arrow nocked and ready.
Medieval castle towers in the background, storm clouds gathering, dramatic twilight
lighting with purple and orange hues. Fantasy illustration style, dynamic composition,
epic atmosphere.
```

### Example 3: Emotional Moment

```
Close-up, slightly high angle. An elderly woman with silver hair in a bun and deep
wrinkles around her eyes closes her eyes, a single tear rolling down her cheek, sitting
in a wooden chair by a window. Soft natural light from the window illuminates the side
of her face, lace curtains visible, quiet and intimate atmosphere. Photorealistic style,
gentle lighting, melancholic mood.
```

### Example 4: Environmental Establishing Shot

```
Wide establishing shot, eye-level. A bustling cyberpunk street market at night, neon
signs in Japanese and English reflecting in rain-slicked pavement, crowds of people with
umbrellas moving between vendor stalls selling tech and street food. Vibrant pink and
cyan neon lighting, light rain creating atmospheric haze. Cyberpunk aesthetic, cinematic
composition, vibrant colors.
```

---

## Gemini-Specific Optimizations

### What Works Well in Gemini Imagen 3

1. **Natural Language**: Full sentences and descriptive phrases
2. **Concrete Details**: Specific clothing, hairstyles, objects
3. **Lighting Descriptions**: Detailed lighting dramatically improves quality
4. **Compositional Cues**: Shot types, angles, framing
5. **Style Specification**: Clear artistic direction

### What to Avoid

1. **Keyword Spam**: Don't list 30 comma-separated modifiers
2. **Conflicting Instructions**: "bright sunny day, dark moody lighting"
3. **Overly Complex Scenes**: Too many subjects or actions dilutes focus
4. **Unclear Subjects**: Make it obvious what the main subject is
5. **Negative Prompts** (Not Supported): Gemini doesn't use negative prompts like some models

### Prompt Length

**Optimal Range**: 80-150 words for static image prompts

**Too Short** (< 50 words):

- Lacks specificity
- Model fills in missing details unpredictably
- Higher variance in results

**Too Long** (> 200 words):

- Model may ignore later parts
- Conflicting details more likely
- Diminishing returns

**Sweet Spot** (80-150 words):

- Enough detail for consistency
- Clear enough for model to understand
- Focused on visual essentials

---

## Character Consistency Techniques

### The Reference Description Method

1. **Create a canonical description** for each character
2. **Store it** in the beat breakdown or as a project note
3. **Reuse identical phrases** in every prompt

**Example**:

**Canonical Description**:

```
"Lena, a woman in her late 20s with waist-length straight platinum blonde hair,
pale porcelain skin, bright violet eyes, wearing a long black coat over a white
high-neck shirt and black pants, silver ring on right hand"
```

**Usage in Prompts**:

```
Prompt 1: Medium shot, eye-level. Lena, a woman in her late 20s with waist-length
straight platinum blonde hair, pale porcelain skin, bright violet eyes, wearing a
long black coat over a white high-neck shirt and black pants, stands at a train
platform...

Prompt 5: Close-up, low angle. Lena's face fills the frame, her platinum blonde hair
blowing in the wind, violet eyes narrowed as she looks up at something off-camera.
She's wearing her long black coat, collar turned up...
```

**Notice**: Even when the shot changes (medium → close-up), the core descriptors (platinum blonde hair, violet eyes, black coat) are maintained.

### Object/Prop Consistency

Same principle applies to recurring objects:

**Canonical**:

```
"An ancient leather-bound journal with brass corner protectors and a red ribbon bookmark"
```

**Reuse**:

```
Prompt 3: ...holding the ancient leather-bound journal with brass corner protectors...
Prompt 7: ...the journal with brass corners lies open on the table...
```

---

## Lighting Guide

### Natural Lighting Scenarios

**Golden Hour** (sunrise/sunset):

```
"warm golden sunlight, long soft shadows, orange and amber tones"
```

**Blue Hour** (twilight):

```
"cool blue twilight, soft gradient from purple to dark blue, minimal shadows"
```

**Midday Sun**:

```
"bright harsh sunlight from directly above, strong shadows, high contrast"
```

**Overcast/Cloudy**:

```
"soft diffused light, even illumination, minimal shadows, muted colors"
```

**Moonlight**:

```
"cool silver moonlight, deep shadows, blue-tinted highlights, mysterious atmosphere"
```

### Artificial Lighting Scenarios

**Interior Room Light**:

```
"warm ambient light from ceiling fixture, soft shadows, cozy atmosphere"
```

**Desk Lamp** (Film Noir style):

```
"single warm desk lamp in otherwise dark room, dramatic side lighting, deep shadows"
```

**Neon Signs**:

```
"vibrant neon lighting in pink and cyan, colored reflections, high contrast"
```

**Candlelight**:

```
"warm flickering candlelight, soft orange glow, gentle shadows dancing on walls"
```

**Fireplace**:

```
"warm dancing firelight from the left, orange and amber tones, dynamic shadows"
```

### Advanced Lighting Techniques

**Rim Lighting**:

```
"strong backlight creating a bright outline around the subject's silhouette"
```

**Split Lighting**:

```
"light from the left illuminates half the face, right side in shadow, dramatic contrast"
```

**Silhouette**:

```
"bright backlight with subject in complete shadow, only outline visible"
```

**Volumetric Lighting** (God Rays):

```
"beams of sunlight streaming through windows, dust particles visible in light shafts"
```

---

## Common Pitfalls and Solutions

### Pitfall 1: Generic Descriptions

❌ **Problem**:

```
"A person in a room with furniture"
```

✅ **Solution**:

```
"A teenage girl with short curly brown hair and wearing a yellow hoodie sits cross-legged
on a plush grey sofa in a modern living room with white walls and a potted plant by the
window. Soft afternoon sunlight streaming through sheer curtains."
```

### Pitfall 2: Keyword Stuffing

❌ **Problem**:

```
detective, noir, rain, night, trench coat, fedora, mystery, dark, moody, shadows,
cinematic, 8k, detailed, atmospheric, dramatic
```

✅ **Solution**:

```
Close-up of a detective in a trench coat and fedora, rain dripping from the brim,
standing on a dark city street at night with neon reflections in puddles. Film noir
aesthetic, moody atmospheric lighting with dramatic shadows.
```

### Pitfall 3: Character Inconsistency

❌ **Problem**:

```
Prompt 1: "A woman with short red hair..."
Prompt 2: "A woman with long blonde hair..."
```

_(Same character, different description = different appearance in generated images)_

✅ **Solution**:

```
Prompt 1: "A woman with shoulder-length curly red hair and green eyes, wearing a denim jacket..."
Prompt 2: "A woman with shoulder-length curly red hair and green eyes, wearing a denim jacket..."
```

_(Identical descriptors = consistent appearance)_

### Pitfall 4: Conflicting Elements

❌ **Problem**:

```
"Bright sunny day with storm clouds and rain, warm golden light and cool shadows"
```

✅ **Solution**:

```
"Dramatic moment just after a storm, sun breaking through dissipating dark clouds,
creating patches of warm golden light among lingering cool shadows"
```

_(Explains the transition, resolves conflict)_

### Pitfall 5: Overly Complex Composition

❌ **Problem**:

```
"A crowded marketplace with 20 different vendors, a juggler, musicians, children playing,
dogs running, birds flying, and a parade in the background, all with different clothing
and activities happening simultaneously"
```

_(Too many elements = unfocused, chaotic result)_

✅ **Solution**:

```
Wide shot of a bustling marketplace, vendors with colorful stalls in the foreground,
crowds of people moving through the aisles, warm afternoon light casting long shadows
across the cobblestone ground. Vibrant, energetic atmosphere, slightly blurred background
to suggest depth and activity.
```

_(Simplified, focused on mood and key elements)_

---

## Style Keyword Library

### Artistic Styles

**Photorealism**:

```
"photorealistic, professional photography, high detail, sharp focus"
```

**Anime/Manga**:

```
"anime style, soft cel shading, vibrant colors, expressive characters"
```

**Fantasy Illustration**:

```
"fantasy illustration style, painterly, rich colors, detailed environment"
```

**Film Noir**:

```
"film noir aesthetic, high contrast black and white, dramatic shadows, moody atmosphere"
```

**Cyberpunk**:

```
"cyberpunk aesthetic, neon lighting, rain-slicked streets, high tech low life, vibrant colors"
```

**Watercolor**:

```
"watercolor painting style, soft edges, flowing colors, artistic paper texture"
```

**Oil Painting**:

```
"oil painting style, visible brush strokes, rich colors, classical composition"
```

**Digital Concept Art**:

```
"digital concept art, detailed, professional illustration, game asset quality"
```

### Compositional Quality

**Cinematic**:

```
"cinematic composition, film-like framing, professional cinematography"
```

**Dramatic**:

```
"dramatic composition, strong contrasts, dynamic angles"
```

**Minimalist**:

```
"minimalist composition, clean simple background, focus on subject"
```

**Epic**:

```
"epic composition, grand scale, sweeping vista, breathtaking atmosphere"
```

---

## Workflow Integration

### Stage-Specific Guidelines

**Beat Board (9-panel)**: Establishing Visual Baseline

- Focus on defining character canonical appearance
- Establish setting details
- Define lighting approach
- Apply consistent style keywords
- Target: 80-150 words per prompt

**Sequence Board (4-panel)**: Continuous Motion

- Inherit character/setting from source beat
- Focus on action and camera movement
- Maintain screen direction (180-degree rule)
- Target: 80-150 words per prompt

**Motion Prompts**: Video Generation

- Simplify description (focus on motion, not exhaustive detail)
- Specify motion direction and speed
- Include camera movement if relevant
- Target: 40-80 words per prompt

---

## Quick Reference Checklist

Before finalizing an image prompt, verify:

- [ ] Shot type and camera angle specified
- [ ] Subject described with specific details
- [ ] Action/pose clearly defined
- [ ] Setting includes 2-4 key features
- [ ] Lighting direction and quality described
- [ ] Style keywords included
- [ ] Prompt is 80-150 words (40-80 for motion)
- [ ] Uses narrative descriptive style (not keyword list)
- [ ] Character description matches canonical form
- [ ] No conflicting elements

---

This guide is optimized for Gemini Imagen 3 but principles apply broadly to modern AI image generation models. Adjust specifics (e.g., negative prompts, technical quality keywords) based on your target model's capabilities.
