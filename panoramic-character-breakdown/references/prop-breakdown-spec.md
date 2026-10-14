# Layer 6: 装备道具层规范

> **何时 read**：生成装备/道具分解图、私人物品展示时。

## 核心目标

对角色的核心装备进行不同角度的展示和拆解，
明确其功能结构、材质、尺寸及与角色的比例关系。

## 装备/道具分解图（Prop Breakdown）

### 道具形态分析

使用参考图分析道具的长宽厚比例与主要展开方向，按下表选择排版：

| 道具形态 | 推荐排版 | 整图比例 |
|----------|---------|---------|
| **横向扁平型**（宽>>高，如箱体/长枪/车辆） | N行×1列 竖排 | 1:1 或 3:4 |
| **纵向细长型**（高>>宽，如剑/权杖/立柱） | 1行×N列 横排 | 16:9 |
| **接近等比型**（宽≈高，如头盔/球体/方盒） | 1×3 横排或 2×2 网格 | 16:9 或 1:1 |
| **复杂异形**（多方向伸展，如带翅膀/支架） | 1×3 横排或 2×2 网格 | 16:9 或 1:1 |

### 视角定义（摄影机位环绕）

采用**摄影机位环绕拍摄**效果（非工程正交投影）。
每个面板像摄影师在该位置实际拍摄：有自然透视、真实光影和地面柔和阴影。

**三视图机位**：
| 面板 | 机位 | 描述 |
|------|------|------|
| 1 | 前方 3/4 | 前方偏侧，略俯视约30°，同时看到顶部+正面+一个侧面 |
| 2 | 正侧面 | 正侧面，平视或微俯视，完整侧面轮廓 |
| 3 | 后方 3/4 | 后方偏侧，略俯视，顶部+背面+另一个侧面 |

**四视图机位**：三视图 + 面板4（对侧面，与面板2相对的另一个侧面）

### 一致性强约束

- **参考图是唯一视觉真理**：prompt 中强调以参考图为绝对锚点
- **逐部件精确描述**：逐一列出每个部件的形状/材质/颜色/位置/数量
- **一致性增强词必须写入**：
  ```
  same product shape as reference image, identical silhouette, 
  exact color reproduction, same material texture, identical surface finish, 
  no design modifications, identical product details across all views
  ```
- **Negative prompt 精准取反**：把道具的关键特征取反写入，防止模型自由发挥

### 面板数量强约束

模型对复杂道具容易自行增加面板数量。必须多重锁定：
1. `exactly N panels, each panel contains exactly ONE instance of the prop`
2. `NOT more than N, NOT N+1, NOT N+2, NOT N+3`
3. `If you generate more than N instances the entire image is WRONG`
4. Negative: `more than N items, extra panels, duplicate views, extra rows`

### 侧面提示词规范

- 面板 2：`Side view, the camera is positioned at one side of the prop`
- 面板 4：`The camera orbits to the opposite side from panel 2, showing the other side`
- **禁止** left / right / mirror / 镜像

## 尺寸比例展示

道具与角色并置，展示比例关系：
- 角色手持/佩戴道具的全身图
- 道具旁放置参照物（如手/硬币/尺规）
- 标注关键尺寸

## 功能展示

展示道具的不同状态（如适用）：
- 收纳态 vs 展开态
- 充能态 vs 释放态
- 正常态 vs 损坏态

## 材质特写

每种材质单独特写：
- 金属：反光度/锈蚀/刻痕
- 木材：纹路/漆面/磨损
- 织物：编织方式/褪色/破损
- 宝石/水晶：透明度/折射/嵌入方式

## 私人物品展示

展示角色随身携带的日常物品，丰富角色的生活感：
- 背包/手提包内容散落展示
- 桌面/工作台物品摆放
- 每个物品可辨识，反映角色性格

**排版**：单张插图，物品自然散落排列，标注名称。
