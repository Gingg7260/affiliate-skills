# Contributing to Affiliate Skills

Thanks for contributing! This guide explains how to add your own skill to the collection.

## How Skills Are Organized

Every skill belongs to one of five funnel stages:

| Stage | Focus | Example Skills |
|-------|-------|---------------|
| S1: Research | Find and evaluate programs | `affiliate-program-search`, `crypto-affiliate-scanner` |
| S2: Content | Create promotional content | `viral-post-writer`, `tiktok-script-writer`, `email-sequence-builder` |
| S3: Blog | Write SEO articles | `affiliate-blog-builder`, `youtube-script-writer` |
| S4: Landing | Build conversion pages | `landing-page-creator`, `webinar-registration-page` |
| S5: Distribution | Deploy and distribute | `bio-link-deployer`, `github-pages-deployer` |

Pick a stage, build a skill.

## Creating a New Skill

### 1. Fork and clone

```bash
git clone https://github.com/affitor/affiliate-skills.git
cd affiliate-skills
```

### 2. Scaffold your skill

Use the template:

```bash
cp SKILL_TEMPLATE.md skills/your-skill-name/SKILL.md
mkdir -p skills/your-skill-name/references
```

Naming convention: `kebab-case`, `verb-noun` format (e.g., `viral-post-writer`, `affiliate-blog-builder`).

### 3. Write your skill

Fill in `SKILL.md` with:

- **Frontmatter:** name and a pushy description (cover multiple trigger phrases)
- **Input Schema:** what the skill needs (required vs optional fields)
- **Workflow:** step-by-step what the skill does
- **Output Schema:** structured output for agent chaining
- **Output Format:** human-readable output (tables, markdown, HTML)
- **Error Handling:** what to do when things go wrong
- **Examples:** at least 2 realistic prompts with expected output summaries

If any reference content exceeds 50 lines, put it in `references/` as a separate file.

### 4. Test your skill

Run these three tests:

1. **Stranger test:** Someone who's never heard of Affitor types a natural prompt. Does the output make sense?
2. **Chain test:** Paste the output into a new conversation. Can the next skill in the funnel understand it?
3. **Platform test:** Copy the output outside Claude. Does it work? (Post to X, deploy to Vercel, paste into WordPress)

### 5. Submit a PR

- Create your skill in `skills/[skill-name]/`
- Include: `SKILL.md` + `references/` + 3 test prompts in PR description
- PR description: which stage, what it does, test results

## Quality Checklist

Before submitting, verify:

- [ ] `SKILL.md` has frontmatter with `name` and `description`
- [ ] Description is pushy — covers 5+ trigger phrases
- [ ] At least 2 examples with realistic prompts
- [ ] References in separate files if >50 lines
- [ ] Output is portable (user can use it immediately outside Claude)
- [ ] Includes affiliate disclosure guidance
- [ ] Works standalone (no dependency on other skills)
- [ ] Works in chain (picks up context from conversation if available)
- [ ] Input Schema and Output Schema defined
- [ ] Error handling covers common failure modes
- [ ] Tested with 3 different prompts

## After Merge

Your skill will be automatically published to [list.affitor.com/skills](https://list.affitor.com/skills) via CI. You'll be credited as the author.

## Questions?

Open an issue or reach out on [list.affitor.com](https://list.affitor.com).
