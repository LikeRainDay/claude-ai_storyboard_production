---
name: Film Storyboard Skill
description: 影视分镜方法论、提示词写法指南和模板
version: 1.0.0
---

# Film Storyboard Skill (影视分镜技能)

此技能为 Storyboard Artist 提供专业的影视分镜方法论和提示词生成能力。

## 技能组件

### 1. **storyboard-methodology-playbook.md** 📖

分镜方法论完整指南（参考用）：

- 四大支柱：清晰、简洁、一致、渐进
- Beat breakdown 方法论
- 镜头构图和摄影
- 连贯性管理
- AI 图像生成特殊技巧
- **高级电影技巧**：蒙太奇、转场、时空处理

### 2. **gemini-image-prompt-guide.md** 📖

提示词写法指南（参考用）：

- 叙事描述式风格（非关键词堆砌）
- 提示词结构模板
- 角色一致性技巧
- 光影描述方法
- **Nano Banner 格式优化**（新增）
- Gemini/Midjourney 优化建议

### 3. **Templates**

- `beat-breakdown-template.md` — Beat breakdown 输出格式
- `beat-board-template.md` — Beat board (9 宫格)输出格式
- `sequence-board-template.md` — Sequence board (4 格)输出格式

## 平台支持

### Nano Banner（默认推荐）

**格式**: Episode Visual Script 模式

- 9 个 beats，每个 beat 包含 Visual Description + Lighting & Mood
- 优化用于 nano banner 3x3 网格生成
- 单次生成完整 9 宫格，保证一致性

### Midjourney v6

**格式**: 独立 prompts + 参数

- 每个 beat 独立 prompt
- 包含`--ar 16:9 --style cinematic --v 6`参数
- 网格位置标注

### Gemini Imagen 3 / DALL-E 3

**格式**: 标准叙事描述式 prompts

- 无特殊参数要求
- 依赖详细的叙事描述

## 视觉风格候选

### 推荐风格组合

**写实风格**:

```
photorealistic, professional photography, cinematic lighting, high detail
```

**动漫风格**:

```
anime style, soft cel shading, vibrant colors, expressive characters
```

**概念艺术风格**:

```
digital concept art, painterly style, dramatic atmosphere, detailed environment
```

**电影黑色风格**:

```
film noir aesthetic, high contrast black and white, dramatic shadows, moody atmosphere
```

**赛博朋克风格**:

```
cyberpunk aesthetic, neon lighting, rain-slicked streets, vibrant pink and cyan colors
```

**奇幻插画风格**:

```
fantasy illustration style, painterly, rich colors, epic composition
```

**水彩风格**:

```
watercolor painting style, soft edges, flowing colors, artistic paper texture
```

### 光影方案候选

**黄金时刻**:

```
warm golden hour sunlight, long soft shadows, orange and amber tones
```

**蓝色时刻**:

```
cool blue twilight, soft gradient from purple to dark blue, minimal shadows
```

**电影光影**:

```
cinematic lighting, dramatic contrast, three-point lighting setup
```

**自然柔光**:

```
soft diffused natural light, even illumination, gentle shadows
```

**霓虹夜景**:

```
vibrant neon lighting in pink and cyan, colored reflections, high contrast
```

**戏剧性侧光**:

```
dramatic side lighting, split lighting effect, deep shadows
```

### 宽高比选项

- `16:9` - 宽屏电影（推荐）
- `1:1` - 方形（Instagram）
- `9:16` - 竖屏（TikTok, Reels）
- `4:3` - 传统电视
- `21:9` - 超宽电影

## 用途

Storyboard Artist 使用此技能来：

- 从剧本中识别和提取 9 个关键叙事节拍
- 生成 9 宫格 beat board 提示词（建立视觉基准）
- 生成 4 格 sequence board 提示词（展开连续镜头）
- 保持角色外观、场景、光色的一致性
- 遵循专业分镜方法论标准
- **针对不同平台优化输出格式**

## 何时使用此技能

Storyboard Artist 应在以下情况参考此技能：

- 生成 beat breakdown 时参考 beat selection criteria
- 生成 beat board 时参考 prompt writing guide 和平台格式要求
- 生成 sequence board 时参考 continuity rules
- 解决 Director 关于一致性的反馈时参考 methodology
- 不确定提示词格式时参考 templates
- **选择视觉风格时参考风格候选列表**
- **针对 nano banner 优化时参考特定格式指导**

## 核心原则

### 四大支柱（4C Framework）

1. **Clear 清晰**: 每个提示词明确无歧义
2. **Concise 简洁**: 详细但不臃肿（Visual Description: 80-120 词，Lighting & Mood: 30-50 词）
3. **Consistent 一致**: 角色/场景/光色在所有 prompts 中保持一致
4. **Progressive 渐进**: 9 宫格 →4 宫格逐层细化，不矛盾

### 分层渐进流程

```
Beat Breakdown (9个锚点)
  ↓ 继承叙事结构
Beat Board (9宫格) — 建立视觉基准（角色、场景、光色）
  ↓ 继承视觉元素
Sequence Board (4格) — 展开动作序列，保持一致性
```

### 关键约束

**输出规则**:

- ❌ **禁止 frontmatter 元数据**（如`---\nepisode: ep01\n---`）
- ❌ **禁止模板说明**（如"此模板..."、"注意事项"）
- ❌ **禁止 Next/下一步指令**
- ✅ **仅输出实际内容**（prompts 本身）

**Nano Banner 特殊要求**:

- 使用 Episode Visual Script 格式
- Visual Description: 80-120 词（详细视觉）
- Lighting & Mood: 30-50 词（光影氛围）
- 9 个 beats 完整结构

**角色一致性**:

- 建立规范描述（canonical description）
- 所有 prompts 逐字重复关键识别符
- 外观、服装、特征标记保持 100%一致

## Nano Banner 格式指导

Nano banner 需要特殊的 Episode Visual Script 格式，**不同于**标准 Gemini 提示词：

### 标准格式

```markdown
EPISODE {XX}: BEAT BOARD VISUAL SCRIPT

Beat 1: [Beat 标题]
Visual Description: [镜头类型]. [角色规范描述] [动作/姿势] [场景细节] [关键视觉元素]. [80-120 词]
Lighting & Mood: [光影方向、质量、色温] [情绪氛围]. [30-50 词]

Beat 2: [Beat 标题]
Visual Description: ...
Lighting & Mood: ...

[继续 Beat 3-9]
```

### 与 Gemini 格式的区别

| 特性 | Nano Banner                               | Gemini/Midjourney |
| ---- | ----------------------------------------- | ----------------- |
| 结构 | Visual Description + Lighting & Mood 分离 | 单一 prompt 块    |
| 长度 | 80-120 词 + 30-50 词                      | 80-150 词总计     |
| 格式 | Episode Visual Script                     | 叙事描述式        |
| 输出 | 一次生成完整 3x3 网格                     | 逐个生成          |

## 技能激活

此技能对 Storyboard Artist agent **始终可用**。所有分镜输出必须符合 methodology 和 templates。

---

**用法**: Storyboard Artist agent 自动引用此技能。Methodology 和 guide 标记为 📖 仅在需要时参考。
