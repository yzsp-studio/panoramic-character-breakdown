# Layer 4: 服饰拆解层规范

> **何时 read**：生成服装分层图、变装设定、细节/材质特写时。

## 核心目标

通过外部元素讲述角色的背景、职业和性格故事。
服装不是"穿什么"，是"角色是谁"的视觉表达。

## 服装分层/分解图（Costume Breakdown）

### 分层逻辑

将角色着装从内到外逐层拆解，每一层独立展示：

```
Layer 0: 内衣/贴身衣物
Layer 1: 内搭（衬衫/T恤/打底）
Layer 2: 外套/上衣（西装/夹克/大衣）
Layer 3: 下装（裤子/裙子）
Layer 4: 鞋子
Layer 5: 外层附件（披风/围巾/腰带）
Layer 6: 配饰（手表/耳环/项链/帽子/眼镜）
```

### 排版规范

- **横版 16:9 单图**，从左到右按穿戴顺序排列
- 每层衣物独立展示在角色身上，其他层透明/虚化
- 最右侧为完整穿戴效果
- 引导线标注材质名称
- 背景纯白/浅灰

### Prompt 写法

```
character costume breakdown, [角色身份卡片], 
sequential layered presentation from left to right:
Panel 1: base layer only — [内搭描述],
Panel 2: adding [外套描述],
Panel 3: adding [下装描述],
Panel 4: adding [外层附件描述],
Panel 5: complete outfit with all accessories,
white background, technical fashion illustration style,
clean annotation lines pointing to key materials,
exactly 5 panels in a single horizontal row
```

## 变装设定（Costume Variations）

### 核心原则

不同情境下的服装设计，但**核心视觉元素**必须在所有变装中保持一致：
- 配色系统中的主色必须出现
- 标志性配饰/设计元素必须保留
- 发型和面部特征完全不变

### 常见变装情境

| 情境 | 服装类型 | 设计要点 |
|------|---------|---------|
| 日常 | 休闲装 | 放松、真实的生活感 |
| 工作/战斗 | 职业装/战斗装 | 功能性、专业感 |
| 正式/礼服 | 晚礼服/正装 | 优雅、仪式感 |
| 季节变体 | 冬装/夏装/雨衣 | 实用性、季节氛围 |
| 睡衣/居家 | 家居服 | 私密、角色性格流露 |

### 排版规范

- **横版 16:9 单图**，3-5 套变装横向排列
- 每套全身立绘，统一站姿
- 底部简短文字标注情境名称
- 背景纯色统一

## 细节/材质特写（Detail & Material Callouts）

### 必须特写的元素

- 服装花纹/刺绣/印花 → 放大至可见织物纹理
- 面料质感 → 丝绸的光泽/牛仔的纹理/皮革的纹路
- 破损/做旧痕迹 → 如有，精确展示磨损位置和程度
- 纹身/刺青 → 精确图案和位置
- 特殊工艺 → 铆钉/拉链/扣子/缝线

### 排版规范

- 中心放置角色全身图
- 四周环绕 4-6 个放大特写框
- 引导线从全身图连接到特写框
- 每个特写框标注材质名称

### Prompt 写法

对每个材质，描述：
- 物理属性：`rough texture / smooth satin / matte finish / glossy sheen`
- 颜色属性：`deep burgundy / weathered brown / iridescent blue`
- 做旧程度：`pristine / slightly worn / heavily distressed`
- 厚度/重量感：`lightweight chiffon / heavy wool / structured leather`

## 私人物品展示（Personal Belongings）

展示角色随身携带的物品，丰富角色的生活感：
- 打开的背包/手提包，旁边散落物品
- 每个物品单独可辨识
- 物品选择反映角色性格（整洁/凌乱、实用/感性）

**排版**：单张插图，物品自然散落排列，简短标注。
