---
name: webinar-registration-page
description: >
  Build a webinar or event registration page as self-contained HTML. Use this skill
  when the user wants to create a webinar page, build an event registration page,
  make a workshop signup page, create a live demo registration, build a masterclass
  landing page, or design a free training signup page with countdown timer.
---

# Webinar Registration Page

Build a webinar/event registration page as a single self-contained HTML file. Includes countdown timer, speaker bio, agenda/what you'll learn, social proof, and a registration form that captures leads.

## When to Use

- User wants to host a webinar that promotes affiliate products
- User needs a registration page for a live demo or workshop
- User wants to build an email list through a free training offer
- User needs an event page with countdown timer and signup form

## Workflow

1. **Define the event:**
   - Title (benefit-focused: "How to X in Y minutes" format)
   - Date and time (with timezone)
   - Duration (typically 45-60 min)
   - What attendees will learn (3-5 bullet points)
   - Speaker name, title, and brief bio

2. **Structure the page:**
   - **Hero section:** Event title, date/time, countdown timer, primary CTA
   - **What you'll learn:** 3-5 specific takeaways with checkmark icons
   - **Speaker bio:** Photo placeholder, name, credentials, social proof
   - **Agenda:** Timeline of what happens during the event
   - **Social proof:** "X people registered", past event testimonials
   - **Registration form:** Name + email (keep it simple)
   - **FAQ:** Common questions (Is it free? Will there be a replay? What do I need?)

3. **Build the countdown timer:**
   - JavaScript countdown to event date
   - Shows days, hours, minutes, seconds
   - After event passes, show "Watch the replay" instead

4. **Registration form strategy:**
   - Only collect name + email (fewer fields = higher conversion)
   - Form submits to user's email service (Mailchimp, ConvertKit, etc.)
   - Or use a simple `mailto:` fallback if no email service
   - Show "You're registered!" confirmation message after submit
   - Add registrant to email sequence that promotes the affiliate product

5. **Build as single HTML file:**
   - All CSS inline, all JS inline — zero external dependencies
   - Mobile-responsive (most registrations happen on phone)
   - Fast-loading (no images by default, use CSS gradients and emojis)
   - Professional color scheme (blues/purples work best for webinars)
   - FTC disclosure if affiliate product will be pitched during webinar

6. **Affiliate integration:**
   - The webinar itself pitches the affiliate product
   - Registration page mentions "we'll show you the tool we use" (curiosity)
   - Thank-you/confirmation page can include early-bird affiliate link
   - Follow-up email sequence drives to affiliate offer

## Input Schema

```
{
  title: string             # (required) Webinar title
  date: string              # (required) Event date/time with timezone
  speaker: object           # (required) name, title, bio
  learning_points: array    # (required) 3-5 things attendees will learn
  duration: string          # (optional, default: "60 minutes")
  product: object           # (optional) Affiliate product to be pitched
  form_action: string       # (optional) Form submission URL
  theme: string             # (optional, default: "professional") professional | bold | minimal
}
```

## Output Schema

```
{
  html_file: string         # Complete HTML file content
  page_title: string        # SEO title
  email_subject_lines: array # 3 subject lines for promotion emails
  follow_up_sequence: array # Suggested email sequence outline
}
```

## Output Format

Single self-contained HTML file with working countdown timer and registration form. User saves as `index.html` and deploys.

Also outputs 3 email subject lines to promote the webinar and a brief follow-up sequence outline.

## Error Handling

- If no date specified, use "Coming soon" with email signup for notifications
- If no speaker info, create a generic "Your Host" section with placeholder
- If no form_action URL, use a client-side form that shows confirmation and stores data in localStorage (with instructions to connect a real email service)

## Examples

**Example 1:** "Create a webinar registration page for 'How to Make $500/month with AI Affiliate Marketing' on March 25th" → Full HTML page with countdown to March 25, 5 learning points, speaker section, registration form, and "500+ people registered" social proof.

**Example 2:** "Build a workshop signup page for a live demo of Jasper AI" → Registration page with product-focused agenda, "See Jasper in action" value props, speaker bio, countdown timer, and early-bird discount mention.
