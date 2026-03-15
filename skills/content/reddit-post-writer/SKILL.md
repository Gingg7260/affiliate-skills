---
name: reddit-post-writer
description: >
  Write Reddit posts and comments that recommend affiliate products without getting
  flagged as spam. Use this skill when the user wants to promote on Reddit, write a
  Reddit post for affiliate, create subreddit-native content, draft a Reddit comment
  recommending a tool, write a "what tool do you use" response, or share a product
  recommendation on Reddit naturally.
---

# Reddit Post Writer

Write Reddit posts and comments that recommend affiliate products in a way that adds genuine value to the community. Reddit users hate ads — this skill creates content that helps first and recommends second.

## When to Use

- User wants to promote an affiliate product on Reddit
- User needs to answer a "what tool do you use for X?" post
- User wants to create a discussion post that naturally mentions their affiliate product
- User needs a genuine product review for a specific subreddit

## Workflow

1. **Identify the subreddit** — each subreddit has different rules, tone, and expectations. Research the subreddit's posting guidelines, common post types, and what gets upvoted vs downvoted.

2. **Choose the right post type:**
   - **Experience post:** "I switched from X to Y, here's what happened" (most effective)
   - **Question + answer:** "How do you handle X? I've been using Y and..." (engagement-driven)
   - **Resource list:** "Tools I use for X" (value post with product embedded)
   - **Comment reply:** Answer someone's question with a genuine recommendation

3. **Write the content:**
   - Lead with the problem or experience, NOT the product
   - Use Reddit's casual, first-person tone — never sound like marketing copy
   - Include specific details that prove you actually used the product
   - Mention at least one con or limitation (credibility)
   - If including a link, use the product's main URL, not an obvious affiliate link
   - Keep it conversational — contractions, informal language, occasional humor

4. **Reddit-specific rules:**
   - NO affiliate links directly in posts (most subreddits ban them)
   - Strategy: link to your blog post/landing page that contains the affiliate link
   - Or mention the product by name and let readers search for it
   - Always disclose if asked: "Yeah I have an affiliate link, happy to share if you want it"
   - Check subreddit rules for self-promotion limits (most allow 10% self-promo)

5. **Format for Reddit:**
   - Use Reddit markdown (double newline for paragraphs, `**bold**`, `- bullets`)
   - Break into short paragraphs (2-3 sentences max)
   - Use headers for long posts
   - TL;DR at the bottom for posts over 200 words

## Input Schema

```
{
  product: object           # (required) Product to recommend — name, features, pricing
  subreddit: string         # (optional) Target subreddit (e.g., "r/SaaS", "r/Blogging")
  post_type: string         # (optional, default: "experience") experience | question | resource_list | comment
  context: string           # (optional) Existing post/thread to reply to
  tone: string              # (optional, default: "casual") casual | technical | enthusiastic
}
```

## Output Schema

```
{
  title: string             # Post title (for new posts)
  body: string              # Post body in Reddit markdown
  subreddit: string         # Target subreddit
  post_type: string         # Type of post created
  disclosure_note: string   # How to handle affiliate disclosure if asked
}
```

## Output Format

Reddit-formatted post with title and body, ready to paste into Reddit's post editor.

## Error Handling

- If no subreddit specified, suggest 3 relevant subreddits based on the product category
- If product details are thin, use `web_search` to gather genuine feature info
- If the subreddit bans all product mentions, suggest alternative subreddits

## Examples

**Example 1:** "Write a Reddit post recommending Jasper AI for r/Blogging" → Experience post about switching from manual writing to Jasper, with specific before/after metrics, one limitation mentioned, and a link to "my full review" (which contains the affiliate link).

**Example 2:** "Reply to a Reddit thread asking about the best email marketing tools, recommend ConvertKit" → Helpful comment listing 3 tools tried, why ConvertKit won, specific feature that sealed the deal, casual tone with "feel free to DM me for my affiliate link if you want a discount."
