<h1 align="center">心念贴纸 ImageGen Skill</h1>

<p align="center"><code>heart-sticker-imagegen-skill</code></p>

<p align="center"><em>「传一张图，先选风格，再把熟悉的人变成独一份贴纸。」</em></p>

<p align="center">
  <img alt="Codex Skill" src="https://img.shields.io/badge/Codex-Skill-bc694a">
  <img alt="Image styles" src="https://img.shields.io/badge/image_styles-11-d4a085">
  <img alt="Text styles" src="https://img.shields.io/badge/text_styles-9-a55a42">
  <img alt="Examples" src="https://img.shields.io/badge/examples-31-6b7280">
</p>

<p align="center">
  Codex · Built-in <code>image_gen</code> · <a href="https://github.com/mundane799699/heart-sticker">Prompt source</a>
</p>

这是一个给 Codex 使用的贴纸生成 Skill。你上传照片，或给出一句必须逐字呈现的文字；它先挑出几种真正合适的风格，等你确认，再调用内置 `image_gen` 完成生成。

它复用了 Heart Sticker 的 11 套图片提示词和 9 套文字提示词，并补上了主体一致性、文字复核、背景处理和错误约束。不是把整套提示词一次塞给模型。是先判断任务，再选择，再生成。

原始网站说“传图片、选风格、生成、打印、邮寄”。这个 Skill 把其中最有价值的创作链路带进 Codex：**给素材 → 选风格 → 确认 → 出图**。

## 真人案例

同一位人物，保留黑色长发、轻薄刘海、彩色星星发夹和面部特征，同时允许动作、道具与场景随风格变化。原始参考照片没有提交到仓库。

<table>
  <tr>
    <td align="center"><img src="heart-sticker-imagegen/assets/examples/real-person/cartoon-sticker.png" width="220"><br><sub>卡通贴纸</sub></td>
    <td align="center"><img src="heart-sticker-imagegen/assets/examples/real-person/vintage-comic.png" width="220"><br><sub>复古漫画</sub></td>
    <td align="center"><img src="heart-sticker-imagegen/assets/examples/real-person/kawaii.png" width="220"><br><sub>可爱贴纸</sub></td>
    <td align="center"><img src="heart-sticker-imagegen/assets/examples/real-person/neon-future.png" width="220"><br><sub>霓虹未来</sub></td>
  </tr>
  <tr>
    <td align="center"><img src="heart-sticker-imagegen/assets/examples/real-person/pixar-3d.png" width="220"><br><sub>3D 动画</sub></td>
    <td align="center"><img src="heart-sticker-imagegen/assets/examples/real-person/ghibli.png" width="220"><br><sub>手绘动画</sub></td>
    <td align="center"><img src="heart-sticker-imagegen/assets/examples/real-person/pixel-art.png" width="220"><br><sub>像素艺术</sub></td>
    <td align="center"><img src="heart-sticker-imagegen/assets/examples/real-person/clay-style.png" width="220"><br><sub>粘土风</sub></td>
  </tr>
  <tr>
    <td align="center"><img src="heart-sticker-imagegen/assets/examples/real-person/figure.png" width="220"><br><sub>插画</sub></td>
    <td align="center"><img src="heart-sticker-imagegen/assets/examples/real-person/graffiti.png" width="220"><br><sub>涂鸦</sub></td>
    <td align="center"><img src="heart-sticker-imagegen/assets/examples/real-person/minimal-line.png" width="220"><br><sub>儿童绘画</sub></td>
    <td></td>
  </tr>
</table>

<details>
<summary><strong>展开卡通人物的 11 种风格</strong></summary>
<br>
<table>
  <tr>
    <td align="center"><img src="heart-sticker-imagegen/assets/examples/cartoon-person/cartoon-sticker.png" width="220"><br><sub>卡通贴纸</sub></td>
    <td align="center"><img src="heart-sticker-imagegen/assets/examples/cartoon-person/vintage-comic.png" width="220"><br><sub>复古漫画</sub></td>
    <td align="center"><img src="heart-sticker-imagegen/assets/examples/cartoon-person/kawaii.png" width="220"><br><sub>可爱贴纸</sub></td>
    <td align="center"><img src="heart-sticker-imagegen/assets/examples/cartoon-person/neon-future.png" width="220"><br><sub>霓虹未来</sub></td>
  </tr>
  <tr>
    <td align="center"><img src="heart-sticker-imagegen/assets/examples/cartoon-person/pixar-3d.png" width="220"><br><sub>3D 动画</sub></td>
    <td align="center"><img src="heart-sticker-imagegen/assets/examples/cartoon-person/ghibli.png" width="220"><br><sub>手绘动画</sub></td>
    <td align="center"><img src="heart-sticker-imagegen/assets/examples/cartoon-person/pixel-art.png" width="220"><br><sub>像素艺术</sub></td>
    <td align="center"><img src="heart-sticker-imagegen/assets/examples/cartoon-person/clay-style.png" width="220"><br><sub>粘土风</sub></td>
  </tr>
  <tr>
    <td align="center"><img src="heart-sticker-imagegen/assets/examples/cartoon-person/figure.png" width="220"><br><sub>插画</sub></td>
    <td align="center"><img src="heart-sticker-imagegen/assets/examples/cartoon-person/graffiti.png" width="220"><br><sub>涂鸦</sub></td>
    <td align="center"><img src="heart-sticker-imagegen/assets/examples/cartoon-person/minimal-line.png" width="220"><br><sub>儿童绘画</sub></td>
    <td></td>
  </tr>
</table>
</details>

<details>
<summary><strong>展开“空格的键盘”的 9 种文字风格</strong></summary>
<br>
<table>
  <tr>
    <td align="center"><img src="heart-sticker-imagegen/assets/examples/text/trendy.png" width="220"><br><sub>潮流活力</sub></td>
    <td align="center"><img src="heart-sticker-imagegen/assets/examples/text/calligraphy.png" width="220"><br><sub>经典书法</sub></td>
    <td align="center"><img src="heart-sticker-imagegen/assets/examples/text/poster.png" width="220"><br><sub>文字海报</sub></td>
  </tr>
  <tr>
    <td align="center"><img src="heart-sticker-imagegen/assets/examples/text/golden.png" width="220"><br><sub>黑金雕刻</sub></td>
    <td align="center"><img src="heart-sticker-imagegen/assets/examples/text/childlike.png" width="220"><br><sub>童心随性</sub></td>
    <td align="center"><img src="heart-sticker-imagegen/assets/examples/text/graffiti-art.png" width="220"><br><sub>艺术涂鸦</sub></td>
  </tr>
  <tr>
    <td align="center"><img src="heart-sticker-imagegen/assets/examples/text/cute-comic.png" width="220"><br><sub>可爱漫画</sub></td>
    <td align="center"><img src="heart-sticker-imagegen/assets/examples/text/trendy-creative.png" width="220"><br><sub>潮流创意</sub></td>
    <td align="center"><img src="heart-sticker-imagegen/assets/examples/text/emoji-text.png" width="220"><br><sub>表情包文字</sub></td>
  </tr>
</table>
</details>

## 快速开始

使用 Skills CLI 安装：

```bash
npx skills add SpaceZephyr/heart-sticker-imagegen-skill
```

或手动复制：

```bash
git clone https://github.com/SpaceZephyr/heart-sticker-imagegen-skill.git
cp -R heart-sticker-imagegen-skill/heart-sticker-imagegen ~/.codex/skills/
```

安装后需要重新打开 Codex 任务，让 Skill 被重新发现。

## 怎么用

图片贴纸：

```text
使用 $heart-sticker-imagegen，把我上传的人像做成贴纸。先给我 5 个合适的风格，等我确认后再生成。
```

文字贴纸：

```text
使用 $heart-sticker-imagegen，制作文字“空格的键盘”。先给我文字风格选择，确认后再生成。
```

如果想一次比较全部效果，可以直接说：

```text
保留人物特质，动作和道具可以变化，输出全部图片风格。
```

## 四步完成

1. **给素材**：上传人物、宠物或物品图片；文字任务则给出必须逐字呈现的内容。
2. **选风格**：Skill 根据主体和用途推荐 3–5 个选择。
3. **做确认**：你选定风格后，Skill 才会开始生成。
4. **拿成品**：调用 Codex 内置 `image_gen`，展示结果并检查人物与文字准确性。

## 它能做什么

- 11 种图片贴纸风格：卡通、复古漫画、可爱、霓虹未来、3D 动画、手绘动画、像素、粘土、插画、涂鸦、儿童绘画。
- 9 种文字贴纸风格：潮流活力、经典书法、文字海报、黑金雕刻、童心随性、艺术涂鸦、可爱漫画、潮流创意、表情包文字。
- 保留人物可见特质，也允许按需求替换动作、道具和场景。
- 支持自定义风格与去除背景，不依赖 Heart Sticker 原站账号、积分或密钥。

## 仓库结构

```text
heart-sticker-imagegen-skill/
├── README.md
└── heart-sticker-imagegen/
    ├── SKILL.md
    ├── agents/openai.yaml
    ├── references/
    │   ├── image-styles.md
    │   ├── text-styles.md
    │   ├── case-gallery.md
    │   └── source-manifest.md
    └── assets/examples/
        ├── real-person/
        ├── cartoon-person/
        └── text/
```

## 诚实边界

- 这不是独立图片模型；运行时必须能调用 Codex 内置 `image_gen`。
- 中文文字生成仍可能出现错字、漏字或字序错误，Skill 会要求复核，但不能保证第一次完全正确。
- 风格转换会保留人物的核心可见特征，不保证像素级复刻原图。
- 真人案例只包含生成结果，不包含用户上传的原始照片；使用他人肖像前，请先取得授权。

## 许可证与来源

本仓库暂未声明独立开源许可证。20 套基础提示词整理自 [mundane799699/heart-sticker](https://github.com/mundane799699/heart-sticker)，提取提交与文件位置记录在 [source-manifest.md](heart-sticker-imagegen/references/source-manifest.md)。上游 README 标注“保留所有权利”，再分发或商用前请自行确认授权边界。

Skill 的工作流编排与案例由 Codex 整理生成。本项目不是 Heart Sticker 官方项目，也不调用其线上接口。README 的短标题、案例墙和四步流程参考了原落地页的表达方式，但没有复制其品牌资产。
