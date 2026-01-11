# AI 分镜制作系统

基于 Claude Agent + Skill 架构构建的 AI 驱动分镜师系统，用于自动化影视分镜工作流程。

## 系统概览

此系统协调一个**Producer**与四个专业子 agent，自动生成结构化的分镜提示词：

```
Producer Agent (CLAUDE.md)
├── Scriptwriter — 生成故事剧本
├── Storyboard Artist — 创建beat breakdowns、9宫格、4格提示词
├── Director — 审查所有输出进行质量控制
└── Animator — 生成视频生成的motion prompts
```

### 核心价值

- **效率提升**：从概念到提示词的自动化工作流，减少约 80%的手动工作
- **一致性保证**：严格的角色/场景/光影继承减少 AI 生成的随机性
- **专业标准**：基于影视分镜方法论，遵循摄影和剪辑原则
- **质量控制**：自动化导演审查与修订循环
- **可恢复**：文档驱动，中断后可通过查看进度恢复
- **多平台**：支持 Nano Banner、Midjourney、Gemini、DALL-E

## 完整工作流程

### 5 阶段完整流程

```
0. 剧本生成 (故事创作)
   输入: 故事概念、类型、主题
   输出: 完整剧本，包含场景、角色、对话

1. Beat Breakdown (9个关键叙事时刻)
   输入: 剧本 + 视觉风格配置
   输出: 9个关键叙事锚点
   审查: Director检查完整性、清晰度、选择质量

2. Beat Board (9宫格分镜)
   输入: 已批准的beat breakdown
   输出: 9个静态图像提示词（视觉基准）
   审查: Director检查一致性、覆盖度、提示词格式

3. Sequence Board (4格序列)
   输入: 已批准的beat board
   输出: 连续4镜头序列提示词（展开关键时刻）
   审查: Director检查运动连贯性、轴线稳定性、继承规则

4. Motion Prompts (视频生成)
   输入: 已批准的sequence board
   输出: 视频模型的动态motion prompts
   审查: Director检查简洁性、物理可行性、焦点

所有提示词使用英文以获得最佳AI兼容性
```

## 项目结构

```
project/
├── script/                              # 剧本源文件（用户创建）
│   ├── ep01-awakening.md
│   └── ep02-revelation.md
│
├── outputs/                             # 生成的artifacts（自动创建）
│   ├── beat-breakdown-ep01.md           # Beat breakdown
│   ├── beat-board-prompt-ep01.md        # 9宫格提示词
│   ├── sequence-board-prompt-ep01.md    # 4格序列提示词
│   └── motion-prompt-ep01.md            # Motion prompts
│
└── .claude/                             # 系统配置
    ├── agents/                          # Agent定义
    │   ├── storyboard-artist.md
    │   ├── director.md
    │   ├── animator.md
    │   └── scriptwriter.md
    │
    └── skills/                          # Skill包
        ├── film-storyboard-skill/       # 分镜方法论
        ├── storyboard-review-skill/     # 审查标准
        ├── animator-skill/              # Motion prompt方法论
        └── scriptwriter-skill/          # 剧本创作方法论
```

## 快速开始

### 1. 创建剧本

在`script/`目录创建新的 episode 剧本：

```markdown
# Episode 01: 觉醒

> **系列连续性说明**: 系列首集，介绍主角和世界观。

## 场景 1 - INT. Emma 公寓 - 清晨

小小的单间公寓，阳光透过脏污的窗户洒入...

EMMA（25 岁，银色齐腰长直发，苍白肤色，紫罗兰色眼睛，
穿黑色长风衣和白色高领衫）坐在床边...
```

### 2. 生成 Beat Breakdown

与 Claude 交互：

```
请为ep01生成beat breakdown
```

系统将自动：

1. Scriptwriter 读取`script/ep01-awakening.md`
2. Storyboard Artist 识别 9 个关键叙事时刻
3. Director 审查质量
4. 输出到`outputs/beat-breakdown-ep01.md`

### 3. 生成 Beat Board (9 宫格)

```
请为ep01生成beat board
```

系统将：

1. Storyboard Artist 基于 approved breakdown 创建 9 个提示词
2. 应用 visual style 和 platform 配置
3. Director 审查一致性
4. 输出到`outputs/beat-board-prompt-ep01.md`

### 4. 生成 Sequence Board (4 格)

```
请为ep01生成sequence board
```

系统将：

1. Storyboard Artist 从 9 个 beats 中选择关键 beat
2. 展开为 4 镜头连续序列
3. Director 检查运动连贯性和轴线规则
4. 输出到`outputs/sequence-board-prompt-ep01.md`

### 5. 生成 Motion Prompts

```
请为ep01生成motion prompts
```

系统将：

1. Animator 将 4 格序列转换为 motion prompts
2. 优化用于视频生成模型
3. Director 审查物理合理性
4. 输出到`outputs/motion-prompt-ep01.md`

## 视觉风格配置

系统支持多种预设风格和平台：

### 风格预设

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

### 支持的平台

**Nano Banner** (默认推荐):

- 3x3 网格，一次性生成 9 个 beats
- Episode Visual Script 格式
- Visual Description (80-120 词) + Lighting & Mood (30-50 词)

**Midjourney v6**:

- 独立 prompts + 参数
- `--ar 16:9 --style cinematic --v 6`

**Gemini Imagen 3 / DALL-E 3**:

- 标准叙事描述式 prompts
- 无特殊参数要求

## 核心方法论

### 四大支柱 (4C Framework)

1. **Clear (清晰)**: 每个提示词明确无歧义
2. **Concise (简洁)**: 详细但不臃肿
   - Visual Description: 80-120 词
   - Lighting & Mood: 30-50 词
   - Motion Prompt: 40-80 词
3. **Consistent (一致)**: 角色/场景/光影在所有 prompts 中保持一致
4. **Progressive (渐进)**: 9 宫格 →4 宫格逐层细化，继承视觉元素

### 分层渐进流程

```
Beat Breakdown (9个锚点)
  ↓ 继承叙事结构
Beat Board (9宫格) — 建立视觉基准（角色、场景、光色）
  ↓ 继承视觉元素
Sequence Board (4格) — 展开动作序列，保持一致性
  ↓ 继承主体描述
Motion Prompts — 转换为时间动态描述
```

## 关键约束

### 角色一致性

**规范描述**（在 Beat 1 建立）：

```
A young woman in her late 20s with waist-length straight silver hair,
pale porcelain skin, and bright violet eyes, wearing a long black coat
over a white high-neck shirt
```

**在所有后续 beats 中逐字重复**关键识别符：

- 发型、发色、发长
- 眼睛颜色
- 主要服装
- 肤色
- 显著标记

### 输出纯净性

**严格禁止**在输出文件中包含：

- ❌ Frontmatter 元数据（`---\nepisode: ep01\n---`）
- ❌ 模板说明或注释
- ❌ "下一步"指令
- ❌ 任何非 prompt 内容

**仅输出**：实际的提示词内容本身

## 高级功能

### 系列连续性

Scriptwriter 支持查看之前的剧集并创作续集：

```
基于ep01和ep02，为ep03设想一个关于背叛的故事
```

系统将：

1. 读取`script/ep01-*.md`和`script/ep02-*.md`
2. 分析角色发展和未解决情节线
3. 基于用户输入创作新剧集
4. 保持角色外观和世界观一致性

### 专业电影技巧

系统包含高级电影技巧支持：

**蒙太奇**:

- Narrative Montage (叙事) - 压缩时间
- Thematic Montage (主题) - 对比并置
- Parallel Montage (平行) - 交叉剪辑

**转场**:

- Cut, Match Cut, Dissolve
- Fade to Black, Smash Cut
- 每种都有使用时机指导

**时空处理**:

- Flashback (闪回) - 含视觉指标
- Dream Sequence (梦境)
- Slow Motion (慢动作)
- Time Lapse (延时)
- Freeze Frame (定格)

### 质量控制

Director 自动审查每个阶段，提供 PASS/FAIL 判决：

**审查标准**：

- Beat 数量正确
- 描述清晰具体
- 角色外观一致
- 镜头规格完整
- 物理合理性
- 无跳切或轴线违规

**修订循环**：

- FAIL → Storyboard Artist 修订 → Director 复审
- 连续 3 次 FAIL → 升级给 Producer/用户干预

## Agent 架构

### Producer (CLAUDE.md)

你（Claude）作为 Producer：

- 协调所有 sub-agents
- 理解用户意图
- 调度工作流程
- 处理升级问题

### Scriptwriter

**职责**：

- 创作结构化剧本
- 查看之前剧集保持连续性
- 基于用户输入设想新故事
- 提供 ≥9 个 beats 候选

**Skills**: `scriptwriter-skill`

### Storyboard Artist

**职责**：

- 从剧本识别 9 个关键 beats
- 生成 9 宫格 beat board 提示词
- 生成 4 格 sequence board 提示词
- 保持角色/场景/光影一致性

**Skills**: `film-storyboard-skill`

### Director

**职责**：

- 审查所有 outputs (beat breakdown, beat board, sequence board, motion prompts)
- 提供 PASS/FAIL 判决
- 指出具体问题和修复建议
- 仅读取，不创作

**Skills**: `storyboard-review-skill`

### Animator

**职责**：

- 将 4 格静态序列转换为 motion prompts
- 优化用于 AI 视频生成模型
- 保持主体一致性
- 确保物理合理的运动

**Skills**: `animator-skill`

## Skill 架构 (2.0 标准化)

所有 Skills 已按照 [Claude Code 官方标准](https://code.claude.com/docs/en/skills) 重构，采用**渐进式披露**模式。

### film-storyboard-skill

**核心文件**:

- `SKILL.md` (139 行) - 概述、核心原则、快速开始、导航
- `REFERENCE.md` 📖 - 平台特性和风格库（渐进式披露）
  - Nano Banner vs Midjourney vs Gemini 格式对比
  - 7 种视觉风格库（写实、动漫、概念艺术等）
  - 6 种光影方案候选
  - 宽高比选项
- `storyboard-methodology-playbook.md` 📖 - 完整方法论
- `gemini-image-prompt-guide.md` 📖 - 提示词写法指南
- `templates/` - 输出模板

### scriptwriter-skill

**核心文件**:

- `SKILL.md` (175 行) - 概述、核心原则、快速开始、导航
- `GUIDELINES.md` 📖 - 详细写作规范（渐进式披露）
  - 场景格式规范
  - 角色首次出场规则
  - Beats 分布指导
  - 对话写作技巧
- `screenplay-methodology.md` 📖 - 剧本创作方法论
- `templates/` - 输出模板

### animator-skill

**核心文件**:

- `SKILL.md` (225 行) - 概述、核心原则、快速开始、导航
- `MOTION_LIBRARY.md` 📖 - 完整运动库（渐进式披露）
  - 主体运动库（人物移动、动作、表情）
  - 镜头运动库（Pan、Dolly、Crane、Orbit）
  - 自然运动（风、水、光影）
  - 运动速度指导
  - 平台特性和优化
- `motion-prompt-methodology.md` 📖 - Motion prompt 方法论
- `templates/` - 输出模板

### storyboard-review-skill

**核心文件**:

- `SKILL.md` (68 行) - 审查理念和检查清单引用
- `review-checklist.md` - 详细审查标准

## 技术细节

### 文件命名规范

```
script/ep{XX}-{title}.md               # 剧本
outputs/beat-breakdown-ep{XX}.md       # Beat breakdown
outputs/beat-board-prompt-ep{XX}.md    # Beat board
outputs/sequence-board-prompt-ep{XX}.md # Sequence board
outputs/motion-prompt-ep{XX}.md        # Motion prompts
```

### Nano Banner 3x3 网格

9 个 beats 对应网格位置：

```
┌─────────┬─────────┬─────────┐
│ Beat 1  │ Beat 2  │ Beat 3  │
│ 左上    │ 中上    │ 右上    │
├─────────┼─────────┼─────────┤
│ Beat 4  │ Beat 5  │ Beat 6  │
│ 左中    │ 中心    │ 右中    │
├─────────┼─────────┼─────────┤
│ Beat 7  │ Beat 8  │ Beat 9  │
│ 左下    │ 中下    │ 右下    │
└─────────┴─────────┴─────────┘
```

### 提示词语言

- **中文**: 系统内部交互、说明、元数据
- **英文**: 实际的 AI 提示词内容
  - Visual Description
  - Lighting & Mood
  - Motion Prompts

**原因**: AI 图像/视频模型在英文提示词下表现最佳

## 示例输出

### Beat Board (Nano Banner 格式)

```markdown
EPISODE 01: BEAT BOARD VISUAL SCRIPT

Beat 1: The Isolated Spark
Visual Description: Wide shot, high angle. A young woman in her late 20s
with waist-length straight silver hair, pale porcelain skin, and bright
violet eyes, wearing a long black coat over a white high-neck shirt, stands
alone on a crowded train platform. Commuters rush past her in blurred motion
while she remains perfectly still, staring at an ancient leather-bound journal
in her hands. Modern metropolitan subway station with fluorescent lighting
and yellow safety lines on the ground.
Lighting & Mood: Harsh overhead fluorescent lights creating flat, institutional
illumination. Cool blue-white color temperature. Isolated, contemplative
atmosphere with contrast between her stillness and surrounding chaos.

Beat 2: Crossing the Threshold
Visual Description: Medium shot, eye-level. The silver-haired woman in the
long black coat sits in a dimly lit subway car...
Lighting & Mood: Flickering cool fluorescent overhead light mixing with warm
amber glow from the journal pages...

[继续 Beat 3-9...]
```

### Motion Prompt

```markdown
序列 1 (基于 Beat 1-2)

A woman with long silver hair in a black coat walks from left to right along
a train platform, wind blowing her hair gently. Other commuters move quickly
past in opposite direction. Camera static, eye-level. Steady walking pace,
contemplative mood. 5 seconds.
```

## 最佳实践

### 创作高质量剧本

1. **视觉化优先** - 用可视化动作描述，避免抽象心理描写
2. **角色首次出场** - 提供完整外观描述
3. **足够的 beats** - 确保 ≥9 个清晰的关键时刻
4. **三幕结构** - Setup (25%) → Confrontation (50%) → Resolution (25%)

### 保持一致性

1. **建立规范** - 在 Beat 1 确定角色外观
2. **逐字重复** - 关键识别符在所有 beats 中完全相同
3. **继承规则** - 4 格序列必须继承源 9 格的视觉元素
4. **检查清单** - 使用 Director 的审查标准自查

### 优化提示词

1. **叙事描述式** - 流畅句子，非关键词堆砌
2. **适当长度** - Visual Description 80-120 词，Lighting & Mood 30-50 词
3. **明确镜头** - 每个提示词包含镜头类型和角度
4. **光影描述** - 指定光源、方向、色温、氛围

## 故障排除

### Beat Board 一致性问题

**症状**: Director 反馈角色外观不一致

**解决**:

1. 检查 Beat 1 的规范描述
2. 确保所有 beats 使用相同的关键词
3. 验证服装、发型、眼睛颜色等完全匹配

### Sequence Board 跳切

**症状**: Director 指出轴线违规或跳切

**解决**:

1. 检查屏幕方向（180 度法则）
2. 确保镜头类型变化明显
3. 添加过渡指示（Cut, Dissolve 等）

### Motion Prompt 过长

**症状**: Director 反馈超过 80 词

**解决**:

1. 简化场景描述
2. 专注于运动本身
3. 移除过度的视觉细节

## 系统要求

- Claude Code 或 claude.ai/code
- 工作区：本地文件系统访问
- 无需外部依赖

## 许可

本系统为内部工具，方法论基于公开的影视制作标准。

## 贡献

改进建议：

- 新的视觉风格预设
- 额外的电影技巧文档
- 更多的模板示例
- 平台特定优化

---

**系统版本**: 2.0 (Skills 标准化)
**最后更新**: 2026-01-11
**Agents**: 4 个专业 sub-agents
**Skills**: 4 个标准化技能包（渐进式披露模式）
**Skills 总行数**: 607 行（优化 -39.4%）
**符合标准**: 100% [Claude Code 官方标准](https://code.claude.com/docs/en/skills)
