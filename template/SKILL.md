---
name: your-skill-name
description: >
  Replace with when the AI should activate this skill. Be pushy — cover multiple
  phrasings so the AI activates for a wide range of user prompts.
license: MIT
metadata:
  author: your-github-handle
  version: "1.0"
  stage: SX-StageName
---

# Your Skill Name

What this skill does in 2-3 sentences. Focus on the outcome, not the process.

## Stage

This skill belongs to Stage SX: StageName

## When to Use

- Scenario 1
- Scenario 2
- Scenario 3

## Input Schema

```
{
  required_field: {          # (required) Description
    name: string             # Example value
  }
  optional_field: string     # (optional, default: "value") Description
}
```

## Workflow

### Step 1: Gather Context

What to check first. How to handle missing inputs.

### Step 2: Execute Core Task

The main work the skill does.

### Step 3: Format and Deliver

How to structure the output.

## Output Schema

Other skills can consume these fields from conversation context:

```
{
  primary_output: string     # Main result for downstream chaining
  secondary_output: string   # Additional data for downstream skills
}
```

## Output Format

```
## [Skill Name]: [Context]

### Section 1
[Main content]

### Section 2
[Supporting content]
```

## Error Handling

- **Missing required input:** How to recover gracefully.
- **External data unavailable:** Fallback strategy.
- **Edge case:** How to handle unexpected scenarios.

## Examples

**Example 1:** [realistic user prompt]
→ [step-by-step what the skill does]
→ [expected output summary]

**Example 2:** [different scenario]
→ [step-by-step]
→ [expected output summary]

**Example 3:** [edge case or beginner scenario]
→ [step-by-step]
→ [expected output summary]

## References

- `references/your-reference.md` — description of what it contains
- `shared/references/ftc-compliance.md` — FTC disclosure requirements
- `shared/references/affitor-branding.md` — branding rules
