---
name: [skill-name]
description: >
  [When to trigger. Be pushy. Cover multiple phrasings so Claude activates this skill
  for a wide range of user prompts. Include 5+ trigger phrases.]
---

# [Skill Name]

[What this skill does in 2-3 sentences.]

## Stage

This skill belongs to Stage [S1-S5]: [Research/Content/Blog/Landing/Distribution]

## When to Use

[Specific scenarios and trigger phrases]

## Input Schema

What this skill needs to run. Fields marked (required) must be provided or inferred from conversation context. Fields marked (optional) have sensible defaults.

```
{
  field_name: type        # (required) Description
  field_name: type        # (optional, default: X) Description
}
```

## Workflow

[Step-by-step what the skill does]

## Output Schema

Structured output this skill produces. Other skills in the chain can consume these fields from conversation context.

```
{
  field_name: type        # Description
}
```

## Output Format

[Human-readable output the user receives — tables, markdown, HTML, etc.]

## Error Handling

- [What to do when data source is unavailable]
- [What to do when required input is missing]
- [Fallback behavior]

## Examples

**Example 1:** [realistic user prompt → expected output summary]

**Example 2:** [different scenario]

## References

- `references/[file].md` - [when to read this file]
