---
name: four-grid-character-board
description: Create consistent four-panel character reference board workflows from face, outfit, hairstyle, animation, or text references. Use when the user asks for character boards, four-grid character boards, multi-view character reference images, cinematic character references, mother-image/master-image workflows, or GPT-agent character board instructions.
---

# Four Grid Character Board

## Overview

Use this skill to produce a high-consistency character reference set for a single character. The workflow uses a master front full-body image first, then derives individual single-image views for a final user-assembled 2x2 board.

For the full production specification, read `references/production-rules.md` before generating or editing any character-board assets.

## Output Variants

- **Codex deployment version**: Use this skill folder directly in Codex. Follow `SKILL.md` plus `references/production-rules.md`.
- **GPT agent version**: Use `gpt-agent/instructions.md` as the Chinese state router and upload the four ordered generation files plus the validation file in `gpt-agent/` as knowledge files.

## Default Workflow

1. Read the user's current references and text requirements.
2. Classify inputs:
   - face identity reference
   - outfit/reference clothing
   - hairstyle/reference accessories
   - style reference
   - user override requirements
3. Read `references/production-rules.md`.
4. Generate one new `master_front_full_body.png`.
5. Use the master image as the consistency anchor for:
   - `image_01_front_portrait.png`
   - `image_02_three_quarter_portrait.png`
   - `image_03_back_full_outfit.png`
6. Prefer cropping `image_04_front_outfit_detail.png` from the master image. Generate it separately only if the user asks or if local cropping is unavailable.
7. If the task is in Codex and local image processing is available, normalize/crop/stitch as requested. If the task is for a GPT agent, provide single-image workflow instructions and do not require local stitching.

## Core Rules

- Never return a user-uploaded reference image as a generated result.
- Never rename, crop, upscale, or lightly retouch a user reference to impersonate a generated output.
- Generate one image at a time.
- Do not create a 2x2 grid unless the user is in a Codex/local workflow and explicitly expects final stitching.
- Do not create character sheets, model sheets, turnaround sheets, labels, watermarks, borders, or text.
- The master image is a default single-generation anchor, not a repeated step. Regenerate it only when the user asks to modify, redo, replace, or adjust the master.
- After regenerating the master, base all later views on the new master only.

## Visual Defaults

- Realistic live-action cinematic quality.
- Neutral gray studio background by default.
- Switch to clean white studio background when the subject outfit, hair, accessories, or skin tone contains gray tones.
- Head close-ups: 1:1 square.
- Master/full-body/outfit-detail long views: vertical 9:16.
- Minimize empty background while preserving required body parts.
- Head close-ups include natural pores, fine lines, uneven light/shadow, subtle grain, dust/noise, and non-flat skin texture unless the user requests clean commercial lighting.

## Validation Checklist

Before final response, check:

- Each generated image is a real generated image, not a placeholder path.
- One character only.
- Correct view and aspect ratio for each step.
- Consistent identity, hairstyle, outfit, accessories, shoes, and proportions.
- Background follows the gray/white conditional rule.
- No text, logo, watermark, labels, borders, or multi-view sheet layout.
- If final stitching is performed, order is `1-2-4-3`: front portrait, three-quarter portrait, outfit detail, back full outfit.

## Final Response

Keep the final response concise. Include:

- generated image preview or saved paths
- output directory or artifact location, when applicable
- recommended stitch order
- simple character description prompt in the format defined in `references/production-rules.md`
