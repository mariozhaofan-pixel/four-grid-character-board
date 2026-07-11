# 第2步：正面头像

只用于基于当前母图生成 `image_01_front_portrait.png`。

## 启动条件

当前对话已有真实生成的 `master_front_full_body.png`，并且用户按流程进入本步或明确指定正面头像。用户点名重做本图时，即使本图已经生成也重新执行。

## 一致性参考

- 必须使用当前母图作为身份与造型参考，不重新生成母图。
- 保持同一身份、年龄、脸型、五官比例、肤色、发型、发色、发饰、妆容、服装领口和肩部细节。
- 如果母图在此后被修改，本图需要基于新版母图重新生成。

## 画面要求

- 1:1方图头部特写，从头顶到肩颈或少量上胸。
- 人物正对镜头，脸、头部和肩颈占据主要画面，尽量减少背景留白。
- 不出现完整身体，不生成正面全身图。
- 延续母图风格。默认中性灰色影棚背景；服装、头发、配饰或肤色含明显灰色系时使用白色影棚背景。
- 无文字、水印、logo、标签、编号、边框、四宫格或多视角排版。

## 当前步骤提示词

结合当前母图与用户要求，并原样包含：

```text
same character as master front full body image, 1:1 square head close-up portrait, head and shoulders, facing camera, face fills the frame, minimal background margins, same face, same hairstyle, same outfit collar and shoulder details, realistic live-action cinematic photo, neutral gray studio background by default; use a clean white studio background if the outfit, hair, accessories, or skin tone contains gray tones. 面部特征：可见毛孔细纹，自然红润感，面部要有明暗变化，不要均匀受光，有光影颗粒，灰尘噪点，不要干净无层次。 no text, no watermark, no logo, no border
```

用户明确要求干净商业棚拍、无噪点、磨皮或均匀柔光时，可按其要求调整面部质感。

直接调用图像生成一次。图片真实返回后，本步骤完成；用户表达继续推进或指定三分之二侧脸头像时进入第3步。
