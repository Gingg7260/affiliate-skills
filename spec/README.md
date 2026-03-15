# Agent Skills Specification

This repo follows the [Agent Skills open standard](https://agentskills.io) as defined by the [anthropics/skills](https://github.com/anthropics/skills) repository.

## Required Frontmatter

Every `SKILL.md` must have:

```yaml
---
name: lowercase-with-hyphens
description: >
  When Claude should use this skill. Write in natural language,
  cover multiple trigger phrases.
---
```

## Skill Folder Structure

```
skills/{stage}/{skill-name}/
├── SKILL.md              (required)
├── LICENSE.txt            (required — MIT or Apache 2.0)
├── agents/
│   └── openai.yaml       (optional — cross-platform compatibility)
├── references/            (optional — supplementary docs)
├── templates/             (optional — HTML/asset templates)
├── scripts/               (optional — helper scripts)
└── examples/              (optional — example inputs/outputs)
```

## Stages

Skills are organized by affiliate funnel stage:

| Stage | Directory | Purpose |
|---|---|---|
| S1 | `skills/research/` | Find and evaluate programs |
| S2 | `skills/content/` | Create social media content |
| S3 | `skills/blog/` | Write SEO articles |
| S4 | `skills/landing/` | Build conversion pages |
| S5 | `skills/distribution/` | Deploy and distribute |

## References

- [Agent Skills Spec](https://agentskills.io)
- [anthropics/skills](https://github.com/anthropics/skills/blob/main/spec/agent-skills-spec.md)
- [Equipping agents for the real world](https://www.anthropic.com/engineering/agent-skills) — Anthropic engineering blog
