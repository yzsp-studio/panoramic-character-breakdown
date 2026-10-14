# Layer 7: 色彩系统层规范

> **何时 read**：生成多光照环境色标图、完整配色方案时。

## 核心目标

确保角色在不同光照环境下的颜色表现可预测、可复现。
不同于简单的配色板，色彩系统层定义了角色色彩在**真实光照条件下的动态变化**。

## 标准配色方案

### 色彩权重分配

| 类别 | 数量 | 权重 | 用途 |
|------|------|------|------|
| **主色** | 3 种 | 60% | 服装主体、头发 |
| **辅色** | 5 种 | 30% | 内搭、配饰、细节 |
| **强调色** | 2 种 | 10% | 眼睛、标志性元素、发光部件 |

### 色卡呈现规范

- 每个色块标注：色名 + HEX 色值 + 对应部位
- 色块按实际使用比例排列（大块在前）
- 避免使用渐变色和复杂图案
- 单独标注肤色和发色（这两项最容易被 AI 改变）

### Prompt 写法

```
character color palette sheet, [角色名],
[N] color swatches arranged by usage proportion,
each swatch labeled with HEX code and body part,
skin tone: [HEX], hair color: [HEX],
primary colors: [色名1] [HEX1], [色名2] [HEX2], [色名3] [HEX3],
secondary colors: [列举],
accent colors: [列举],
clean graphic design layout, white background
```

## 多光照环境色标图（Color Script）

### 四种标准光照条件

定义角色标准色值在不同光照下的**实际呈现效果**：

| 光照环境 | 色温 | 对角色色彩的影响 | Prompt 关键词 |
|---------|------|-----------------|-------------|
| **白天户外** | 5500K 中性 | 色彩最接近标准值 | `daylight, neutral white balance, clear sky` |
| **黄昏/黄金时刻** | 2500-3000K 暖 | 所有色彩偏暖，阴影偏紫蓝 | `golden hour warm light, orange tint, blue-purple shadows` |
| **夜晚/月光** | 7000K+ 冷 | 色彩整体偏蓝灰，饱和度降低 | `moonlight, cool blue tint, desaturated, dark ambient` |
| **室内暖光/火光** | 2000-3000K 极暖 | 色彩偏橙红，阴影偏深 | `warm indoor lighting, candlelight, tungsten orange cast` |
| **霓虹/人工光** | 混合色温 | 色彩受光源色影响，反射和混色 | `neon lights casting colored shadows, mixed color temperature` |

### 排版规范

- **横版 16:9 单图**，同一角色在 4-5 种光照下的半身像横排
- 每个面板上方标注光照环境名称和色温
- 下方附该环境下的简化色卡（主色在该光照下的实际显示色）
- 角色姿势和表情在所有面板中完全相同，仅光照变化

### Prompt 示例

```
color script reference sheet, [角色身份卡片],
same neutral standing pose in 4 different lighting conditions side by side:
Panel 1 "Daylight 5500K" — neutral white balance outdoor sunlight,
Panel 2 "Golden Hour 3000K" — warm low sun orange-golden tones,
Panel 3 "Moonlight 7000K" — cool blue night ambient,
Panel 4 "Indoor Warm 2500K" — tungsten warm indoor candlelight,
each panel labeled with lighting name,
consistent character appearance across all panels,
white border between panels, exactly 4 panels
```

## 季节色彩变体（可选扩展）

当角色需要跨季节出现时，定义季节性色彩调整：

| 季节 | 色彩调整方向 |
|------|------------|
| 春 | 饱和度略提升，增加粉绿色调 |
| 夏 | 高饱和，明度提升，对比加强 |
| 秋 | 偏暖，饱和度略降，增加橙棕色调 |
| 冬 | 饱和度降低，偏冷灰，增加蓝白色调 |
