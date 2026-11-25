# Product Detail Designer

**A lightweight, image-first AI skill for creating ecommerce product detail pages.**

Latest release: [v1.0.2](https://github.com/licat233/product-detail-designer/releases/tag/v1.0.2)

[简体中文](#简体中文) · [English](#english)

## 简体中文

Product Detail Designer 是一个面向整个电商行业的通用 AI Skill。它帮助 AI 根据产品图片、产品资料和风格参考，直接制作具有商业展示质量的电商产品详情页图片。

它不属于任何特定品牌或公司，也不绑定某个产品类别、设计软件或技术栈。

### 设计目标

- **直接生成成品：** 默认从用户提供的产品图片和制作要求出发，直接生成最终详情页图片。
- **Chat-first：** 优先适配 ChatGPT 普通 Chat 会话等对话式 AI 环境。
- **先确认制作需求：** 正式生成前确认输出语言、图片尺寸 / 比例、电商平台 / 展示位置和销售地区；缺失信息一次问完。
- **零依赖：** 不要求安装 Python、Node.js、第三方包、脚本、API 或本地渲染环境。
- **产品真实：** 优先保留真实产品的结构、颜色、材质、标识和关键部件。
- **信息可信：** 不编造参数、认证、测试结果、销量、评价或其他商业声明。
- **资料与设计分离：** PDF、宣传册和规格书默认只用于提取产品事实，不照搬或改编其页面 UI；最终详情页必须独立策划和设计。
- **视觉统一：** 整套图片保持统一的设计语言，同时避免每屏重复同一种构图。
- **少做无用中间件：** 不默认制作独立背景、1:3 母版、Moodboard、HTML 预览或 Contact Sheet。

### 在 ChatGPT 普通会话中使用

ChatGPT 普通 Chat 会话不会因为 GitHub 仓库公开就自动安装 Skill。使用时：

1. 将 [SKILL.md](SKILL.md) 作为附件提供给 ChatGPT，或发送 [v1.0.1 固定版本原始文件](https://raw.githubusercontent.com/licat233/product-detail-designer/v1.0.2/SKILL.md)。
2. 附上产品图片，以及已有的说明书、参数表或宣传册（如有）。
3. 发送你的产品详情页制作提示词。
4. ChatGPT 会先检查输出语言、图片尺寸 / 比例、电商平台 / 展示位置和销售地区；缺失的信息会在一条消息中集中确认。
5. 确认或授权 AI 决定后，如果当前会话支持图像生成，Skill 会指导 ChatGPT 直接制作最终图片；无需安装本仓库的任何依赖。

PDF、宣传册和规格书用于理解产品与核实信息，不是默认的视觉模板。除非你明确要求复刻或改版原文件，AI 必须独立设计电商详情页，不能把 PDF 页面换色、换字体后当作最终作品。

你可以继续使用自己已经习惯的详细制作提示词。Skill 负责图像生成与质量控制，不应擅自改写用户的制作要求或额外增加审批环节。

### 适用范围

消费品、电子产品、家居用品、服装、工业品、零部件、美妆、食品、户外用品，以及其他需要电商详情页视觉内容的产品。

### 仓库内容

- `SKILL.md`：完整 Skill 定义。
- `examples/chatgpt-quick-start.md`：普通 Chat 会话的简短启动示例。
- `CHANGELOG.md`：版本记录。
- `LICENSE`：MIT License。

### 原则

复杂的设计工作由 AI 在内部完成；用户只需要提供产品、资料和目标。不要把内部工作流变成用户的额外负担。

## English

Product Detail Designer is a general-purpose AI skill for creating commercial-quality ecommerce product detail images from product photos, product information, and visual references.

It is brand-neutral and category-neutral. It does not depend on a particular company, product type, design application, or technology stack.

### Design goals

- **Generate finished images directly.** Start from the user's product images and brief, then create the requested final visuals.
- **Chat-first.** Prioritize ordinary ChatGPT conversations and other conversational AI environments.
- **Confirm the production brief.** Before final generation, confirm output language, image dimensions/aspect ratio, ecommerce platform/placement, and sales region. Ask for all missing items together.
- **No setup dependencies.** No Python, Node.js, packages, scripts, API keys, or local rendering pipeline are required.
- **Protect product identity.** Preserve the real product's structure, color, material, branding, and distinctive components.
- **Keep claims accurate.** Never invent specifications, certifications, test results, sales figures, reviews, or commercial promises.
- **Keep the set coherent.** Maintain a shared visual language while varying each screen's composition and information structure.
- **Avoid unnecessary intermediates.** Separate backgrounds, 1:3 masters, moodboards, HTML reviews, and contact sheets are not default deliverables.

### Use in an ordinary ChatGPT conversation

A public GitHub repository is not automatically installed into an ordinary ChatGPT chat. To use this skill:

1. Attach [SKILL.md](SKILL.md) to the conversation or provide the [v1.0.1 pinned raw file](https://raw.githubusercontent.com/licat233/product-detail-designer/v1.0.2/SKILL.md).
2. Attach the product images and any available product documents.
3. Send your own product-detail-page prompt.
4. The assistant checks the output language, image dimensions/aspect ratio, ecommerce platform/placement, and sales region, asking for all missing details in one concise message.
5. After confirmation or explicit delegation, if native image generation is available, the skill guides the assistant to create the final images directly. No repository dependencies need to be installed.

Keep using your own established production prompt. The skill governs image-generation behavior and quality control; it should not rewrite the user's brief or add unrequested approval stages.

### Supported product categories

Consumer goods, electronics, home and living, apparel, industrial products, components, beauty, food, outdoor products, and other ecommerce categories.

### Repository contents

- `SKILL.md`: the complete skill definition.
- `examples/chatgpt-quick-start.md`: a short starter for ordinary chat sessions.
- `CHANGELOG.md`: release history.
- `LICENSE`: MIT License.

### Principle

The AI handles the complex design work internally. The user supplies the product, source material, and goal—not a pile of extra workflow tasks.

## License

MIT. See [LICENSE](LICENSE).
