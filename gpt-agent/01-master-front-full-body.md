# 第1步：正面全身母图

只用于生成 `master_front_full_body.png`。

## 启动条件

- 首次收到角色参考、服装参考或文字要求。
- 当前对话中尚无真实生成的母图。
- 用户明确要求重做或修改母图、身份、脸、发型、服装、身体比例或整体风格。

## 参考图分工

- 面部或角色参考：年龄感、身份、脸型、五官、肤色、妆容、发型与气质。
- 服装或造型参考：服装类型、版型、颜色、材质、层次、鞋袜、手套、配饰、道具及正背面结构。
- 用户标注“图1角色 / 图2服装”时，图1提供身份、面部、发型和气质；图2提供服装、鞋袜、配饰及结构，并覆盖图1里的服装。
- 拼图或多视角参考只用于提取信息，不复刻其排版。
- 用户局部文字要求优先于参考图默认内容。

## 画面要求

- 全新生成的一位角色，正面站立，从头到鞋完整可见。
- 竖屏9:16，人物尽可能占满画面，头顶和鞋底仅留少量安全边距。
- 默认真实真人电影质感；用户指定风格时采用其风格。
- 默认中性灰色影棚背景；服装、头发、配饰或肤色含明显灰色系时改用白色影棚背景。
- 锁定身份、发型、服装、鞋袜、配饰、道具和身体比例，供后续三张使用。
- 无文字、水印、logo、标签、编号、边框、四宫格、model sheet、turnaround sheet或多视角排版。

## 当前步骤提示词

将用户参考信息和局部要求压缩到一个短段落，并原样包含：

```text
single character, front full body, standing, vertical 9:16 portrait composition, head to shoes fully visible, minimal background margins, subject fills the frame as much as possible without cropping head or shoes, realistic live-action cinematic photo, neutral gray studio background by default; use a clean white studio background if the outfit, hair, accessories, or skin tone contains gray tones, natural skin texture, realistic fabric and accessory details, no text, no watermark, no logo, no border
```

直接调用图像生成一次。母图真实返回后，本步骤完成；下一次“继续”进入第2步。
