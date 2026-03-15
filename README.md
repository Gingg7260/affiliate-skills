# Affiliate Skills by Affitor

> AI-powered skills that take you from zero to first commission.

Open-source [Claude Skills](https://docs.anthropic.com/en/docs/claude-code/skills) for affiliate marketers. Each skill covers one stage of the affiliate funnel. Use them standalone or chain them together.

## The Affiliate Funnel

```
S1: Research      affiliate-program-search    Find and evaluate the best programs to promote
       |
       v
S2: Content       viral-post-writer           Write posts that drive clicks on any platform
       |
    +--+--+
    |     |
    v     v
S3: Blog          affiliate-blog-builder      SEO-optimized review and comparison articles
    |
    v
S4: Landing       landing-page-creator        High-converting pages, pure HTML/CSS
    |
    v
S5: Distribution  bio-link-deployer           Your own link-in-bio page, zero dependencies
```

## Skills

| Skill | Stage | Status | Description |
|-------|-------|--------|-------------|
| [affiliate-program-search](skills/affiliate-program-search/) | S1: Research | Shipped | Research and score affiliate programs from list.affitor.com |
| [viral-post-writer](skills/viral-post-writer/) | S2: Content | Planned | Write viral posts for LinkedIn, X, Reddit, Facebook |
| [affiliate-blog-builder](skills/affiliate-blog-builder/) | S3: Blog | Planned | SEO-optimized affiliate blog posts |
| [landing-page-creator](skills/landing-page-creator/) | S4: Landing | Planned | High-converting landing pages in HTML/CSS |
| [bio-link-deployer](skills/bio-link-deployer/) | S5: Distribution | Planned | Linktree alternative you own |

## Quick Start

**Option 1: Copy the skill file**

1. Open any skill folder (e.g., `skills/affiliate-program-search/`)
2. Copy the contents of `SKILL.md`
3. Save it as a skill in your Claude project

**Option 2: Install from list.affitor.com**

```bash
curl -s https://list.affitor.com/api/v1/skills/affiliate-program-search/raw > SKILL.md
```

**Option 3: Use directly**

Just ask Claude something like:

- "Find me the best AI video affiliate programs with recurring commission"
- "Write a LinkedIn post promoting HeyGen"
- "Create a review blog post comparing AI video tools"

## Entry Points

You don't have to start from S1. Jump in wherever you are:

- **Beginner:** S1 → S2 → S3 → S4 → S5 (full funnel)
- **Have a product already:** S2 (write content) or S3 (write a review)
- **Have content, need pages:** S4 (landing page) or S5 (bio link)

## Contributing

We welcome skills from the community. See [CONTRIBUTING.md](CONTRIBUTING.md) for how to submit your own skill.

Every merged skill gets published to [list.affitor.com/skills](https://list.affitor.com/skills).

## License

MIT

---

Built by [Affitor](https://affitor.com). Directory: [list.affitor.com](https://list.affitor.com)
