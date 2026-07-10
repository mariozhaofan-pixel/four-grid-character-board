# Four Grid Character Board

High-consistency character reference board workflow for image-generation agents.

## Copyright And Use Restrictions

Copyright (c) 2026 MARIOZHAOFAN. All rights reserved.

This repository is public for review and personal, non-commercial local use
only. It is not licensed for unrestricted open-source redistribution.

Without prior written permission, you may not republish, mirror, re-upload,
redistribute, sell, sublicense, package, or commercially use this repository or
derivative versions of it.

Commercial use, redistribution, republishing, sublicensing, marketplace uploads,
client work, paid workflow packaging, SaaS use, or derivative publication
requires explicit permission.

Contact for permission:

```text
WeChat: MARIOZHAOFAN
```

This repository contains two deployment variants:

- `codex-skill/`: Codex Skill deployment version.
- `gpt-agent/`: GPT agent Instructions / knowledge-file version.

The workflow is designed for single-character reference sets:

1. Generate one master front full-body image.
2. Generate a front portrait from the master.
3. Generate a three-quarter portrait from the master.
4. Generate a back full-outfit view from the master.
5. Crop or generate a front outfit-detail view.
6. Let the user assemble the final 2x2 board.

## Key Defaults

- Realistic live-action cinematic quality.
- One generated image per step.
- User reference images are inputs only, never outputs.
- Head close-ups use `1:1`.
- Master, full-body, and outfit-detail long views use vertical `9:16`.
- Neutral gray studio background by default.
- Switch to white studio background when the subject has gray-toned outfit, hair, accessories, or skin.
- No text, labels, watermarks, logos, borders, model sheets, or 2x2 grid generation by default.

## Codex Skill Deployment

Copy or symlink this folder into your Codex skills directory:

```text
codex-skill/four-grid-character-board
```

Example target locations:

```text
~/.codex/skills/four-grid-character-board
%USERPROFILE%\.codex\skills\four-grid-character-board
```

The skill entrypoint is:

```text
codex-skill/four-grid-character-board/SKILL.md
```

The full production rules live in:

```text
codex-skill/four-grid-character-board/references/production-rules.md
```

## GPT Agent Deployment

Use these files when configuring a GPT agent:

```text
gpt-agent/instructions.md
gpt-agent/four-grid-character-board-creation.md
```

Recommended setup:

1. Paste `gpt-agent/instructions.md` into the GPT Instructions field.
2. Upload `gpt-agent/four-grid-character-board-creation.md` as a knowledge file, or paste it after the Instructions if your GPT setup does not support files.
3. Enable image generation and image upload / vision capabilities.

## License

Restricted license. See `LICENSE`.
