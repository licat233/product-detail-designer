# Changelog

## 1.0.5 — 2026-11-26

- Added a mandatory **Open-ended Slice** contract: every non-final image must end in the middle of a continuing page, not with a visual closing composition.
- Added `top_edge_mode`, `bottom_edge_mode`, `continuity_carrier`, and `next_slice_handoff` to the slice boundary contract.
- Required a visible non-text continuity carrier to reach or cross the bottom edge of every non-final slice and continue into the next.
- Prohibited visual closing cues on intermediate slices, including bottom whitespace, fades, vignettes, completed card grids, divider lines, end bands, and isolated final compositions.
- Reserved a 10–15% lower continuation zone for non-final slices, keeping critical text away from crop boundaries.
- Required sequential one-image-at-a-time generation; never batch-generate the remaining slices.
- Added a mandatory open-bottom inspection after each generation and a full-page audit that allows only the final slice to close.
- Clarified that a closed intermediate slice must be regenerated before the next slice is produced.

## 1.0.4 — 2026-11-26

- Replaced the screen-first mindset with mandatory **Page first, slices second** composition.
- Made the complete vertical ecommerce page—not each image file—the design unit.
- Limited the page-level H1 / primary title to the first slice only.
- Prohibited per-slice product-introduction titles, repeated hero openings, summaries, website footers, repeated logos, contact bars, and independent sign-offs.
- Clarified that file boundaries do not need to align with content-section boundaries; content and visual scenes may continue across slices.
- Required later slices to be generated sequentially as continuations of the previous slice, using image extension/outpainting when supported or the previous image as a continuation reference.
- Added explicit page-level and slice-boundary audits to reject title/footer repetition and slide-like restarts.

## 1.0.3 — 2026-11-25

- Added mandatory Continuous Long-Page Composition for multi-image ecommerce detail pages.
- Clarified that screens are adjacent production slices of one vertical page, not independent posters or presentation slides.
- Required natural top/bottom edge handoffs and continuity in background, lighting, spatial depth, texture, and visual direction.
- Prohibited unrequested headers, footers, page numbers, 01–08 labels, repeated logo/title bars, corner ornaments, page borders, and slide-like frames.
- Expanded the final audit to inspect image joins and reject slide chrome or standalone-slide styling.
- Updated bilingual README and ChatGPT quick start.

## 1.0.2 — 2026-11-25

- Added explicit separation between product evidence and visual-design references.
- Product PDFs, brochures, manuals, and specification sheets are factual sources by default, not visual templates.
- Prohibited copying, tracing, recoloring, rearranging, or page-by-page adapting source-document UI and layouts for ordinary ecommerce detail-page production.
- Required independently conceived ecommerce storytelling and visual design based on the product, buyer, market, and platform.
- Clarified that individual product photos may be used as appearance references, while complete PDF pages must not be passed as design references by default.
- Added a visual-independence check to the final quality audit.
- Updated the bilingual README and ChatGPT quick start.

## 1.0.1 — 2026-11-25

- Added a required Production Brief Confirmation checkpoint before final image generation.
- Confirm output language, image dimensions/aspect ratio, ecommerce platform and placement, and sales region.
- Ask for all missing items together in one concise message; do not repeat information already supplied.
- Recommend image dimensions when the target placement is known, and distinguish recommendations from verified platform requirements.
- Allow users to explicitly delegate individual decisions while preventing silent assumptions.
- Updated the ChatGPT quick start and bilingual usage documentation.

## 1.0.0 — 2026-11-25

- Initial public release of Product Detail Designer.
- Brand-neutral and product-category-neutral.
- Chat-first, direct image-generation workflow.
- No local dependencies or required external services.
- Product identity and factual-claim safeguards.
- No unrequested background assets, visual masters, HTML reviews, or extra approval gates.
