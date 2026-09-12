# Zhuoqu Cinema · 拙趣映画

[简体中文](README.md) | **English**

Turn cinematic moods and everyday scenes into hand-painted illustrations with textured paper, generous negative space, and a little endearing awkwardness.

“Zhuoqu” (拙趣) describes the charm of deliberate imperfection: uneven lines, slightly awkward poses, and simple forms arranged with care.

This reusable image-generation skill is not tied to GPT or a particular provider. It adapts to the available tool: generate an image directly, prepare a standard prompt, or provide a shorter prompt for models that struggle with detailed instructions.

## Visual style

- **Paper and brush texture:** warm-white fibrous paper, dry gouache, crayon marks, broken lines, and natural gaps in the paint.
- **Restrained color and composition:** a few muted colors with one small accent; a default 3:4 portrait layout that can be changed.
- **Natural proportions:** simple faces and slightly hesitant poses, without exaggerated body lengths or height differences.
- **Cinematic storytelling:** a few concrete scene cues and character relationships convey the mood of a film, series, or everyday moment.
- **Focused edits:** change the requested detail while preserving the accepted composition, palette, and texture as far as the tool allows.

HEYTEA-inspired aesthetics are a visual reference only. The skill does not add tea cups, packaging, logos, or advertising copy by default. This project is not officially affiliated with HEYTEA or the referenced film and television works.

## Getting started

Import this repository into an AI tool that supports custom skills, or place the skill files in that tool’s designated skills directory. If your tool does not support skills, copy a prompt directly instead.

The repository is public: you can browse, download, or clone it without private-repository access authorization.

For a local Codex setup:

```bash
git clone https://github.com/734511533-del/zhuoqu-cinema.git ~/.codex/skills/zhuoqu-cinema
```

For other tools, use their supported import method. The repository provides instructions and prompts, not a standalone image model or API service. Actual image generation requires an image-capable tool.

Once installed, try:

> Use $zhuoqu-cinema to create a hand-painted illustration inspired by the seaside encounter in Goblin. Keep the red scarf and winter sea, with no text.

> Use Zhuoqu Cinema to illustrate someone waiting for a bus on a rainy day. Use grey-green and ivory, with a quiet touch of humor.

> Everything else looks good. Only reduce the height difference between the two people, keeping the composition and brushwork.

You can specify a landscape layout, cover format, subject placement, accent color, or details to preserve. The default is one image. Text-only tools can prepare a reusable prompt instead.

## Working across models

The core instructions are self-contained in [SKILL.md](SKILL.md), currently written in Chinese. This English introduction includes a ready-to-use English prompt below.

`agents/openai.yaml` is optional interface metadata for hosts that recognize that format. Other tools can ignore it. Reading or using the prompts does not require an OpenAI account.

| Available capability | How to use the skill |
| --- | --- |
| Skill loading and image generation | Load the skill and follow the host tool’s calling conventions |
| Prompt input only | Paste a standard or simplified prompt; no skill invocation syntax is needed |
| Frequently missed details or unknown instruction-following ability | Start with the simplified prompt; establish subjects, composition, and color before adding texture |
| Text generation only | Prepare the prompt, then pass it to an image-generation tool |
| No reference-image or local-edit support | Treat changes as redraws; unchanged details cannot be guaranteed |

### Ready-to-use simplified prompt

> Two adults facing each other beside a muted blue-grey sea. One wears a black coat, the other an ivory coat and a red scarf. Similar heights and natural adult proportions. Small figures in the lower part of the image, a large blank warm-white paper area above. Rough dry gouache brushwork, few colors, simple faces. No text or logos.

Replace the subjects, setting, and colors to explore other themes. Prefer short sentences, one language, and concrete spatial descriptions. The default prompts do not depend on exact numeric ratios, weighting syntax, seeds, or provider-specific parameters. Choose a workflow based on observed capabilities, not a model’s brand or country of origin.

### Consistency and limitations

The skill aims to reduce drift through fixed visual priorities, simpler prompts, and one-at-a-time corrections. Image quality, composition accuracy, and editing fidelity still vary across models; identical results are not guaranteed.

The instruction structure and text handoff paths have been checked. Comparative image-generation tests across multiple platforms have not yet been completed.

## Repository files

| File | Purpose |
| --- | --- |
| [SKILL.md](SKILL.md) | Core visual rules, generation workflow, editing guidance, and prompt templates |
| [agents/openai.yaml](agents/openai.yaml) | Display name, description, and default invocation for compatible hosts |
| [assets/icon.svg](assets/icon.svg) | Skill icon |
| [README.md](README.md) | Chinese introduction |
| [README.en.md](README.en.md) | English introduction |

## Where it started

The approach grew from an iterative Goblin-inspired illustration: moving from a branded product photograph to naive hand painting on warm-white paper, then correcting an exaggerated height difference between the characters. The skill preserves those reusable visual and editing principles while allowing the setting to change.
