# Sequence Board 输出格式（参考）

**此模板展示 4 格 sequence board 的结构**

**❌ 严禁输出**：

- Frontmatter 元数据
- 模板说明
- "下一步"指令
- 任何非内容的说明

**✅ 仅输出**：实际的 sequence board 内容

---

## 最终输出格式：

```markdown
# Sequence Board - Episode {XX}

## Sequence A: [来自 Beat X]

### Panel 1

[Shot type]. [详细视觉描述，继承 beat board 的角色/场景/光色]

### Panel 2

[Shot type]. [连续动作描述]

### Panel 3

[Shot type]. [连续动作描述]

### Panel 4

[Shot type]. [连续动作描述]

## Sequence B: [来自 Beat Y]

### Panel 1

...

### Panel 2

...

### Panel 3

...

### Panel 4

...
```

## 关键要求：

- **继承一致性**: 必须继承对应 beat board 的角色描述、场景设定、光色方案
- **动作连贯**: 4 个 panels 之间动作连续，无跳跃
- **轴线稳定**: 遵守 180 度法则
- **镜头流畅**: Panel 间的转换自然

## Agent 注意事项：

- 无需 frontmatter 元数据
- 无需模板说明
- 每个 sequence 恰好 4 个 panels
- 必须基于已批准的 beat board
- 叙事英文提示词（AI 兼容性）
