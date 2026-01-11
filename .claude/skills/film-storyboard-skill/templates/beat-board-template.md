# Beat Board 输出格式（参考）

**此模板展示正确的 nano banner 输出结构**

**❌ 严禁输出**：

- Frontmatter 元数据（`---\nepisode: ep01\n---`）
- 模板说明、注意事项
- "下一步"或 workflow 指令
- 任何非 prompt 内容

**✅ 仅输出**：实际的 beat board 内容（见下方格式）

---

## Nano Banner 格式（默认 - 推荐）:

```markdown
EPISODE {XX}: BEAT BOARD VISUAL SCRIPT

Visual Description: [详细视觉描述：镜头类型、角色/主体、动作、场景、关键视觉元素 - 80-120 词]
Lighting & Mood: [灯光方向、质量、色温和情绪氛围 - 30-50 词]

Beat 2: [Beat 标题]
Visual Description: ...
Lighting & Mood: ...

Beat 3: [Beat 标题]
Visual Description: ...
Lighting & Mood: ...

Beat 4: [Beat 标题]
Visual Description: ...
Lighting & Mood: ...

Beat 5: [Beat 标题]
Visual Description: ...
Lighting & Mood: ...

Beat 6: [Beat 标题]
Visual Description: ...
Lighting & Mood: ...

Beat 7: [Beat 标题]
Visual Description: ...
Lighting & Mood: ...

Beat 8: [Beat 标题]
Visual Description: ...
Lighting & Mood: ...

Beat 9: [Beat 标题]
Visual Description: ...
Lighting & Mood: ...
```

## 为什么这个格式适合 Nano Banner:

1. **清晰结构** - 每个 beat 明确标注
2. **关注点分离** - Visual description 独立于 lighting/mood
3. **一致格式** - 便于 nano banner 解析
4. **叙事流** - 读起来像视觉脚本
5. **角色一致性** - 规范描述在所有 beats 中重复

## Midjourney v6 格式:

```markdown
## Beat 1: [标题] (左上)

[详细提示词] --ar 16:9 --style cinematic --v 6

## Beat 2: [标题] (中上)

...
```

## Gemini/DALL-E 格式:

各个 beat 提示词，无特殊格式要求。

## Agent 注意事项：

- **无需 frontmatter 元数据**
- **无需模板说明**
- **使用一致的角色规范描述**
- **Visual Description 应详细** (80-120 词)
- **Lighting & Mood 应具体** (30-50 词)
- **叙事英文提示词**（AI 兼容性）
