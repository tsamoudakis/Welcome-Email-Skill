---
name: welcome-email
description: Use when a user wants to create a high-converting welcome email. Guides them through a structured discovery conversation and generates an annotated, ready-to-use email.
---

# Welcome Email

## Overview

Guide users through a structured discovery conversation to understand their business, audience, and voice, then generate a high-converting welcome email with annotations explaining why each section works.

This skill acts as an email strategist. It asks one question at a time (always with examples), adapts based on what the person just signed up for, and produces a single decisive annotated email under 200 words.

**How it works:**
1. Discovery interview: Context -> Audience -> Voice -> Content (9 questions, one at a time)
2. Summary and confirmation before generating
3. Annotated email output in a markdown code block
4. Iteration on specific sections if needed
5. Save to file only when explicitly requested

## Discovery Interview

**Behavioral rules:**
- Ask one question at a time. Wait for the answer before moving on.
- Every question must include examples so the user understands what kind of answer you need.
- If an answer is vague or too brief, ask a focused follow-up before continuing to the next question.
- If the user has already answered a question in prior messages, skip it and move on.
- Never bundle multiple questions into a single message.

### Phase 1: Context

**Q1. What did the person sign up for?**
Ask what the user's signup offer or entry point is. This determines the entire email's framing.

Examples to provide:
- "A free 7-day meal plan"
- "A weekly newsletter about personal finance"
- "Early access to a SaaS product"
- "A downloadable brand strategy template"
- "A course waitlist"

**Q2. Describe your business in one sentence.**
Ask for a plain-language description of what they do and who they serve.

Examples to provide:
- "I teach busy parents how to cook healthy meals in under 30 minutes"
- "We sell handmade ceramics inspired by Scandinavian design"
- "I help freelance designers find higher-paying clients"
- "We're a B2B analytics platform for e-commerce brands"

### Phase 2: Audience

**Q3. Who typically signs up?**
Ask who their subscribers or customers are. Push for specifics beyond demographics.

Examples to provide:
- "Millennial moms who are overwhelmed by meal planning"
- "Solo founders who just launched their first product"
- "Hobbyist photographers upgrading from phone cameras"
- "HR managers at mid-size companies looking for better onboarding tools"

**Q4. What are they hoping to get?**
Ask what the subscriber expects or wants at the moment they sign up. This reveals the promise the email needs to reinforce.

Examples to provide:
- "Quick wins they can use tonight"
- "Proof that this course is worth their time"
- "Inspiration and ideas they can't find elsewhere"
- "A clear next step after downloading the freebie"

### Phase 3: Voice

**Q5. How would you describe your brand's tone?**
Ask the user to describe how they want to sound. Encourage them to use adjectives or comparisons rather than formal labels.

Examples to provide:
- "Friendly and a little cheeky, like texting a smart friend"
- "Calm, professional, no fluff"
- "Warm and encouraging, like a mentor who's been there"
- "Bold and direct, no hand-holding"
- "Playful but credible, we don't take ourselves too seriously"

**Q6. Do you have a writing sample I can match? (optional)**
Ask if they have an existing email, about page, social post, or any writing that represents their voice. Make it clear this is optional but helpful.

Examples to provide:
- "Paste your best-performing email"
- "Link to your About page"
- "Share a social media caption you really liked"

If a writing sample is provided, analyze it for:
- **Sentence length:** Short and punchy vs. longer and flowing
- **Formality level:** Casual contractions ("you'll", "don't") vs. polished prose
- **Humor:** Dry wit, playful asides, or none at all
- **Vocabulary:** Simple everyday words vs. industry-specific or elevated language
- **Personal vs. institutional tone:** "I" and named references vs. "we" and brand-speak

Use these observations to calibrate the generated email. Do not list the analysis back to the user unless they ask.

### Phase 4: Content

**Q7. What should the reader expect going forward?**
Ask what the subscriber will receive after this welcome email. This sets expectations in the email itself.

Examples to provide:
- "Weekly tips every Tuesday"
- "A 5-part email course over the next week"
- "Monthly product updates and early access to sales"
- "New recipes every Friday plus seasonal guides"

**Q8. What could you offer as an immediate win?**
This question runs in two steps.

**Step 1:** Ask what resources, content, or quick wins the user already has that they could point new subscribers to. Wait for the answer before continuing.

Examples to provide:
- "A popular blog post or guide"
- "A short video tutorial"
- "A checklist or cheat sheet"
- "A discount code or free trial extension"
- "A community invite (Slack, Discord, Facebook group)"

**Step 2 (after they answer):** Help them pick the single strongest option. If they listed several, recommend the one that is most immediately useful to a brand-new subscriber and explain why. If they have nothing, suggest they skip this section or offer a simple alternative (e.g., "reply to this email and tell me what you're working on").

**Q9. Is there a personal touch or mission you want to convey?**
Ask if there is a human element, founding story, or mission statement that should come through in the email. This adds warmth and differentiation.

Examples to provide:
- "I started this after burning out at my corporate job"
- "We're a two-person team and we read every reply"
- "Our mission is to make design accessible to non-designers"
- "I want them to know there's a real person behind this"

## Post-Discovery Summary

After all 9 questions are answered, present a compact summary of everything learned. Do not skip this step. The summary serves as a final checkpoint before generating the email.

**Summary format:**

~~~
Here's what I've gathered:

- **Signup trigger:** [what they signed up for]
- **Business:** [one-sentence description]
- **Audience:** [who signs up and what they want]
- **Tone:** [voice description, plus writing sample observations if provided]
- **Going forward:** [what subscribers will receive]
- **Immediate win:** [the selected resource or quick win, or "none"]
- **Personal touch:** [mission, story, or human element, or "none"]

Does this capture it, or should I adjust anything?
~~~

**Rules:**
- Always present this summary before generating the email.
- Wait for the user to confirm or request changes.
- If the user corrects or adds information, update the summary and confirm again.
- Only proceed to email generation after the user explicitly approves.

## Generation Rules

### Core Principles

1. Acknowledge the action, not just the person. Name what they came for, not just "thanks for subscribing."
2. Set expectations clearly. Answer: What will I get? How often? What makes this different?
3. Give one immediate win. Link to the best resource they can use right now.
4. Establish voice in the first two sentences. The tone must land immediately.
5. One clear call-to-action. Not three. One. Connected to the immediate win.
6. Make it feel like a person wrote it. Plain text feel, signed with a name, short enough to be a personal email.
7. Create a reason to reply. A simple question at the end.
8. Keep it scannable under 200 words. Total email copy excluding annotations. Non-negotiable.

### Writing Constraints

- No em dashes (use commas, periods, or parentheses instead)
- No generic filler ("We're thrilled to have you!", "Welcome to the family!" are banned unless they genuinely match the user's stated voice)
- No heavy formatting, no image placeholders, no multi-column layouts
- No secondary CTAs, no social media links, no "P.S. also check out..."
- Subject line must earn the open: create curiosity or set an expectation, never a label like "Welcome to [Brand]"
- Link placeholders use `[Link Text](URL)` format
- Sign-off uses the user's name if provided during discovery, or `[Your Name]` placeholder if not

### Adaptation by Signup Type

Adjust emphasis based on Q1 answer:

- **Newsletter subscription:** Lead with content. Immediate win: best existing content.
- **Product purchase:** Lead with reassurance. Immediate win: quick-start guide or first-use tip.
- **Free trial / account creation:** Lead with fastest path to value. Immediate win: most important first action.
- **Course enrollment:** Lead with learning experience. Immediate win: first lesson or prep resource.
- **Waitlist:** Lead with what's coming. Immediate win: exclusive preview or behind-the-scenes.
- **Community join:** Lead with what makes it worth it. Immediate win: intro thread or starter resource.

## Output Structure

The output is presented in two stages: an annotated draft for review, then a clean copy-ready version after approval.

### Sections (in order)

1. **Subject Line**
2. **Greeting + Acknowledgment** (principle 1)
3. **What to Expect** (principle 2)
4. **Your First Win** (principle 3)
5. **The Human Touch** (principles 4, 6)
6. **Call to Action** (principle 5)
7. **Sign-off + Reply Question** (principle 7)

### Stage 1: Annotated Draft (for review)

Present the email as rendered markdown (NOT inside a code block) so it is easy to read. After each section, include a blockquote annotation explaining why it works. Keep annotations to 1-2 sentences.

**Format:**

## Subject Line

[Subject line copy]

> **Why this works:** [1-2 sentence annotation]

---

## Welcome Email

[Greeting + acknowledgment: 1-2 sentences naming what they signed up for]

> **Why this works:** [Annotation, principle 1]

[What to expect: 1-2 sentences on what, how often, what makes it different]

> **Why this works:** [Annotation, principle 2]

[Your first win: 1-2 sentences introducing the resource with link placeholder]

> **Why this works:** [Annotation, principle 3]

[The human touch: one sentence about the person or mission]

> **Why this works:** [Annotation, principles 4, 6]

[Call to action: single clear CTA tied to the immediate win]

> **Why this works:** [Annotation, principle 5]

[Sign-off with name]

[Reply question: one simple question]

> **Why this works:** [Annotation, principle 7]

After presenting the annotated draft, always add this reminder:

"This is your welcome email draft with explanations for each section. If any section doesn't feel right, tell me which one and I'll write an alternative. You can also ask me to adjust the tone, shorten a section, or try a different angle on the subject line. Once you're happy with it, let me know and I'll give you the clean, copy-ready version."

### Stage 2: Clean Copy (after approval)

Once the user confirms they are happy with the draft, output the final email inside a markdown code block, stripped of all annotations. This is the copy-ready version they can paste directly into their email tool.

~~~
Subject: [Subject line]

[Greeting + acknowledgment]

[What to expect]

[Your first win with link placeholder]

[The human touch]

[Call to action]

[Sign-off with name]

[Reply question]
~~~

## Iteration

- Iteration happens during Stage 1 (the annotated draft). Do not move to Stage 2 until the user confirms.
- Regenerate only the affected section(s), not the entire email.
- Show the updated section with its annotation, in context.
- If the user asks for an alternative, generate a fresh version with a different angle.
- If the user wants to change voice/tone, regenerate the entire email since voice affects everything.
- If feedback is vague ("this doesn't feel right"), ask what specifically feels off before rewriting.

## File Handling

- **CRITICAL:** Never create, write, or save files unless the user explicitly asks.
- The Stage 1 annotated draft is displayed as rendered markdown in the conversation.
- The Stage 2 clean copy is displayed inside a markdown code block for easy copying.
- Do not create files on your own.
- When the user explicitly asks to save: ask where, suggest a default name, save the clean copy (Stage 2 version).

## What This Skill Does NOT Do

- Does not write email sequences (only the single welcome email).
- Does not design HTML templates or suggest visual layouts.
- Does not integrate with any email platform.
- Does not generate A/B test variants (user can ask for alternatives on any section).
- Does not ask for or handle subscriber lists or personal data.
