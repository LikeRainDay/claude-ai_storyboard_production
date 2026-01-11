---
name: Animator Skill
description: AI视频生成的motion prompt方法论
version: 1.0.0
---

# Animator Skill (动画师技能)

此技能为 Animator 提供创建动态 motion prompts 的专业知识，优化用于 AI 视频生成工作流。

## 技能组件

### 1. **motion-prompt-methodology.md** 📖

Motion prompt 原则综合指南（参考用）：

- 简洁性和专注性（一个主要动作）
- 方向性和速度指定
- 主体与镜头运动的区分
- 视频时长的物理合理性
- 视频模型优化技术

### 2. **templates/motion-prompt-template.md**

- Motion prompt 输出的结构化格式

## 支持的视频平台

### Runway Gen-3 (推荐)

**优势**:

- 支持复杂运动
- 高质量输出
- 良好的物理一致性

**最佳时长**: 3-5 秒

### Pika Labs

**优势**:

- 快速生成
- 适合简单运动
- 易于使用

**最佳时长**: 3-4 秒

### Stable Video Diffusion (SVD)

**优势**:

- 开源免费
- 可本地部署
- 适合细微运动

**最佳时长**: 2-4 秒

### AnimateDiff

**优势**:

- 与 Stable Diffusion 集成
- 风格化动画
- 社区支持强

**最佳时长**: 1-3 秒

## 运动类型库

### 主体运动

**人物移动**:

```
walks from left to right
runs toward camera
turns slowly to face left
steps backward cautiously
```

**人物动作**:

```
reaches out with right hand
picks up object from table
opens door slowly
sits down in chair
stands up from seated position
```

**表情/姿态**:

```
head turns from left to right
smiles gradually
eyes widen in surprise
leans forward
```

### 镜头运动

**平移 (Pan)**:

```
camera pans left to right
camera pans right to left following subject
slow pan upward revealing environment
```

**推拉 (Dolly)**:

```
camera dollies forward toward subject
camera dollies backward revealing wider scene
slow dolly in on subject's face
```

**升降 (Crane/Boom)**:

```
camera rises slowly upward
camera descends from high angle to eye level
```

**环绕 (Orbit)**:

```
camera orbits around subject clockwise
camera circles subject from right to left
```

**其他**:

```
camera tilts up from feet to face
camera zooms in slowly
handheld camera movement, slight shake
static camera, no movement
```

### 自然运动

**风**:

```
wind blows hair gently to the right
leaves flutter in breeze
coat billows in strong wind
```

**水**:

```
water ripples expand outward
waves lap against shore
rain falls steadily
```

**光影**:

```
shadows lengthen gradually
light flickers across face
sunbeams stream through window
```

## 运动速度指导

### 慢速运动 (缓慢、渐进)

**用词**:

- slowly
- gradually
- gently
- drifts
- eases

**适用场景**:

- 情绪细腻时刻
- 悬念营造
- 美学展示

**时长**: 4-5 秒

### 中速运动 (平稳、正常)

**用词**:

- walks
- moves
- turns
- steady pace

**适用场景**:

- 日常动作
- 叙事推进
- 标准镜头

**时长**: 3-4 秒

### 快速运动 (迅速、突然)

**用词**:

- quickly
- swiftly
- rushes
- darts
- sudden

**适用场景**:

- 动作场景
- 惊吓时刻
- 紧迫感

**时长**: 2-3 秒

## 用途

Animator 使用此技能来：

- 将 4 格静态序列转换为时间运动描述
- 优化视频生成模型的提示词（Runway, Pika, SVD 等）
- 保持来自源序列的主体一致性
- 确保物理真实的运动描述
- 控制运动速度和方向
- 区分主体运动与镜头运动

## 何时使用此技能

Animator 应在以下情况参考此技能：

- 从批准的 sequence boards 创建 motion prompts
- 解决 Director 关于运动清晰度的反馈
- 确定时长的适当运动复杂度
- 指定镜头运动 vs 主体运动
- **选择运动类型时参考运动库**
- **选择运动速度时参考速度指导**
- 不确定视频平台特性时参考平台说明

## 关键原则

### 1. 简洁胜于复杂

**视频模型在专注、清晰的指令下表现更好**：

- 一个主要动作（非三个同时动作）
- 明确的方向性（从左到右、朝向镜头等）
- 真实的节奏（动作可在 3-5 秒内完成）
- 以主体为中心（比静态 prompts 更少的场景描述）

### 2. 物理合理性

**时长与动作匹配**:

```
3秒: 简单动作
- 转头
- 拿起物体
- 走2-3步
- 微笑

5秒: 中等动作
- 穿过小房间
- 坐下或站起
- 开门走入
- 转身走开

❌ 不现实:
- "角色跑100米" 在3秒
- "完整战斗序列" 在5秒
```

### 3. 运动优先，细节其次

**简化静态描述，强调运动**:

❌ **过度详细**:

```
A 25-year-old woman with waist-length straight silver hair, pale porcelain skin,
bright violet eyes, wearing a long black coat over a white high-neck shirt and
black pants, silver ring on right hand, walks from left to right...
```

✅ **运动优先**:

```
A woman with silver hair in a long black coat walks from left to right across
the train platform. Steady walking pace. 4 seconds.
```

### 4. 明确运动源

**清楚指明什么在动**:

```
主体运动: "Character walks left to right. Camera static."
镜头运动: "Flower static. Camera pans right slowly."
组合运动: "Athlete runs toward camera while camera dollies backward at matching speed."
```

## 输出约束

**严格禁止**:

- ❌ Frontmatter 元数据
- ❌ 模板说明
- ❌ "下一步"指令
- ❌ 超过 80 词的冗长描述
- ❌ 多个竞争性动作
- ❌ 物理上不可能的运动

**必须包含**:

- ✅ 40-80 词的简洁描述
- ✅ 一个清晰的主要动作
- ✅ 运动方向（left to right, toward camera 等）
- ✅ 速度/节奏（slowly, quickly 等）
- ✅ 时长（3 seconds, 5 seconds 等）
- ✅ 主体 vs 镜头运动的区分

## Motion Prompt 结构模板

```
[简化主体描述] [主要动作] [方向].
[镜头运动(如有)]. [速度描述]. [时长].
```

**示例**:

```
A woman with silver hair in a crimson coat walks from left to right along
a train platform, wind blowing her hair. Camera pans right to follow her.
Steady walking pace. 5 seconds.
```

## 常见错误与解决

### ❌ 错误: 过于冗长

```
In a beautifully lit Victorian study with dark wood paneling, ornate furniture,
floor-to-ceiling bookshelves filled with leather-bound volumes, and a large
mahogany desk, a detective in a grey suit with a fedora slowly enters through
the oak door... (120+ words)
```

✅ **解决**: 简化场景，强调运动

```
A detective in a grey suit enters a Victorian study through the oak door,
looking around cautiously. Camera static. Slow, deliberate pace. 4 seconds.
(25 words)
```

### ❌ 错误: 多个动作

```
Character runs forward, jumps over obstacle, spins in mid-air, draws sword,
and lands in fighting stance
```

✅ **解决**: 选择一个主要动作

```
Character runs forward and jumps over obstacle, landing in crouch. Fast pace.
3 seconds.
```

### ❌ 错误: 方向模糊

```
Character moves around the room
```

✅ **解决**: 明确方向

```
Character walks from background to foreground, approaching camera. Medium pace.
4 seconds.
```

### ❌ 错误: 不清楚什么在动

```
Scene shifts from left to right
```

✅ **解决**: 明确主体/镜头

```
Camera pans left to right across the cityscape. Buildings static. Smooth steady pan.
5 seconds.
```

## 技能激活

此技能对 Animator agent **始终可用**。所有 motion prompts 必须符合 methodology 和 template。

---

**用法**: Animator agent 自动引用此技能。Methodology 标记为 📖 仅在需要时参考。
