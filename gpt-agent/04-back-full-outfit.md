# 第4步：背面全身服装图

只用于基于当前母图生成 `image_03_back_full_outfit.png`。

## 启动条件

当前对话已有真实母图、正面头像和三分之二侧脸头像，尚无真实生成的背面全身图，并且用户发送“继续”或明确要求背面全身图。

## 一致性参考

- 必须使用当前母图作为身份、服装与比例参考，不重新生成前面三张。
- 保持同一角色、身体比例、发型背面、服装结构、颜色、材质、腰带绑带、鞋袜、手套、配饰和道具。
- 参考图没有展示明确背面结构时，根据正面结构做克制、合理且一致的背面延伸，不新增抢眼设计。

## 画面要求

- 人物背对镜头，背面全身，从头到鞋完整可见。
- 竖屏9:16，人物尽可能占满画面，头顶和鞋底仅留少量安全边距。
- 必须展示背面发型、背部服装、腰部、腿部、鞋袜与配饰结构。
- 不转身看镜头，不生成正面、侧面或正面全身图。
- 延续母图风格。默认中性灰色影棚背景；服装、头发、配饰或肤色含明显灰色系时使用白色影棚背景。
- 无文字、水印、logo、标签、编号、边框、四宫格或多视角排版。

## 当前步骤提示词

结合当前母图与用户要求，并原样包含：

```text
same character and same outfit as master front full body image, back view full body, vertical 9:16 portrait composition, standing with back facing camera, head to shoes fully visible, minimal background margins, subject fills the frame as much as possible without cropping head or shoes, same hairstyle from the back, same outfit materials and accessories, realistic live-action cinematic photo, neutral gray studio background by default; use a clean white studio background if the outfit, hair, accessories, or skin tone contains gray tones, no text, no watermark, no logo, no border
```

直接调用图像生成一次。图片真实返回后，固定四张流程完成并进入验收。
