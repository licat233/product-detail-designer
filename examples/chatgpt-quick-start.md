# ChatGPT Quick Start

This is an optional starter for an ordinary ChatGPT conversation. It does not replace a user's more detailed production prompt.

## 中文

请使用 **Product Detail Designer v1.0.3** Skill 帮我制作电商产品详情页。

**Skill 文件（请先完整阅读）：**
https://raw.githubusercontent.com/licat233/product-detail-designer/v1.0.3/SKILL.md

我会提供产品图片，以及产品说明书、规格书或其他相关资料。

请先分析我提供的产品图片和资料，然后检查以下四项制作信息：

1. **输出语言**：最终详情页图片中的文案使用什么语言？
2. **图片尺寸 / 比例**：每屏需要什么像素尺寸或宽高比例？
3. **电商平台 / 展示位置**：例如 Amazon 商品图片、Amazon A+ Content、Shopify 产品页、Alibaba.com 详情页，或其他平台。
4. **销售地区 / 目标市场**：例如美国、欧洲、日本、东南亚、中东或全球市场。

如果我已经提供某项信息，不要重复询问。缺少多项信息时，请在一条消息中一次性问完。若平台和展示位置已知但我不知道尺寸，请先推荐合适的尺寸或比例并让我确认。若我明确授权你决定某项信息，请自行选择并简要说明采用的设定。

四项信息全部确认或由我明确授权你决定后，直接使用图像生成能力制作最终详情页图片。默认采用 8 屏，除非我另有说明。

严格区分产品事实资料与视觉设计参考：说明书、规格书、宣传册 PDF 默认只用于提取产品信息，不得照搬、临摹、换色改版或按页改编其 UI、布局、图标、表格和内容顺序。除非我明确要求复刻或改版原文件，否则必须根据产品、买家、市场和平台独立策划并设计全新的电商详情页。产品实拍图用于识别和呈现真实产品，不得擅自改变产品外观。

默认把全部图片设计成**一张连续纵向详情页的相邻切片**，不是多张独立海报或 PPT。图片上下边缘必须自然衔接，背景、光线、空间和视觉动线要连续；不要添加页眉、页脚、页码、01–08 序号、重复 Logo / 标题栏、装饰性边角、整屏边框或 PPT 式页面框架。文件编号只用于内部管理，不得出现在买家可见画面中。每屏可以有不同内容和构图，但不能像一张独立幻灯片。

严格保护产品真实外观和资料准确性。不要编造参数或认证，不要安装依赖，不要编写代码，也不要制作未要求的独立背景、1:3 母版、HTML 预览或其他中间文件。生成后自行检查并修复产品、文字、参数和排版问题。

如果当前会话无法读取 Skill 或不具备实际图像生成能力，请明确告诉我，不要假装已经完成。

## English

Use **Product Detail Designer v1.0.3** to create ecommerce product detail page images.

**Read the Skill first:**
https://raw.githubusercontent.com/licat233/product-detail-designer/v1.0.3/SKILL.md

I will provide product photos and any available product documents, specifications, or brochures.

First review the supplied materials, then check these four production details:

1. **Output language** — the language that should appear in the final images.
2. **Image dimensions / aspect ratio** — the pixel dimensions or ratio for each screen.
3. **Ecommerce platform / placement** — for example, Amazon product images, Amazon A+ Content, Shopify product-page media, Alibaba.com product detail page, or another placement.
4. **Sales region / target market** — for example, the US, Europe, Japan, Southeast Asia, the Middle East, or global.

Do not ask again for information I have already provided. If multiple items are missing, ask for all of them in one concise message. If the platform and placement are known but I do not know the image size, recommend a suitable size or ratio and ask me to confirm. If I explicitly delegate a decision, choose a sensible option and briefly state the assumption.

Once all four items are confirmed or explicitly delegated, generate the final images directly using the available image-generation capability. Use 8 screens by default unless I specify otherwise.

Keep product evidence separate from visual design references. Product manuals, specification sheets, and brochure PDFs are factual sources by default; do not copy, trace, recolor, redesign, or adapt their page UI, layouts, icon grids, tables, or page sequence. Unless I explicitly request a faithful redesign of the source document, independently plan and design a new ecommerce detail page for the product, buyer, market, and platform. Use real product photos to preserve the product's actual appearance.

Design all images as **adjacent slices of one continuous vertical ecommerce page**, not as independent posters or PowerPoint slides. The top and bottom edges must connect naturally, with consistent background, lighting, spatial depth, and visual flow. Do not add headers, footers, page numbers, 01–08 labels, repeated logo/title bars, decorative corners, full-image borders, or slide-like page frames. File numbering is internal only and must never appear in buyer-visible artwork. Each slice may have distinct content and composition, but must not look like a standalone slide.

Preserve the real product and keep all factual claims accurate. Do not invent specifications or certifications, install dependencies, write code, or create unrequested standalone backgrounds, 1:3 masters, HTML previews, or other intermediate assets. Inspect and repair product, copy, specification, and layout errors before delivery.

If the Skill cannot be read or native image generation is unavailable, say so plainly. Never pretend the work is complete.
