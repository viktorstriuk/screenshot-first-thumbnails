---
name: screenshot-first-thumbnails
description: Create authentic, eye-catching YouTube thumbnails from source screenshots, photos, and user-supplied characters using a human-made cutout-and-overlay aesthetic. Use for gaming, vlogs, travel, reactions, and other videos when the user wants a finished thumbnail while retaining the exact appearance of supplied avatars, logos, and pixel art rather than AI redesigns.
---

# Screenshot-First YouTube Thumbnails

## Goal

**Create the finished thumbnail**, not merely a prompt, idea, or design explanation. Make it look like a skilled YouTuber assembled it using screenshots/photos, pasted cutouts, bold typography, arrows, outlines, shadows, and selective edits in Photoshop, Photopea, or Canva.

**Core principle: compositing, not illustration.** Retain authentic source imagery. Do not redraw everything into a seamlessly lit AI poster.

**Non-negotiable: the user's supplied character is an asset to preserve, not a design prompt to reinterpret.** Visual identity takes priority over theme, embellishment, and stylistic cohesion.

## Inputs and Defaults

Use the request and attachments to identify the topic, the user-supplied character or logo, the background or setting, requested headline, language, and any references. If enough information exists, make the thumbnail immediately. Don't invent video events or claims. If no headline is given, choose a short headline in the user's language.

Default output: 16:9, ideally 1280×720 or higher. Keep key visuals away from the bottom-right YouTube duration badge.

## Workflow

### 1. Classify and Inventory Source Assets

- Identify which uploaded images are **identity-locked assets** (the person's avatar/character, mascot, brand mark, logo) and which are editable background/reference images.
- Treat every user-supplied character image as the **ground truth** for that character. Never treat it as a loose invitation to generate a new version.
- For gaming thumbnails, use a genuine screenshot from the correct game and edition where possible. Prefer a screenshot supplied by the user; otherwise use official galleries, publisher/store materials, or verified gameplay captures.
- For travel, vlogs, reactions, tutorials, and other non-gaming videos, use a real photo or genuine screenshot of the relevant setting when available. The gaming screenshot requirement does **not** apply to these topics.
- Distinguish a real screenshot/photo from key art, concept art, or an AI reconstruction. Don't claim an approximation is authentic source footage.
- Respect usage rights of sourced material and avoid misleading provenance claims.

### 2. Character Identity Lock — Highest-Priority Visual Rule

**If a character/avatar/mascot is attached, reproduce its appearance as faithfully as the available tools permit.**

Preserve the following exactly unless the user explicitly requests an alteration:

- face geometry; eyes, eyebrows, mouth, expression, and their positions;
- silhouette and body/head proportions;
- hairstyle, colors, distinctive shapes and markings;
- clothing, accessories already present, and exact design of those items;
- art style, line weight, pixelation, shading, rendering resolution, and color palette;
- original pose and hand/arm arrangement whenever the source permits.

**Do not**:

- redraw the head, face, eyes, or body to “improve” them;
- transform pixel art into smooth cartoon art, 3D, anime painting, or a higher-detail style;
- reshape eyes or mouth, invent extra pixels or facial features, smooth square corners, or change the character silhouette;
- put sunglasses, hats, scarves, uniforms, glasses, headphones, bags, costumes, facial expressions, or hand-held objects **on the character** merely to fit the video's theme;
- replace the original character with a similar-looking new character or change their pose without explicit permission;
- cover identity-defining face features with thematic props or headline text.

**Theme belongs around the character, not automatically on the character.** For example, for a “Dubai vlog” with a simple pixel mascot, keep the mascot visually identical and indicate Dubai with a skyline photograph, plane icon, location pin, suitcase sticker, or title arranged nearby. An accessory may sit beside or behind the cutout, but should not change its shape, face, or outfit.

If the user *explicitly requests* a wardrobe or pose change, make only that requested change, preserving all unrelated identity features. If editing tools cannot reliably make this narrow change, prefer the original look over an unrequested redesign and mention the limitation.

### 3. Pixel-Art / Icon / Logo Preservation

For low-resolution, geometric, pixel-art, flat-color, or icon-like assets:

1. **Best method: extract or mask the original pixels, then paste that exact image as a layer.** Keep the original RGB colors and geometry when possible.
2. Resize with **nearest-neighbor interpolation** to retain crisp edges; never use automatic smoothing, AI upscaling, anti-aliasing, or texture synthesis on the identity-locked layer by default.
3. Add an outline or shadow on **separate layers outside the silhouette**, not by altering the pixels inside it.
4. Avoid recoloring the character to match the scene. Keep scene lighting, glows, or color grading off the interior of the locked asset.
5. For backgrounds embedded in the character image, isolate the silhouette carefully. If transparent cutout extraction is uncertain, preserve the original rectangular asset rather than hallucinating missing edges or body parts.
6. Do not add costume elements to empty transparent regions of the character layer. Add decorations as independent graphics elsewhere.

**Identity comparison gate:** Compare the output character against the uploaded original at a similar size. Check eyes, mouth, silhouette, color blocks, pixel geometry, original accessories, and pose. If anything identity-defining changed without user consent, the draft fails even if it is attractive. Rebuild with the unmodified original cutout.

### 4. Choose the Background and Main Subject

- Keep real gameplay/photo texture and recognizable environment details. Crop and make modest local adjustments as needed; avoid AI reimagining of the whole scene.
- In gaming, preserve correct in-game models and visually identifiable monsters/locations. Don't substitute different games in a franchise or invent game HUD elements.
- In travel/vlogs, preserve recognizable landmarks and photographic texture rather than turning locations into unrealistically polished fantasy scenes.
- If a real source frame is technically unavailable, a generated backdrop may be used, but **do not generate the character together with it** when separate-layer compositing is possible. Be transparent that the background is reconstructed.

### 5. Compose as a Human Editor Would

- Place the original cutout on the left or another prominent side (often 30–50% of the image width), with identity-defining features clearly visible.
- Give the background's main subject room: a monster, landmark, location, object, or important event.
- Use a short readable headline, generally 2–5 words across one or two lines.
- One simple arrow, circle, location pin, or sticker can direct attention, but not every thumbnail needs one.
- Let elements overlap slightly. Human-made layer separations are desirable: the avatar may have a white sticker border and offset black shadow even though the photographed backdrop has different lighting.
- Do not forcibly make all materials look as though they were photographed or rendered together.

### 6. Apply Simple, Local Editing Effects

Use thick white cutout borders, thin black strokes, hard or offset shadows, localized airbrush glow, modest contrast/saturation adjustments, simple hand-drawn arrows, and white/yellow text with strong dark outlines.

Keep effects uneven and selective rather than uniformly cinematic. Don't flood the whole image with sparks, smoke, orange glows, excessive lens flares, or fragments. **Never apply these effects by repainting the identity-locked character layer.**

### 7. Typography and Legibility

- Keep the headline short, large, and readable at phone size; honor the user's exact text and language if provided.
- Avoid tiny text, meaningless HUD text, random symbols, unnecessary logos, and misspelled Cyrillic characters.
- Protect the character's face and the main subject from text overlap.
- Keep text contrast high without making the thumbnail look like an official movie poster.

### 8. Choose the Right Production Method

**If programmatic editing/layer composition is available:**

1. Use the real source background.
2. Mask/extract the user-provided character without modifying its internal pixels.
3. Scale/position the locked layer using an appropriate interpolation method (nearest-neighbor for pixel art).
4. Add separate layers for outline, shadows, text, markers, and effects.
5. Export the final thumbnail; visually compare the character with the original.

**If only a generative image editor is available:**

- Request a composite of the exact supplied character cutout; explicitly state that the character is an immutable reference asset, not a redesign target.
- Restrict any creative generation to the backdrop, text treatment, and **separate** decorative elements; do not ask the model to reimagine the character for the setting.
- Inspect the output carefully for changes to facial pixels, body proportions, costume, or style. Retry with stronger isolation instructions if possible.
- **Do not claim pixel-perfect or exact identity preservation if the model has redrawn the character.** If exactness cannot be achieved, state the limitation and recommend actual layer compositing for fidelity.

**If only text output is available:** Provide an actionable editing recipe or prompt, clearly indicating that a finished image could not be produced.

## Things to Strictly Avoid

- Reimagining the user's supplied avatar as a traveler, hunter, influencer, superhero, etc. without explicit instruction.
- Adding sunglasses, hats, scarves, expressions, or new body parts because they fit a theme.
- Rounding/reshaping pixel-art eyes, mouth, outlines, or body proportions.
- Generating the backdrop and avatar as one unified scene when the user's exact character should instead be pasted on top.
- Converting real game screenshots into polished painted fantasy art.
- Fake creatures presented as real game monsters, nonexistent interfaces, and overworked AI-poster lighting.
- Effects that mask design differences or make a character appear “close enough” when it is no longer the original.

## Priorities When Requirements Conflict

1. Explicit user requirements and explicitly requested edits.
2. **Identity fidelity of supplied characters, mascots, logos, and pixel art.**
3. Authenticity and fidelity of source screenshots/photos.
4. Legible thumbnail composition and headline.
5. Theme-matching decorations, aesthetic cohesion, and spectacle.

**Never trade character fidelity for improved thematic styling.** When “more spectacular” conflicts with “looks genuinely composited,” prefer the latter.

## Final Quality Gate

Before sending, check:

- [ ] Does the supplied character still have the **same face, eyes, mouth, silhouette, proportions, colors, clothing, expression, and pose**?
- [ ] For pixel art, do the key pixel shapes remain crisp and unchanged, with no smoothing or improvised features?
- [ ] Are all thematic hats, sunglasses, scarves, and similar additions absent unless explicitly requested?
- [ ] Does the character feel like the **original image was pasted on top**, rather than regenerated in the background's style?
- [ ] Does the background retain the appropriate game's or location's authentic appearance where real imagery was available?
- [ ] Is the headline correct and clearly readable when small?
- [ ] Do simple Photoshop-like effects support the content without hiding it?
- [ ] Is the final image convincingly handmade rather than a fully illustrated cinematic poster?

**Identity is a hard gate:** if any of the first four conditions fail, correct the result or disclose inability to preserve the original character. Do not accept an identity-changing output just because the rest looks good.

## Output

Deliver the finished thumbnail image when tools permit, preferably PNG or JPG. Keep the follow-up concise. State whether real screenshots/photos or reconstructed imagery were used, especially if exact source preservation was unavailable. Never assert that the character is unchanged if it was actually regenerated and visibly altered.

## Examples

**Gaming:** “Make a Monster Hunter thumbnail. Use my attached character exactly as it is on the left, a real Rathalos gameplay screenshot on the right, and the text ‘FIRST HUNT!’.” The character keeps its original face/clothes/style; separate white outline, arrow, and headline layers are added.

**Travel:** “Make a Dubai vlog thumbnail with my attached pixel mascot.” Place the **unchanged pixel mascot** as a large crisp cutout over a real Dubai skyline photo; add the text “DUBAI VLOG!” and independent travel stickers. **Do not** give the mascot sunglasses, a hat, scarf, backpack, altered eyes, or a new pose unless the user requests it.
