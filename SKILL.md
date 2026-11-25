---
name: product-detail-designer
description: Create commercial-quality ecommerce product detail page images from product photos, product documents, and visual references. Use when a user asks to create, design, generate, or improve product listing images, ecommerce detail pages, product feature panels, or long-form product page visuals.
license: MIT
---

# Product Detail Designer

A brand-neutral, chat-first skill for creating ecommerce product detail page images across industries and product categories.

## Core contract

1. **The user's prompt is the production brief.** Follow its requested page count, language, ratio, style, approval gates, and deliverables. Do not rewrite the brief or add workflow stages.
2. **Default to making the images.** When the user supplies product images and asks for finished detail-page images, analyze the inputs internally and proceed to image generation. Do not stop at advice, a long blueprint, or a design discussion unless the user asks for planning or their prompt explicitly requires approval.
3. **Keep the interaction lightweight.** Ask a question only when a missing or conflicting fact would materially change the product depiction or make the result commercially misleading. Otherwise make a reasonable design decision and continue.
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

### Backgrounds and continuity

- Integrate a suitable background into each final image. Do not generate a separate background image as a prerequisite.
- Use a consistent visual language across the set; do not force one identical background onto every screen when different scenes better explain the product.
- Maintain continuity through shared colors, lighting logic, typography, spacing, materials, and recurring visual cues.
- Do not create a 1:3 visual master or other continuity canvas unless the user explicitly requests it.
- Do not split one overview image or contact sheet into final deliverables.

## Page structure

Follow the requested number of images. If the user requests an 8-screen page, create exactly 8 distinct screens.

If the user does not specify a count for a long-form ecommerce detail page, use 8 as a practical default, adjusting only when the product or platform clearly calls for a different scope.

Each screen should answer a different buyer question or advance a different part of the purchase decision. Avoid repeating the same hero layout, headline pattern, icon row, or feature-card grid.

Build a natural buyer journey rather than forcing every product into a rigid template. Depending on the product, useful modules may include:

- Product introduction and primary value.
- Main features and practical benefits.
- Construction, materials, or close-up details.
- How it works, installation, or operation.
- Application scenarios and compatibility.
- Product variants, configurations, or specifications.
- Evidence, limitations, and purchase confidence.
- A final selection or contact prompt.

Do not add a module merely to fill space. Do not show screen-order numbers (01–08, Screen 1, etc.) unless the user explicitly requests visible numbering. Real step numbers, model numbers, measurements, and quantities remain valid.

## Image generation

- Generate the actual requested final images, not instructions for the user to generate them.
- Give each screen its own content and composition. Do not ask the image model for eight unrelated copies of one generic prompt.
- Use the supplied product and style references directly when the image tool supports references.
- When several final images are needed, generate them as distinct screen-specific outputs. Use a multi-image batch only when the tool supports different instructions for each image.
- Keep text concise enough to render legibly. Preserve exact critical copy and data; inspect every generated image for spelling, numbers, units, and unwanted pseudo-text.
- Do not add fake UI, badges, seals, ratings, certifications, watermarks, or decorative labels.
- Do not use blur, mirrored padding, stretching, oversized frames, or arbitrary crops to conceal a composition or aspect-ratio problem.

## Review and repair

Before delivery, inspect each image for:

1. **Product:** identity, structure, color, parts, and logo remain accurate.
2. **Copy:** spelling, exact critical wording, numbers, units, and legibility.
3. **Claims:** no unsupported technical or commercial statements.
4. **Design:** clear hierarchy, professional ecommerce quality, useful imagery, and no filler.
5. **Set consistency:** coherent visual language with meaningful composition variety.
6. **Completeness:** the requested number, order, ratio, and deliverables are present.

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
