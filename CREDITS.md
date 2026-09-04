# 来源与致谢

本仓库不盈利、纯开源。下面列出每一处借用或参考：来源、许可、用在哪里、借用方式（逐字复制 / 改写 / 只参考思路）。
没有列出的部分为本仓库自行实现。

## 代码与算法

| 内容 | 来源 | 许可 | 用在哪里 | 方式 |
|---|---|---|---|---|
| 落雨 / 落雪的起点（雨丝、雪片、卡片顶高度场积雪） | 朋友原作《落雨与积水》《落雪与积雪》 | 经作者同意（署名待补） | 三个版本的 rain / snow | 改写：雪片、水珠、融化全部重做，高度场沉积核保留 |
| 玻璃上水珠的物理：随机落点、长大、动量 + 摩擦的蠕滑、拖尾子滴、滑过吞并（面积守恒） | RainEffect，Lucas Bebber for Codrops，https://github.com/codrops/RainEffect | MIT（见 https://tympanus.net/codrops/licensing/） | `GlassDrop` | 参考思路改写，未复制代码 |
| 雨滴折射画法（倒像切片、暗边显形）的参考 | raindrop-fx，SardineFish，https://github.com/SardineFish/raindrop-fx | MIT | `paintDrop` | 只参考效果，未复制代码 |
| 三棱镜色散、Snell 折射的参考 | explerify / physandbox / kamilprusko-prism 一类光学模拟器 | 各自许可 | 早期棱镜面板 | 只参考做法，未复制代码 |
| 云 sprite 的方向：多层软云各自速度漂移、闪电照亮整个场景 | iOS 天气 app 的视觉 | — | 云层、白闪 | 只参考视觉，无代码 |

## 知识来源

| 内容 | 来源 |
|---|---|
| 冰雹的洋葱层结构（清冰壳 + 乳白核） | NOAA / EPOD 对冰雹剖面的描述 |
| 彩虹的形成条件、亮度分布、Alexander 暗带、supernumerary、副虹色序反转 | RMetS、NWS 的科普材料 |

## 照片（版本 A 内置背景）

按 Unsplash License 通过 Unsplash CDN 热链接使用，不随仓库分发：

- https://unsplash.com/photos/1470770841072-f978cf4d019e
- https://unsplash.com/photos/1477959858617-67f85cf4f1df
- https://unsplash.com/photos/1439066615861-d1af74d74000
- https://unsplash.com/photos/1506744038136-46273834b3fb

## 审过但没有采用的开源实现

为了找可以直接抄的东西，审过 40 余个开源天气 / 玻璃效果实现（许可逐一核过）。值得记一笔、但最终没有采用的：

- 「2D Clouds」（drift，Shadertoy 4tdSWr）：作者在评论区明确授权任意使用；是 GLSL 方案，本仓库的云用 canvas 2D 自行实现了同类 fbm 做法。
- liquid-glass（Shu Ding，MIT）：SVG 位移贴图的玻璃折射，只在 Chromium 生效，iOS Safari 不支持，故未用于卡片。
- three.js `LightningStrike`（MIT，r152 及以前）：3D 分形闪电，对单文件 canvas 2D 页面过重。
- 「Falling Snow with Accumulation」（Simon，CodePen，MIT）：高度场积雪与融化循环，与朋友原作的做法同源，未复制。
