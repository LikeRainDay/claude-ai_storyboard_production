# Motion Prompt 输出格式（参考）

**此模板展示结构 - 最终输出不应包含这些说明**

## 最终输出应包含：

```markdown
# Motion Prompts - Episode {XX}

## Motion 1 (来自 Sequence A, Panel 1)

[40-80 词的动作导向提示词，描述运动、镜头、节奏、时长]

## Motion 2 (来自 Sequence B, Panel 1)

[40-80 词提示词]

...
```

## Motion Prompt 结构：

[主体] [主要动作] [方向] [+ 镜头运动]. [镜头规格]. [节奏]. [时长: X 秒].

## 示例：

```
A woman with silver hair in a crimson coat walks from left to right along a train platform,
wind blowing her hair. Camera pans right to follow her. Steady walking pace. 5 seconds.
```

## Agent 注意事项：

- 无需 frontmatter 元数据
- 无需模板说明
- 仅输出实际 motion prompts（每个 40-80 词）
- 着重于：运动、方向、速度、时长
- 比图像提示词更简化 - 着重动作
