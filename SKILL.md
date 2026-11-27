---
name: product-detail-designer
description: Create commercial-quality ecommerce product detail page images from product photos, product documents, and visual references. Use when a user asks to create, design, generate, or improve product listing images, ecommerce detail pages, product feature panels, or long-form product page visuals.
license: MIT
version: 1.0.6
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
8. **Product appearance integrity is P0.** Original product photos are identity anchors; every product-bearing slice must be checked against them. Product identity outranks page continuity and visual polish.

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

## Product identity integrity — P0 hard gate

**The real product is the subject of the page, not a visual suggestion for the image model. Product identity is a non-negotiable acceptance condition (P0), not a weighted design score.** A beautiful image that depicts a different-looking product is a failed deliverable.

### Build an internal Product Identity Lock

Before planning the page, establish a compact internal identity record from the supplied evidence. Do not turn this into a form the user must fill in or an unsolicited report.

Record:

- `product_identity`: exact product name, model, variant, and any visually similar variants that must not be mixed.
- `identity_anchor_assets`: filenames or asset IDs of the original, unedited product photographs that establish the real appearance.
- `supporting_visual_assets`: genuine close-ups, additional views, installation photos, and application photos that clarify particular features.
- `identity_markers`: visible silhouette and proportions; component count and arrangement; distinctive geometry; ports, connectors, fasteners, markings, logos, and labels; color, finish, texture, and material appearance; included parts and assembly relationships.
- `unknown_or_unseen`: sides, internal structures, hidden parts, colors, dimensions, or details that the supplied evidence does not establish.
- `forbidden_changes`: the identity markers that must not be added, removed, reshaped, recolored, relocated, or replaced.

Use the user's explicit corrections and identification of the authoritative product assets as the controlling source. If the model or variant is ambiguous, or two source assets appear to show different versions, ask one concise question before generating product imagery. Do not silently combine them.

Keep this record internal unless the user asks to see it. The goal is reliable execution, not additional paperwork.

### Evidence and reference roles

Keep these reference roles separate in every image-generation task:

1. **Product identity anchors — original source assets.** Original product photos and genuine close-ups establish what the product actually looks like. Engineering drawings can establish documented geometry and relationships. Use the closest matching original view for the depiction being made.
2. **Page-continuity reference — previously accepted slice.** It establishes the scrolling page's background, scene, composition, lighting direction, perspective, and content handoff only. It is not a source of truth for product geometry, color, construction, markings, or component count.
3. **Visual-style reference — explicitly designated design material.** It guides only the visual aspects the user asks it to guide; it does not override product identity.

The original product identity anchors always take precedence over generated images and page-continuity references. Never promote an AI-generated slice, a Visual Master, a moodboard, or a prior AI rendering into an authoritative product reference. A Visual Master may guide page-level design, but any product depiction inside it remains illustrative unless it is the untouched original source photo.

For every slice that depicts the product, include the relevant original identity anchor(s) in that generation task whenever the tool supports multiple references. If the tool accepts only one image reference, prioritize the original product identity anchor; carry page continuity through the written handoff instead. **Product identity outranks page continuity.**

### Choose a product-depiction mode for each slice

Set an internal `product_depiction_mode` for each slice that shows the product:

- **`original-photo` — safest default.** Use the actual supplied product photograph as the product image. Non-destructive cropping and uniform scaling are acceptable when they do not hide or distort identity-critical details. Design the typography, layout, background, and supporting information around it.
- **`source-photo-composite` — preferred when a new scene is needed and true compositing is available.** Keep the original product photo or cutout as the foreground subject and create or edit the surrounding scene separately. Use masking/layers only when the available tool actually supports them and the original product pixels can remain unchanged. Do not call a reference-based redraw a pixel-preserving composite.
- **`constrained-edit` — controlled fallback.** Use image editing only when the tool can work from the actual source image and the requested edit does not require inventing a new product view. Keep the same evidenced angle and construction. Inspect the result against the original; a reference image alone does not guarantee fidelity.
- **`evidence-based-diagram` — for technical explanation.** Build a schematic or explanatory diagram from an authoritative drawing or clearly visible structure. Preserve the engineering meaning. Do not present an inferred diagram as a photorealistic product photograph.
- **`no-product-depiction` — when evidence is insufficient.** Use copy, typography, application context, or a neutral explanatory visual rather than inventing an unseen product detail.

Prefer `original-photo` whenever it can communicate the point clearly. Do not choose a more elaborate mode merely to make the page look more sophisticated.

### Protected product attributes

Do not let image generation or editing:

- Change the product model, variant, silhouette, geometry, proportions, thickness, shape, or distinctive construction.
- Add, remove, duplicate, merge, or rearrange components, LEDs, lenses, holes, fasteners, ports, wires, connectors, controls, accessories, or package contents.
- Change component count, spacing, alignment, orientation, connection points, or assembly relationships.
- Change product color, material appearance, finish, surface texture, printed markings, labels, logo, model number, or other identifying details.
- Invent a rear view, internal structure, close-up, connector, or feature that is not visible in the source evidence.
- Use perspective warping, non-uniform stretching, generative fill inside the product silhouette, or retouching that changes the product's structure.

Do not request a different camera angle or a hidden side unless a genuine reference for that view exists. If the source only establishes one view, use that view or ask for the missing photo. Never fill an evidence gap with a plausible-looking guess.

### Pixel preservation and capability honesty

Do not promise that a product is pixel-preserved merely because an image was supplied as a reference. Only describe a result as pixel-preserving when the actual operation keeps the original product pixels intact (for example, a verified mask/layer composite) and the output has been checked.

If the available image tool cannot reliably isolate or preserve the product:

1. Use the original product photograph directly in the page layout; or
2. Use a simpler composition that leaves the product image untouched; or
3. Explain which additional real product photo is needed.

Do not silently substitute an AI-redrawn approximation and present it as the real product. Lighting, reflections, shadows, and scene effects may be designed around the product, but must not obscure or rewrite its identity markers.

### Per-slice identity handoff

For every product-bearing slice, the internal slice plan must identify:

- `product_depiction_mode`
- `identity_anchor_assets` to be used for that exact depiction
- `critical_identity_markers` to inspect
- `forbidden_changes` relevant to the slice
- Any `unknown_or_unseen` detail that must remain absent or be clearly represented as a schematic

The accepted previous slice may be supplied as a secondary page-continuity reference. It must never replace the original identity anchor. If a previous slice contains a product depiction that later fails the P0 identity check, reject it and do not use it as the next slice's continuity reference.

### P0 appearance verification and recovery

Compare every generated product depiction side by side with its original identity anchor(s), not merely with the previous generated slice. Inspect the actual visible identity markers. A model's statement that it preserved the product is not proof.

Classify any discrepancy:

- **Critical — automatic fail:** wrong model or variant; changed functional structure; missing, extra, duplicated, or merged component; altered connector/port/assembly; invented or removed identity-defining part; or any change that could make the image depict a different product.
- **Major — fail:** clearly changed silhouette, proportions, component spacing or placement, product color/material/finish, labels, logo, model marking, or other recognisable construction detail.
- **Minor — review:** background, surrounding props, lighting outside the product, or a crop/composition issue that does not alter or conceal an identity marker. If a reflection, shadow, or crop makes a critical feature unverifiable, it is not a minor pass.

P0 result must be **PASS / FAIL / UNVERIFIED**. Any Critical or Major discrepancy, or any unverified critical marker, means FAIL. A high visual-design score cannot override a P0 failure.

When a product depiction fails:

1. Reject that image as a product-accurate deliverable.
2. Prefer replacing the product region with the original photo or rebuilding the composition around the untouched source asset.
3. If reliable compositing is unavailable, revert to `original-photo` or `no-product-depiction`; do not keep prompting the model to redraw the same inaccurate geometry.
4. Recheck any following slice that used the rejected image as a continuity reference. Continue only from the last accepted slice.
5. If the supplied evidence cannot support an accurate depiction, explain the limitation and request the specific missing real photo or drawing.

Never pass a failed or unverified product depiction forward as an accepted reference.

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
- One coherent page-level composition, with content modules arranged in a continuous buyer journey.

Keep one page-wide composition. Vary camera angle, crop, product scale, layout, and information density naturally as the page progresses; do not assign a fresh layout or visual opening to every file.

### Page-first composition (mandatory)

**Design one complete vertical ecommerce page first. Only afterward divide that page into separate image files.** The page is the design unit. A Screen / Slice is only a file-delivery boundary; it is not a page, slide, poster, panel, or self-contained content module.

#### Page-level structure

- Plan the complete top-to-bottom buyer journey as one uninterrupted page. Do not independently design each image and try to make the results look related afterward.
- The page gets **one primary title / H1 only**, placed in the opening of the first slice. Never add a new page title, product-introduction headline, masthead, or hero-title band to the top of every later slice.
- Intermediate slices continue the page. They do not need their own introduction, headline, summary, conclusion, or CTA.
- Do not add a footer to any slice. A product-detail image sequence is not a website shell. Do not invent a website footer, contact footer, logo footer, repeated bottom bar, or per-image sign-off. If a final CTA is useful, place it once at the actual end of the complete page and integrate it into the content; it must not look like a footer.
- Show the brand logo, product name, and model identifier only where they genuinely help the page. Do not repeat them as fixed top or bottom furniture on every image.
- Section headings are allowed when a new content section genuinely begins, but they must be part of the flowing page—not a repeated title bar or a large standalone heading that resets each image.
- A slice may begin or end partway through a visual scene or content module. It does not need to be independently complete. Content modules may span across file boundaries.
- Choose slice boundaries after planning the complete page. Do not force every boundary to coincide with the end of a feature, card, section, or buyer question.
- Keep critical copy, specifications, and labels away from cut boundaries so text is not severed. Let the background, scene, product-scale rhythm, diagrams, surfaces, and other visual elements carry the continuity across those boundaries.
- A page may move between scenes or content areas, but transitions must feel like a continuous scroll. Do not restart the composition, background, lighting, or visual hierarchy at the top of each file.

#### Slice boundary contract

For each slice, define internally:

- `slice_entry_state`: what is already happening as the viewer scrolls into this portion of the page.
- `slice_exit_state`: what remains visually or informationally in progress as the viewer scrolls out.
- `top_edge_anchor`: the observable visual state near the top edge, such as background, surface, object position, lighting, perspective, and direction.
- `bottom_edge_anchor`: the observable visual state near the bottom edge.
- `continuity_intent`: how the next slice should continue the page, or why a natural scene transition is appropriate.
- `next_slice_handoff`: the relevant position, direction, scale, perspective, lighting, background, and content state that the next slice should pick up.

The next slice's handoff must be derived from the previous slice's actual generated image, not from a generic instruction such as "same style". Describe only details that can be observed or reliably established. These fields guide composition; they do not imply that the image model can reproduce exact pixels.

#### Non-final slice continuity contract

**Every non-final slice must continue the same page flow. It must not look like a separately completed poster or slide.** A file boundary is a delivery boundary, not a reason to restart or conclude the page.

For each slice, define:

- `top_edge_mode`: `opening` for Slice 01; `continuation` for every later slice.
- `bottom_edge_mode`: `open` for every non-final slice; `closed` only for the final slice.
- `continuity_strategy`: one of `canvas-extension`, `reference-continuation`, or `tonal-continuity`.
- `next_slice_handoff`: the concrete visual and content state the next slice should continue.

Do not force every non-final image to contain a physical object crossing its bottom edge. Do not reserve a mandatory 10–15% strip, add artificial cables/rails/surfaces, or distort a useful composition merely to satisfy a mechanical seam rule. A continuous surface, line, shadow, light strip, or product-supporting element may help when it naturally belongs to the scene, but it is optional.

##### Choose a continuity strategy based on actual tool capability

1. **Canvas extension** — Use when the currently available image tool explicitly supports extending the existing canvas or outpainting while preserving the original area. Extend from the actual previous image. Do not assume this capability exists merely because the tool can accept a reference image.
2. **Reference continuation** — Use as the normal approach when the image tool can reference an earlier image but does not provide a verified canvas-extension operation. Use the actual previous image as a visual reference and describe the required handoff. Preserve the scene, perspective, lighting, material, color relationships, and visual direction as closely as the tool allows. This is a visual continuation strategy, not a promise of pixel-perfect edge matching.
3. **Tonal continuity** — Use when the page's content naturally moves into a different scene or when forcing the previous physical scene to continue would look artificial. Maintain a coherent relationship in palette, lighting, material language, depth, and visual hierarchy. The transition must still feel like the next part of the same ecommerce page, not a new poster.

##### Selection and honesty rules

- Follow an explicit user requirement for strict canvas continuity when the tool can actually support it.
- If the user requires pixel-level or seamless canvas extension and the available tool cannot reliably provide it, explain the limitation before proceeding. Do not silently downgrade the requirement to reference continuation or tonal continuity.
- Never describe reference continuation as pixel-preserving outpainting or guarantee a seamless join unless the actual operation and output have been verified.
- Do not use tonal continuity as an excuse to create unrelated, self-contained slides. It changes the scene, not the page-level narrative.
- Keep important copy, specifications, labels, and product geometry away from crop boundaries. Never split text or critical product details merely to manufacture an open edge.
- Every non-final slice must avoid visual closing cues such as a summary panel, sign-off, CTA, footer, fade-to-blank, or an isolated completed composition. A natural content transition is allowed; a visual page ending is not.
- Only the final slice may use `bottom_edge_mode: closed` and conclude the complete page. It may contain the page's single final CTA when appropriate.

Generate one slice at a time. Inspect the actual result before using it as the reference for the next slice. If its bottom edge reads as a page ending, revise that slice before continuing. Do not generate the remaining slices as a batch.

#### No slide chrome or page furniture

Unless explicitly requested, do not add:

- Page headers, footers, navigation bars, page numbers, screen/slice numbers, 01–08 labels, or chapter markers.
- Repeated page titles, product-introduction titles, logo bars, product-name bars, or model-number mastheads.
- Repeated top/bottom banners, contact strips, decorative rules, corner ornaments, page borders, full-canvas frames, or full-slice card containers.
- A self-contained "title at top + hero + feature cards + footer" composition in every image.
- A new hero image or product introduction at the beginning of every slice.
- An ending treatment, summary panel, or CTA at the bottom of every slice.

Real instructional step numbers, model numbers, specifications, and quantities remain allowed when they are genuine content.

If the user explicitly requests a 1:3 visual master or other continuity reference, use it to plan the page-level composition. It must not turn into a row of separate poster panels. Do not split an overview image or contact sheet into final deliverables.

## Page structure

Follow the requested number of image files. If the user requests an 8-image detail page, create exactly 8 slices of one continuous vertical page.

Plan the buyer journey at the **page level**, not as eight independent mini-briefs. The page may contain product introduction, features, construction details, operation, applications, configurations, specifications, trust information, and one final purchase/contact prompt. Distribute these modules according to the product and platform; a module may continue across more than one slice, and a slice may contain parts of more than one module.

Do not require every slice to answer a different buyer question. Some adjacent slices may continue the same question or content thread. The goal is a coherent page, not eight individually complete answers.

Do not add a module merely to fill space. Treat file numbering as internal production metadata only. Real step numbers, model numbers, measurements, and quantities remain valid.

## Page planning and per-slice task compilation

Before image generation, plan the complete page as one coherent buyer journey. Keep this planning work internal unless the user asks to review a blueprint or their prompt defines an approval gate.

The internal Page Blueprint should contain only the information needed to produce and verify the page:

- Page goal, audience, platform placement, and confirmed production constraints.
- The buyer journey and the logical order of information.
- The single page-level H1 and the approved or planned copy.
- A global visual specification: palette, typography direction, lighting, materials, image treatment, and visual hierarchy.
- A slice map: each slice's purpose, content, relevant product assets, composition, text, top/bottom visual state, and intended handoff.
- For each product-bearing slice: `product_depiction_mode`, `identity_anchor_assets`, `critical_identity_markers`, and relevant `forbidden_changes`.
- The continuity strategy selected for each boundary, based on the tool's actual capabilities and the product scene.

Do not force an eight-slice request into eight unrelated content modules. A content module may continue across file boundaries, and a slice may contain the end of one module and the beginning of another. Do not add filler to make every slice appear equally complete.

### Per-slice prompt compiler

Before each image-generation call, compile a focused task for the current slice only. Include:

1. The current slice's purpose and the portion of the page it represents.
2. Only the relevant global visual rules.
3. The exact copy and factual data intended for this slice.
4. For every product-bearing slice: `product_depiction_mode`, the original `identity_anchor_assets`, the `critical_identity_markers`, and the relevant `forbidden_changes`.
5. The previous accepted image when relevant to continuity, explicitly identified as a page-continuity reference only—not product evidence or a source of product geometry.
6. The chosen continuity strategy and the concrete handoff requirements.
7. The output dimensions/aspect ratio and any user-defined constraints.

Attach the original identity anchor(s) to every generation task that depicts the product whenever the tool supports it. If the tool accepts only one image reference, use the original product anchor and describe the previous slice's continuity state in text. Do not resend the entire eight-slice plan as if all slices were being generated at once. Do not let the previous image override product-source images for product geometry, color, construction, or markings. Do not let a product photograph accidentally become a visual-style template. Keep every reference's role explicit.

Unless the user requests a blueprint or approval checkpoint, do not turn the internal Page Blueprint or prompt compiler into extra user-facing deliverables or approval stages.

## Image generation

- Generate the actual requested final images, not instructions for the user to generate them.
- Generate only the current requested slice in each call. Never ask for a multi-image batch of the remaining slices, a contact sheet, or a collage as a substitute for the individual final images.
- Place only the portion of the page's content that naturally belongs in the current slice. Do not force a separate content module or a complete composition into every file.
- For every slice that depicts the product, use the relevant original product photo(s) as identity anchors. Use the previous accepted slice only for page continuity. Never use a full PDF page as a style reference by default.
- Prefer `original-photo` or a verified `source-photo-composite`. Do not let the image model freely redraw, redesign, recolor, reshape, or invent product details to improve the composition.
- If both product identity and page continuity references cannot be supplied, prioritize product identity and use a written continuity handoff. Do not trade product accuracy for a closer-looking seam.
- Do not generate unseen angles, hidden sides, internal structures, or unsupported close-ups. Use a real source image or an evidence-based diagram; otherwise omit the depiction.
- If true masking/layer compositing is not supported, do not claim that the original product pixels were preserved. Use the original photo directly or explain the limitation.
- Generate the first slice as the single opening of the page. It may contain the page's one primary title / H1 and opening hero.
- Generate later slices **one at a time, sequentially**. Include the actual previous accepted image when the tool supports image references, together with the current slice's planned content and handoff. Use canvas extension only when that operation is explicitly available; otherwise use reference continuation or tonal continuity as selected in the Page Blueprint.
- For Slice 02 and later, do not add a new page title, product introduction, repeated hero, summary, footer, contact bar, or bottom sign-off. Begin with the continuation of the prior page flow. Only the final slice may close the composition. Add a section heading only when the page's actual content structure calls for one, not merely because a new file begins.
- Preserve the page-wide visual hierarchy. Later slices should continue the established page, but the continuity method must match the actual tool capability. Do not promise exact pixel alignment when using a reference image.
- Keep text, critical data, and important product geometry away from crop boundaries. Do not split a word, sentence, specification, or label across files. Do not add artificial physical objects or reserve a fixed bottom strip merely to satisfy a seam rule.
- Inspect adjacent images as parts of one scrolling page. Check background, lighting, material, perspective, object position, visual direction, and content flow. If the available interface permits actual stacking or a composite preview, inspect that result; otherwise inspect the individual images and their adjacent edge regions. Do not claim pixel-perfect seam validation without a real pixel-level comparison.
- Repair visual endings, abrupt scene resets, mismatched background or lighting, perspective shifts, title/footer repetition, and self-contained slide layouts. Use the smallest repair that fixes the issue; do not regenerate the whole set by default.
- Keep text concise enough to render legibly. Preserve exact critical copy and data; inspect every generated image for spelling, numbers, units, and unwanted pseudo-text.
- Do not add fake UI, badges, seals, ratings, certifications, watermarks, or decorative labels.
- Do not use blur, mirrored padding, stretching, oversized frames, or arbitrary crops to conceal a composition or aspect-ratio problem.
## Review and repair

**P0 product-identity gate — run before judging visual polish or any weighted quality score.** Compare every product depiction side by side with its original identity anchor(s). The P0 result must be PASS, FAIL, or UNVERIFIED. Any Critical or Major mismatch, or any critical feature that cannot be verified, rejects the image. No aesthetic score can compensate for a product-identity failure.

Before delivery, inspect each image for:

1. **Product identity (P0):** model/variant, silhouette, proportions, construction, component count and arrangement, ports/connectors, markings, logo, color, material appearance, and assembly remain consistent with the original product evidence.
2. **Copy:** spelling, exact critical wording, numbers, units, and legibility.
3. **Claims:** no unsupported technical or commercial statements.
4. **Design:** clear hierarchy, professional ecommerce quality, useful imagery, and no filler.
5. **Page-first structure:** the complete sequence has one page-level opening and no repeated per-slice title, hero, summary, or footer.
6. **True continuation:** Slice 02 and later continue the previous slice's page flow instead of restarting with a new title, product introduction, or independent composition.
7. **Non-final slice continuity:** every non-final slice continues the page flow without a visual ending. The selected continuity strategy matches the actual image-tool capability; no artificial physical carrier or pixel-perfect seam is required unless the user explicitly requests it and the tool supports it.
8. **Long-page continuity:** all images read as one vertical page when stacked in order; adjacent edges connect naturally without abrupt resets or visible slide boundaries.
9. **No slide chrome:** no unrequested headers, footers, page numbers, repeated title bars/logos, corner ornaments, page borders, full-slice frames, or per-image closing areas.
10. **Set consistency:** coherent visual language with meaningful composition variety.
11. **Visual independence:** the final design is an independently conceived ecommerce page, not a restyled, traced, or page-by-page adaptation of a supplied brochure or specification PDF unless explicitly requested.
12. **Completeness:** the requested number, order, ratio, and deliverables are present.

Repair the smallest responsible part:

- Text issue → revise the affected text or image.
- Product-identity issue → reject the generated product depiction; replace it with the original source photo or a verified composite. Do not repeatedly regenerate an inaccurate product region and do not use the rejected image as a future reference.
- Scene issue → revise that image's scene or composition.
- One-slice issue → repair only that slice.
- A non-final slice reads as a visual ending or its handoff is inconsistent → repair that slice, then recheck the following slice against the corrected handoff.
- A requested canvas-extension or pixel-perfect seam cannot be produced by the available tool → explain the limitation and obtain direction before substituting another continuity strategy.
- Repeated title/footer or slide structure → revise the page-level layout rule and regenerate every affected slice.
- Set-wide inconsistency → adjust only the images affected by the shared visual rule.

Do not regenerate the entire set by default. Do not call a task complete merely because image generation returned successfully.
## Delivery

Deliver the final images in the format and order requested by the user. Keep the handoff concise.

Do not claim to provide a ZIP, editable source, full-page composite, or local file path unless it was actually created and is accessible. Do not include rejected drafts or intermediate assets unless requested.
