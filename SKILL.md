---
name: product-detail-designer
description: Create commercial-quality ecommerce product detail page images from product photos, product documents, and visual references. Use when a user asks to create, design, generate, or improve product listing images, ecommerce detail pages, product feature panels, or long-form product page visuals.
license: MIT
version: 1.0.3
---

# Product Detail Designer

A brand-neutral, chat-first skill for creating ecommerce product detail page images across industries and product categories.

## Core contract

1. **The user's prompt is the production brief.** Follow its requested page count, language, ratio, style, approval gates, and deliverables. Do not rewrite the brief or add workflow stages.
2. **Default to making the images.** When the user supplies product images and asks for finished detail-page images, analyze the inputs internally and proceed to image generation. Do not stop at advice, a long blueprint, or a design discussion unless the user asks for planning or their prompt explicitly requires approval.
3. **Confirm the production brief before final generation.** After reviewing the supplied product material, make sure the output language, image dimensions or aspect ratio, target ecommerce platform and placement, and sales market are known or explicitly delegated by the user. Ask once for all missing items before generating final images.
4. **Use the host's native image-generation capability.** In ChatGPT, use the available image-generation tool. Do not simulate image generation with code or placeholder files.
5. **No setup burden.** Do not require local installation, Python, Node.js, packages, API keys, external services, scripts, HTML editors, or a separate rendering pipeline.
6. **No unrequested intermediate deliverables.** Do not create standalone backgrounds, moodboards, contact sheets, wireframes, HTML reviews, visual-master images, or 1:3 canvases unless the user or their prompt explicitly asks for them.
7. **Be honest about capability.** If native image generation is unavailable or fails, explain the limitation plainly. Never claim an image was generated when it was not.

## Operating modes

Choose the mode from the user's actual request; do not force every task through the same ceremony.

### Direct production (default)

Use when the user asks for finished images, supplies product images, or gives a production prompt.

- Review the supplied images and documents.
- Make the necessary product, copy, layout, and visual decisions internally.
- Generate the requested final images directly.
- Inspect the results and repair only the affected images.
- Deliver the images without an unsolicited planning report.

### Approval-led production

Use only when the user explicitly requests a blueprint, review, or approval gate, or when their supplied prompt defines one.

- Present the requested planning artifact at the requested level of detail.
- Stop only at the approval gate specified by the user.
- After approval, continue with the next requested stage.
- Do not invent additional approvals, trials, or sign-off stages.

An explicit request to generate directly takes precedence over the default planning habits of other workflows.

## Input analysis

Use the material the user actually supplies:

- Product photographs, pack shots, detail photographs, installation images, and application scenes.
- Product brochures, specifications, manuals, packaging details, and existing product-page copy.
- Style references, competitor examples, and brand guidelines.

Internally distinguish:

- **Confirmed:** explicitly supplied or supported by authoritative product material.
- **Observed:** directly visible in the supplied images.
- **Inferred:** a reasonable interpretation of the product category or visible design.
- **Unknown:** unsupported, conflicting, or not visible.

Do not turn an inference into a confirmed technical or commercial claim. If sources conflict on a material fact, ask one concise question or omit the disputed claim.

## Source-material roles and visual independence

**Content reference is not visual reference.** A file supplied to explain the product does not automatically become a design template.

Classify supplied materials by their intended role before creating the page:

- **Product evidence:** brochures, catalogs, datasheets, specification sheets, manuals, certificates, existing product-page copy, and technical documents. Use these to verify product facts, specifications, features, functions, supported applications, limitations, and approved claims.
- **Product visual assets:** product photographs, pack shots, close-ups, installation photographs, and genuine application photographs. Use these to understand and depict the real product. If a useful product photo is embedded in a PDF, extract or reference the individual image only when it can be used clearly and accurately.
- **Technical drawings and diagrams:** use these to understand construction, dimensions, wiring, operation, and relationships between components. Create a new, legible explanation only when useful; preserve the engineering meaning and never invent missing geometry or values.
- **Visual-design references:** moodboards, brand guidelines, sample ecommerce pages, or other files the user explicitly identifies as visual/style references. Follow only the aspects the user asks you to reference.

### Default rule for PDFs and product documents

Unless the user explicitly asks to reproduce, redesign, convert, or follow the visual design of a supplied document, treat every PDF page as a **content/evidence source only**, not as a visual template.

Do not:

- Recreate, trace, imitate, modernize, recolor, translate, or rearrange the PDF's page layout as the ecommerce detail page.
- Copy its page-by-page sequence, composition, title placement, text blocks, tables, icon grids, decorative elements, backgrounds, or information hierarchy.
- Feed a complete PDF page or a screenshot of that page to image generation as a design reference by default.
- Turn each PDF page into a corresponding ecommerce screen, or produce a set that looks like the original brochure with new colors and fonts.

You may extract and reorganize verified facts, approved wording, individual product images, and useful technical information from the document. Rewrite and structure that material for the buyer journey and the confirmed ecommerce platform. The final page must be an independently conceived ecommerce design, not a visual adaptation of the source document.

If the only product visual is embedded in a PDF, use an individual extracted product image only if its resolution and quality are sufficient. Do not substitute an entire brochure page for a missing product photograph. If the real product cannot be seen clearly enough, ask for a proper product image or explain the limitation.

### Required content-to-design separation check

Before generation, be able to state internally:

1. Which supplied sources establish product facts?
2. Which individual assets establish the product's real appearance?
3. Which files, if any, were explicitly designated as visual-design references?
4. What new ecommerce narrative and visual system will be created for this product and placement?

If no style reference was explicitly designated, create the visual system independently from the product category, buyer, market, brand requirements, and platform placement. Do not infer a request to copy a PDF's style merely because the PDF is polished or visually attractive.

**Exception:** if the user explicitly requests a faithful PDF/brochure redesign or explicitly designates a document as the layout/style template, follow that instruction within the stated scope. Do not silently apply this exception to ordinary product-detail-page production.

## Production brief confirmation

This is a required production checkpoint, not a visual-design approval gate. Complete it after reviewing the supplied product material and before generating final images.

### Four required items

Confirm each item unless the user has already stated it clearly in the current conversation or explicitly delegated the decision:

1. **Output language** — the language that should appear in the finished images. Do not infer it from the language used in chat, the language of a brochure, or the user's location.
2. **Image dimensions or aspect ratio** — the intended size for each final image, expressed as width × height in pixels and/or an aspect ratio. Confirm orientation when it is not obvious.
3. **Target ecommerce platform and placement** — for example, Amazon main/secondary product images, Amazon A+ Content, Shopify product-page media, Alibaba.com product detail page, eBay listing images, or a generic independent-store product page. A platform name alone may be insufficient when its placements have different formats.
4. **Sales region / target market** — the intended country or region, such as the United States, EU/Europe, Japan, Southeast Asia, Middle East, or global. Do not infer the sales market from the user's current location.

### How to ask

- Inspect the available product photos and documents first, so any size recommendation can be informed by the product and intended use.
- Check the conversation and supplied brief for answers already given. Never ask again for a confirmed item.
- If two or more items are missing, ask for all missing items in **one concise message**. Do not split the questions across multiple turns.
- Use ordinary conversational questions or a compact numbered list; do not create a long questionnaire.
- For image size: if the platform and placement are known but the user does not know the size, recommend a suitable working size or aspect ratio and ask the user to confirm it. If the platform or placement is unknown, ask for it before recommending platform-specific dimensions.
- Distinguish a verified platform requirement from a design recommendation. Do not invent current platform image limits. If claiming a current official requirement, verify it from the platform's official documentation when browsing is available; otherwise label the size as a recommendation, not an official rule.
- The user may answer with exact values, accept your recommendation, or explicitly say that you may decide. Treat delegation as applying only to the item(s) they delegated.

### Delegated decisions and defaults

- Do not silently choose a missing required item just to avoid asking.
- If the user explicitly says “you decide,” “use your recommendation,” or equivalent for a missing item, choose a sensible option and briefly state the assumption before production.
- If language is delegated, choose based on the explicitly stated audience/market; if that still does not determine it, use the conversation language and state that assumption. An overseas-market request alone does not automatically mean English.
- If platform/placement is delegated, use a neutral ecommerce product-page format unless the user has described a specific sales channel.
- If sales market is delegated, use a broadly international presentation and avoid market-specific legal, regulatory, or certification claims that are not supported by the supplied material.
- If dimensions are delegated, choose a practical size and aspect ratio appropriate to the confirmed placement. Do not present your choice as an official platform requirement unless verified.

### Proceeding to production

Begin final image generation only when all four items are either confirmed or explicitly delegated. Then proceed directly with the user's requested workflow. This checkpoint does not authorize extra blueprints, moodboards, visual masters, or approval gates that the user did not request.

## Product identity protection

Treat the real product as the subject, not as inspiration for a similar-looking invention.

Preserve the characteristics that define its identity:

- Shape, proportions, dimensions that are visually evident, and component relationships.
- Color, finish, texture, material appearance, and distinctive construction.
- Logo, labels, packaging, ports, buttons, fasteners, connectors, and accessories.
- Number of products and parts, and the way parts are assembled or positioned.

Use the supplied product image as the primary visual reference whenever possible. Let image generation create the scene, lighting, supporting props, and composition around the product; do not casually redesign the product itself.

If the model cannot reliably preserve a critical product feature, do not present the altered result as accurate. Repair it, choose a safer composition, or explain the limitation.

## Claims and copy accuracy

Never invent or imply unsupported:

- Technical specifications, materials, compatibility, performance, test results, or service life.
- Certifications, patents, awards, endorsements, customer logos, or partnerships.
- Sales figures, ratings, reviews, conversion rates, discounts, warranties, delivery promises, or stock status.
- Medical, safety, environmental, or regulatory claims.

Use exact user-provided wording for model numbers, measurements, units, ratings, certification names, warnings, and other critical data. Do not silently normalize or “correct” a value.

When copy is not supplied, write concise, specific, buyer-oriented copy based on confirmed facts and clearly supportable observations. Avoid generic superlatives and exaggerated advertising language.

## Visual design

Create a coherent commercial design system that serves the product and the intended market.

Consider:

- Product category, audience, purchase context, and buyer questions.
- Palette, contrast, lighting, materials, typography, spacing, image treatment, and visual hierarchy.
- A useful mix of product hero views, close-ups, feature explanations, diagrams, comparisons, use cases, installation steps, and specifications where relevant.
- Clear reading order and enough negative space for legibility.
- A distinct purpose and composition for each page or screen.

Keep the set visually related without making every image look identical. Vary camera angle, crop, product scale, layout, and information density while retaining a recognizable visual language.

### Continuous long-page composition (mandatory)

**Treat the complete set as one vertical ecommerce page, delivered as adjacent image slices—not as a collection of independent slides, posters, or cards.** A "screen" or "slice" is only a production/file boundary. It is not a buyer-visible page boundary.

- Plan one continuous top-to-bottom reading experience and buyer journey across the entire set.
- Every slice must connect naturally to its neighbors. Define a `top_edge_anchor` and `bottom_edge_anchor` for each slice; the previous slice's `bottom_edge_anchor` must inform the next slice's `top_edge_anchor`. Adjacent edges should share compatible background, color, lighting, texture, spatial depth, and visual direction.
- Extend the scene/background naturally to all four image edges. The bottom of one slice and the top of the next must feel like adjoining parts of the same page, not the end and beginning of separate slides.
- When a product, object, line, shadow, light beam, surface, or other visual element crosses a seam, align its position, scale, direction, and appearance across both slices. Do not create a crossing element unless it can be aligned reliably.
- Transitions between content areas may change scene, color, or density, but should be gradual and compositionally connected rather than abrupt slide resets. A shared visual world does not require one identical background on every slice.
- Keep typography, palette, lighting logic, material treatment, and spacing consistent across the full page while allowing meaningful variation in composition and information density.
- The first slice should enter the page naturally; the final slice should conclude it naturally. Do not turn them into separate cover and back-cover posters unless explicitly requested.
- Content modules may have their own internal cards or panels when useful, but do not frame every slice as a self-contained presentation slide.

**No slide chrome or page furniture:** unless explicitly requested, do not add page headers, footers, navigation bars, page numbers, screen/slice numbers, 01–08 labels, repeated logo/product title bars, corner ornaments, page borders, full-canvas frames, or decorative top/bottom rules. Do not repeat the brand logo or product name at the top of every slice. Do not place a visible "01 / PRODUCT OVERVIEW" or equivalent chapter marker on each image. Real instructional step numbers, model numbers, specifications, and quantities remain allowed.

- Do not create a 1:3 visual master or other continuity canvas unless the user explicitly requests it.
- Do not split one overview image or contact sheet into final deliverables.

## Page structure

Follow the requested number of image files. If the user requests an 8-screen page, create exactly 8 adjacent slices of one continuous vertical page—not 8 visually independent screens.

If the user does not specify a count for a long-form ecommerce detail page, use 8 as a practical default, adjusting only when the product or platform clearly calls for a different scope.

Each slice should answer a different buyer question or advance a different part of the purchase decision, while remaining part of the same continuous page. Avoid repeating the same hero layout, headline pattern, icon row, or feature-card grid. Do not make every slice independently self-contained.

Build a natural buyer journey rather than forcing every product into a rigid template. Depending on the product, useful modules may include:

- Product introduction and primary value.
- Main features and practical benefits.
- Construction, materials, or close-up details.
- How it works, installation, or operation.
- Application scenarios and compatibility.
- Product variants, configurations, or specifications.
- Evidence, limitations, and purchase confidence.
- A final selection or contact prompt.

Do not add a module merely to fill space. Do not show screen-order numbers (01–08, Screen 1, etc.) unless the user explicitly requests visible numbering. Treat all file/slice numbering as internal production metadata only. Real step numbers, model numbers, measurements, and quantities remain valid.

## Image generation

- Generate the actual requested final images, not instructions for the user to generate them.
- Give each slice a distinct content purpose and an appropriate composition while preserving the page-wide flow. Do not design it as an isolated slide or ask the image model for eight unrelated copies of one generic prompt.
- Use individual product images as product-appearance references. Use a visual/style reference only when the user explicitly designates it as such. Never use a full PDF page as a style reference by default; follow the Source-material roles and visual independence rules.
- Generate each requested image as a separate full-resolution file, but design neighboring files as adjoining slices of one long page. Generate in sequence where practical; carry forward the previous slice's outgoing edge handoff as the next slice's incoming edge condition. When image references are supported, use the adjacent slice as a continuity reference without copying its whole composition.
- Before finalizing, inspect the adjacent top/bottom edges at their intended displayed width. Repair mismatched background, lighting, texture, perspective, object alignment, or abrupt transitions. Do not add borders, blur, mirrored padding, or other devices to hide a failed join.
- Keep text concise enough to render legibly. Preserve exact critical copy and data; inspect every generated image for spelling, numbers, units, and unwanted pseudo-text.
- Do not add fake UI, badges, seals, ratings, certifications, watermarks, or decorative labels.
- Do not use blur, mirrored padding, stretching, oversized frames, or arbitrary crops to conceal a composition or aspect-ratio problem.

## Review and repair

Before delivery, inspect each image for:

1. **Product:** identity, structure, color, parts, and logo remain accurate.
2. **Copy:** spelling, exact critical wording, numbers, units, and legibility.
3. **Claims:** no unsupported technical or commercial statements.
4. **Design:** clear hierarchy, professional ecommerce quality, useful imagery, and no filler.
5. **Long-page continuity:** all images read as one vertical page when stacked in order; adjacent edges connect naturally without abrupt resets or visible slide boundaries.
6. **No slide chrome:** no unrequested headers, footers, page numbers, repeated title bars/logos, corner ornaments, page borders, or full-slice frames.
7. **Set consistency:** coherent visual language with meaningful composition variety.
8. **Visual independence:** the final design is an independently conceived ecommerce page, not a restyled, traced, or page-by-page adaptation of a supplied brochure or specification PDF unless explicitly requested.
9. **Completeness:** the requested number, order, ratio, and deliverables are present.

Repair the smallest responsible part:

- Text issue → revise the affected text or image.
- Product issue → correct the product depiction.
- Scene issue → revise that image's scene or composition.
- One-screen issue → repair only that screen.
- Set-wide inconsistency → adjust only the images affected by the shared visual rule.

Do not regenerate the entire set by default. Do not call a task complete merely because image generation returned successfully.

## Delivery

Deliver the final images in the format and order requested by the user. Keep the handoff concise.

Do not claim to provide a ZIP, editable source, full-page composite, or local file path unless it was actually created and is accessible. Do not include rejected drafts or intermediate assets unless requested.
