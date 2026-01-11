# Animator Skill - Motion Library

本文档包含完整的运动类型库、速度指导和平台特性参考。仅在需要选择运动类型或优化平台输出时查阅。

---

## 运动类型库

### 主体运动

#### 人物移动

```
walks from left to right
runs toward camera
turns slowly to face left
steps backward cautiously
walks diagonally across frame
approaches from background to foreground
exits frame left
```

#### 人物动作

```
reaches out with right hand
picks up object from table
opens door slowly
sits down in chair
stands up from seated position
points finger forward
waves hand greeting
kneels down carefully
```

#### 表情/姿态

```
head turns from left to right
smiles gradually
eyes widen in surprise
leans forward
tilts head questioningly
looks up slowly
nods in agreement
raises eyebrow
```

---

### 镜头运动

#### 平移 (Pan)

```
camera pans left to right
camera pans right to left following subject
slow pan upward revealing environment
camera pans down from sky to ground
horizontal pan across cityscape
```

#### 推拉 (Dolly)

```
camera dollies forward toward subject
camera dollies backward revealing wider scene
slow dolly in on subject's face
dolly out from close-up to establish shot
camera pushes in slowly
```

#### 升降 (Crane/Boom)

```
camera rises slowly upward
camera descends from high angle to eye level
crane up revealing landscape
boom down to character level
vertical descent following falling object
```

#### 环绕 (Orbit)

```
camera orbits around subject clockwise
camera circles subject from right to left
360-degree rotation around central subject
arc around object revealing different angles
```

#### 其他镜头运动

```
camera tilts up from feet to face
camera tilts down from face to hands
camera zooms in slowly
camera zooms out revealing context
handheld camera movement, slight shake
tracking shot following character
static camera, no movement
```

---

### 自然运动

#### 风

```
wind blows hair gently to the right
leaves flutter in breeze
coat billows in strong wind
curtains sway in wind
dust particles drift in air current
flag waves vigorously
```

#### 水

```
water ripples expand outward
waves lap against shore
rain falls steadily
droplets run down window
water drips from ceiling
stream flows gently
```

#### 光影

```
shadows lengthen gradually
light flickers across face
sunbeams stream through window
shadow moves across wall
light fades to darkness
sun rays pierce through clouds
```

#### 其他自然元素

```
snow falls softly
fire flickers and dances
smoke rises slowly
clouds drift across sky
fog rolls in gradually
petals fall from tree
```

---

## 运动速度指导

### 慢速运动 (Slow, Gradual)

**关键词**:

- slowly
- gradually
- gently
- softly
- drifts
- eases
- creeps
- lingers

**适用场景**:

- 情绪细腻时刻
- 悬念营造
- 美学展示
- 柔和过渡
- 沉思氛围

**时长**: 4-5 秒

**示例**:

```
A woman slowly turns her head toward the window. Gentle, deliberate movement.
5 seconds.
```

---

### 中速运动 (Normal, Steady)

**关键词**:

- walks
- moves
- turns
- steady pace
- normal speed
- regular motion
- consistent rhythm

**适用场景**:

- 日常动作
- 叙事推进
- 标准镜头
- 真实生活节奏
- 自然对话场景

**时长**: 3-4 秒

**示例**:

```
A man walks across the room from left to right, picking up a book from the table.
Steady walking pace. 4 seconds.
```

---

### 快速运动 (Fast, Sudden)

**关键词**:

- quickly
- swiftly
- rapidly
- rushes
- darts
- sudden
- bursts
- snaps

**适用场景**:

- 动作场景
- 惊吓时刻
- 紧迫感
- 追逐序列
- 突发反应

**时长**: 2-3 秒

**示例**:

```
A detective suddenly turns around, eyes wide, hand reaching for weapon.
Quick, sharp movement. 2 seconds.
```

---

## 支持的视频平台

### Runway Gen-3 (推荐)

**优势**:

- 支持复杂运动
- 高质量输出（1080p+）
- 良好的物理一致性
- 多种运动类型支持

**最佳时长**: 3-5 秒
**推荐运动**: 复杂的镜头运动 + 主体运动组合

**优化技巧**:

- 明确指定 camera movement
- 避免过多同时运动
- 使用方向性描述（left to right, toward camera）

---

### Pika Labs

**优势**:

- 快速生成
- 适合简单运动
- 易于使用
- 良好的连贯性

**最佳时长**: 3-4 秒
**推荐运动**: 单一主体运动或简单镜头平移

**优化技巧**:

- 保持运动简单专注
- 清晰的起始和结束状态
- 避免复杂多层运动

---

### Stable Video Diffusion (SVD)

**优势**:

- 开源免费
- 可本地部署
- 适合细微运动
- 社区支持强

**最佳时长**: 2-4 秒
**推荐运动**: 微妙的表情变化、轻微镜头运动

**优化技巧**:

- 专注于细节运动
- 避免大幅度动作
- 利用静态背景

---

### AnimateDiff

**优势**:

- 与 Stable Diffusion 集成
- 风格化动画
- 社区支持强
- 可控性高

**最佳时长**: 1-3 秒
**推荐运动**: 风格化动作、艺术化运动

**优化技巧**:

- 利用 motion modules
- 保持风格一致性
- 适合非真实感动画

---

## 运动组合模式

### 静态主体 + 镜头运动

```
Flower stands still in center of frame. Camera orbits around it clockwise.
Smooth steady rotation. 5 seconds.
```

**适用**: 产品展示、美学镜头、环境建立

---

### 动态主体 + 静态镜头

```
Runner sprints from left to right across frame. Camera static, wide shot.
Fast running pace. 3 seconds.
```

**适用**: 动作序列、追逐场景、运动展示

---

### 同步运动（跟拍）

```
Athlete runs toward camera while camera dollies backward at matching speed,
maintaining consistent distance. Medium running pace. 4 seconds.
```

**适用**: 对话行走、追逐场景、动态展示

---

### 对比运动

```
Character walks slowly left to right in foreground while camera pans right
to left, creating parallax effect. Slow walking, steady pan. 5 seconds.
```

**适用**: 艺术镜头、视觉深度、情绪表达

---

## 物理合理性检查

### 时长与动作匹配

**3 秒适合的动作**:

- 转头 180 度
- 拿起桌上物体
- 走 2-3 步
- 微笑表情变化
- 简单手势

**5 秒适合的动作**:

- 穿过小房间
- 坐下或站起
- 开门走入
- 转身走开
- 镜头环绕 180 度

**❌ 不现实的组合**:

- "角色跑 100 米" 在 3 秒 (人类极限 ~9 秒)
- "完整战斗序列" 在 5 秒
- "汽车从静止加速到高速" 在 2 秒

---

## 常见运动组合示例

### 情绪转折时刻

```
Character standing still, slowly looks up, eyes widen in realization.
Camera static. Gradual expression change. 4 seconds.
```

### 发现/揭示

```
Camera dollies forward toward mysterious box on table. Box static.
Slow steady dolly. 5 seconds.
```

### 环境建立

```
Camera pans left to right across cityscape at sunset. Static buildings,
moving clouds. Smooth steady pan. 5 seconds.
```

### 对抗/冲突

```
Two characters walk toward each other from opposite sides of frame,
stopping face to face. Camera static. Steady walk. 4 seconds.
```

### 离开/结束

```
Character walks away from camera toward door in background. Camera static.
Slow walking pace. 5 seconds.
```

---

## 使用建议

1. **先确定主要运动** - 主体运动还是镜头运动？
2. **选择速度** - 慢速/中速/快速，匹配情绪
3. **检查时长** - 运动能在指定时长内完成吗？
4. **参考平台特性** - 所选平台支持这种复杂度吗？
5. **简化描述** - 去掉非运动相关的细节

---

**刷新日期**: 本库根据主流 AI 视频平台能力定期更新。
