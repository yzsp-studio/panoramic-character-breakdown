# Layer 5: 身体动态层规范

> **何时 read**：生成全身比例图、动作姿态集、手/脚特写时。

## 核心目标

定义身体比例、动态特征，防止角色在不同动作下"变形"。
身体是角色"形体语言"的载体。

## 全身比例图

### 头身比标注

明确标注头身比（如"7头身"/"8头身"），展示角色的身体比例基准。

**排版**：
- 角色正面全身立绘，旁边绘制等距水平线标注头身比
- 标注关键比例点：肩宽、腰线位置、臀线位置、膝盖线、脚踝线
- 比例尺标注实际设定身高（如"175cm"）

### 角色谱系比例图（多角色项目）

将所有主要角色放在同一画面中，对比身高体型：
- 所有角色脚底对齐同一基准线
- 最高和最矮角色标注身高数值
- 用虚线标注各角色肩高和头顶位置

**Prompt 写法**：
```
character height comparison chart, [所有角色名] standing side by side 
on the same baseline, heights labeled, white background, 
technical reference sheet style, exactly [N] characters
```

## 动作姿态集（Pose Sheet）

### 标志性姿态选择

根据角色类型选择最能体现其动态线条和力量感的姿态：

| 人物类型 | 推荐姿势 | 关键词 |
|---------|---------|--------|
| 西装/正装 | 站姿/叉腰/背手直立/手持文件 | powerful, authoritative |
| 运动装 | 起跑/跳跃/拉伸/运球 | dynamic, athletic |
| 休闲装 | 插兜/靠墙/坐台阶/回眸 | candid, relaxed |
| 古装/汉服 | 拱手/持扇/回眸/提裙 | elegant, ceremonial |
| 制服 | 敬礼/执行任务/操作工具 | disciplined, professional |
| 礼服 | 裙摆展示/侧身回头/持花 | graceful, refined |
| 战斗装 | 战斗待机/施法/格挡/冲锋 | fierce, combat-ready |

### 姿势 Prompt 规范

每个姿势必须描述：
1. **动作起始状态**：身体各部分的具体位置
2. **手的位置**：双手做什么、放在哪里
3. **头部朝向**：面向镜头/侧转/低头/仰视
4. **重心偏向**：左脚/右脚/均匀
5. **气质关键词**：powerful / elegant / candid / dynamic / fierce

示例：
```
Arms crossed over chest, chin slightly raised, weight shifted to right leg,
left foot forward at 30 degrees, confident authoritative stance,
gazing directly at viewer with composed expression
```

### 排版规范

| 数量 | 布局 | 整图比例 |
|------|------|---------|
| 4 个 | 2×2 | 1:1 |
| 6 个 | 2×3 | 3:2 |
| 9 个 | 3×3（推荐） | 1:1 |

- 每格全身立绘
- 纯色背景
- 统一光线

## 手部特写

### 必须展示的手势

- **基础手型**：自然放松/握拳/张开五指
- **功能手势**：握持武器/握笔/触摸/按压
- **角色特有**：结印/施法/比心/竖大拇指（根据角色设定）
- **复杂结构**：如机械义肢、利爪、异形手 → 多角度拆解

### 排版规范

- 2×3 或 3×3 网格，每格一个手势
- 手部占格面积 80%+
- 标注手指数量（防止 AI 画错）
- Negative prompt: `extra fingers, missing fingers, fused fingers, six fingers`

## 脚部特写

- 裸足结构（正面/侧面/底面）
- 穿鞋效果
- 特殊结构（如机甲靴/古代布鞋/利爪）
