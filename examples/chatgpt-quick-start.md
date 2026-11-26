# ChatGPT Quick Start

This is an optional starter for an ordinary ChatGPT conversation. It does not replace a user's more detailed production prompt.

## 中文

请使用 **Product Detail Designer v1.0.6** Skill 帮我制作电商产品详情页。

**Skill 文件（请先完整阅读）：**
https://raw.githubusercontent.com/licat233/product-detail-designer/feat/v1.0.6-page-first-continuity/SKILL.md

我会提供产品图片，以及产品说明书、规格书或其他相关资料。

请先分析我提供的产品图片和资料，然后检查以下四项制作信息：

1. **输出语言**：最终详情页图片中的文案使用什么语言？
2. **图片尺寸 / 比例**：每张图片需要什么像素尺寸或宽高比例？
3. **电商平台 / 展示位置**：例如 Amazon 商品图片、Amazon A+ Content、Shopify 产品页、Alibaba.com 详情页，或其他平台。
4. **销售地区 / 目标市场**：例如美国、欧洲、日本、东南亚、中东或全球市场。

如果我已经提供某项信息，不要重复询问。缺少多项信息时，请在一条消息中一次性问完。若平台和展示位置已知但我不知道尺寸，请先推荐合适的尺寸或比例并让我确认。若我明确授权你决定某项信息，请自行选择并简要说明采用的设定。

四项信息全部确认或由我明确授权你决定后，直接使用图像生成能力制作最终详情页图片。默认采用 8 屏，除非我另有说明。

严格区分产品事实资料与视觉设计参考：说明书、规格书、宣传册 PDF 默认只用于提取产品信息，不得照搬、临摹、换色改版或按页改编其 UI、布局、图标、表格和内容顺序。除非我明确要求复刻或改版原文件，否则必须根据产品、买家、市场和平台独立策划并设计全新的电商详情页。产品实拍图用于识别和呈现真实产品，不得擅自改变产品外观。

必须采用 **Page-first, Slice-second（先设计整页，再切分图片）** 的方法：先把整张纵向详情页作为一个完整页面设计，再按平台要求分成多个图片文件。页面是设计单位，图片只是交付切片，不能逐张设计成独立海报或 PPT。

整张页面只能有一个主标题（H1），只放在第一张图片。中间图片不得重新出现产品介绍标题、独立 Hero、总结标题或标题栏。任何图片都不得添加网站 Footer、重复 Logo、联系信息底栏或独立收尾；如果确实需要 CTA，只能在整张页面真正结束的位置出现一次。内容模块可以跨越图片切分边界，切分位置不等于内容模块的结束位置。除最后一张外，每张图片都必须延续同一页面的内容和视觉动线，不得形成独立收尾或重新开始的海报构图。根据当前图像工具的真实能力选择画布扩展、参考图延续或色调连续：只有工具明确支持画布扩展时才使用 Outpainting；普通参考图生成不能被描述为像素级无缝延续。不要为了满足机械规则而强制添加穿过底边的实体物体、固定底部留白区或人为切断重要产品结构。若我明确要求像素级连续而当前工具无法实现，请先说明限制，不要擅自降级。图片必须一张一张顺序生成，不得批量生成后续切片。

后续图片必须直接延续上一张的视觉和内容，不得重新开始一个完整版式。不要在每张图的顶部安排标题区，也不要在每张图的底部安排 Footer 区。拼接后必须像一张自然向下滚动的详情页，而不是多张 PPT。

严格保护产品真实外观和资料准确性。不要编造参数或认证，不要安装依赖，不要编写代码，也不要制作未要求的独立背景、1:3 母版、HTML 预览或其他中间文件。生成后自行检查并修复产品、文字、参数和排版问题。

如果当前会话无法读取 Skill 或不具备实际图像生成能力，请明确告诉我，不要假装已经完成。

## English

Use **Product Detail Designer v1.0.6** to create ecommerce product detail page images.

**Read the Skill first:**
https://raw.githubusercontent.com/licat233/product-detail-designer/feat/v1.0.6-page-first-continuity/SKILL.md

I will provide product photos and any available product documents, specifications, or brochures.

First review the supplied materials, then check these four production details:

1. **Output language** — the language that should appear in the final images.
2. **Image dimensions / aspect ratio** — the pixel dimensions or ratio for each image.
3. **Ecommerce platform / placement** — for example, Amazon product images, Amazon A+ Content, Shopify product-page media, Alibaba.com product detail page, or another placement.
4. **Sales region / target market** — for example, the US, Europe, Japan, Southeast Asia, the Middle East, or global.

Do not ask again for information I have already provided. If multiple items are missing, ask for all of them in one concise message. If the platform and placement are known but I do not know the image size, recommend a suitable size or ratio and ask me to confirm. If I explicitly delegate a decision, choose a sensible option and briefly state the assumption.

Once all four items are confirmed or explicitly delegated, generate the final images directly using the available image-generation capability. Use 8 image slices by default unless I specify otherwise.

Keep product evidence separate from visual design references. Product manuals, specification sheets, and brochure PDFs are factual sources by default; do not copy, trace, recolor, redesign, or adapt their page UI, layouts, icon grids, tables, or page sequence. Unless I explicitly request a faithful redesign of the source document, independently plan and design a new ecommerce detail page for the product, buyer, market, and platform. Use real product photos to preserve the product's actual appearance.

Use **Page first, slices second**: design the complete vertical ecommerce page as one page before dividing it into separate image files. The page is the design unit; each image is only a delivery slice. Never design every image as a separate poster or slide.

The complete page has **one primary title / H1 only**, placed in the first image. Intermediate images must not restart with another product-introduction title, standalone hero, summary headline, or title bar. Do not add a website footer, repeated logo, contact-information bar, or separate sign-off to any image. If a CTA is genuinely needed, place it once at the actual end of the complete page. Content modules may continue across file boundaries; a file boundary is not a content-section ending. Every image except the final one must continue the same page's content and visual flow without a standalone ending or poster-like restart. Choose canvas extension, reference continuation, or tonal continuity according to the image tool's actual capabilities. Use outpainting only when the tool explicitly supports canvas extension; ordinary reference-based generation must not be described as pixel-perfect seamless continuation. Do not force physical objects through the bottom edge, reserve a fixed blank strip, or cut through important product geometry merely to satisfy a mechanical seam rule. If I explicitly require pixel-level continuity and the available tool cannot provide it, explain the limitation before proceeding rather than silently downgrading the requirement. Generate slices one at a time in sequence; never batch-generate the remaining slices.

Every later image must directly continue the previous image's visual and content flow. Do not reserve a title area at the top or a footer area at the bottom of every image. When stacked, the result must read like one naturally scrolling ecommerce page, not a collection of PowerPoint slides.

Preserve the real product and keep all factual claims accurate. Do not invent specifications or certifications, install dependencies, write code, or create unrequested standalone backgrounds, 1:3 masters, HTML previews, or other intermediate assets. Inspect and repair product, copy, specification, and layout errors before delivery.

If the Skill cannot be read or native image generation is unavailable, say so plainly. Never pretend the work is complete.
