---
name: linkedin-post-generator
description: "LinkedIn post generator that builds authority for stacx24 — a product/service in n8n automation, full stack development, and AI trends. Use this skill whenever the user wants to create, draft, brainstorm, schedule, or publish LinkedIn posts, content calendars, thought leadership content, or social media copy for stacx24. Trigger when the user mentions 'LinkedIn', 'post', 'authority building', 'thought leadership', 'stacx24', or wants to create content about n8n, automation workflows, full stack development, or AI trends for LinkedIn. Even if the user just says 'write a post' or 'I need content', this skill should activate."
---

# LinkedIn Post Generator for stacx24

## Overview

This skill generates authority-building LinkedIn posts for **stacx24**, positioning it as the go-to voice in n8n automation, full stack development, and cutting-edge AI trends. Posts blend professional polish with bold, provocative takes that stop the scroll and spark engagement.

The skill leverages a structured workspace with dedicated folders for drafts, published posts, references, and templates — making it easy to iterate, maintain brand consistency, and build a content pipeline.

## Workspace Structure

The workspace uses four main folders alongside this skill. Every post flows through this pipeline:

```
linkedin-posts/
├── drafts/          → Work-in-progress posts (.md) — save here while iterating
├── published/       → Final approved posts (.md) — move here when ready to publish
├── references/      → Topic research, competitor analysis, audience insights (.md)
├── templates/       → Reusable post format templates (.md)
└── linkedin-post-generator/   → This skill
    ├── SKILL.md
    ├── references/  → Brand voice guide, topic pillars, hooks library
    └── scripts/     → Helper scripts
```

**Folder conventions:**
- All posts use `.md` format by default
- Filename pattern: `YYYY-MM-DD-topic-slug.md` (e.g., `2026-02-11-n8n-api-orchestration.md`)
- Other formats (HTML, DOCX) are fine when the user requests them
- The `references/` folder at the workspace root is for user-added research; the `references/` inside this skill folder holds permanent brand guidelines

## Brand Context: stacx24

Before generating any post, read `references/brand-voice.md` in this skill's folder for the full voice guide.

**Core identity**: stacx24 helps businesses and developers leverage n8n automation, full stack development practices, and emerging AI tools to ship faster and smarter.

**Authority pillars** (read `references/topic-pillars.md` for detailed content angles):

1. **n8n Automation** — workflow automation, integration patterns, no-code/low-code power moves, self-hosted automation
2. **Full Stack Development** — modern web architectures, developer productivity, shipping culture, framework opinions
3. **AI Trends** — practical AI implementation, LLM integrations, AI-powered workflows, what's hype vs. what ships

**Voice characteristics**:
- Professional but not corporate — think "sharp expert at a conference", not "quarterly earnings call"
- Bold enough to challenge conventional thinking — hot takes backed by evidence and experience
- Concrete and tactical — always give the reader something they can act on today
- Pattern-interrupting hooks — the first line must earn the second line

## Workflow

### Step 1: Understand the Request

When the user asks for a LinkedIn post, figure out:

1. **Topic**: Which pillar(s)? Check if the user uploaded anything to `../references/` for context.
2. **Format**: Which template fits? Review available templates in `../templates/`.
3. **Goal**: Awareness, engagement, lead generation, or pure thought leadership?
4. **Angle**: What's the bold take or unique insight that makes this post worth reading?

If the user is vague ("write me a LinkedIn post"), ask which topic pillar to focus on and what specific insight, experience, or opinion to highlight. Don't generate generic content — every post needs a sharp angle.

### Step 2: Draft the Post

1. Read the relevant template from `../templates/`
2. Read `references/brand-voice.md` to calibrate tone
3. Write the draft following these rules:

**Hook (Line 1-2)** — the most important part of any LinkedIn post:
- Must be pattern-interrupting: bold claim, contrarian take, surprising stat, or provocative question
- Keep under 150 characters so it shows fully in the feed without "...see more"
- Never open with generic starters like "I'm excited to share...", "Just had a great meeting...", "Happy to announce..."
- Test: Would YOU stop scrolling for this line?

**Body (Lines 3-15)**:
- Short paragraphs (1-3 sentences max) — LinkedIn is mobile-first
- Use line breaks liberally for scanability
- Include ONE concrete example, case study, or data point
- Build toward a clear insight or lesson
- Weave stacx24's expertise naturally — the post should demonstrate authority, not pitch a product
- Use "→" for bullet lists instead of standard bullets (reads better on LinkedIn)

**Closer (Last 2-3 lines)**:
- End with a question, challenge, or call to action that drives comments (not just likes)
- Include 3-5 relevant hashtags on a separate final line
- Hashtags should be specific and niche (e.g., #n8nAutomation, #FullStackDev) — avoid generic ones (#success, #motivation)

**Formatting rules**:
- Target length: 800-1300 characters (LinkedIn's sweet spot for engagement)
- Bold key phrases sparingly using **bold** notation (will need manual formatting on LinkedIn)
- No emojis unless the user specifically requests them
- Every paragraph should earn its place — cut anything that doesn't add value

### Step 3: Save and Iterate

1. Save the first draft to `../drafts/` as `YYYY-MM-DD-topic-slug.md`
2. Present the draft to the user with a brief note on the angle and format used
3. Iterate based on feedback — be receptive to tone adjustments
4. When the user approves, copy the final version to `../published/`

## Post Formats

Templates for each format live in `../templates/`. Read them for detailed structures. Here's when to use each:

### 1. Hot Take
Contrarian opinion that challenges industry norms. Opens with a bold statement, backs it up with evidence, lands on a nuanced conclusion. **Best for**: engagement, thought leadership, establishing stacx24 as an opinionated expert.

### 2. Tactical How-To
Step-by-step breakdown of something practical. "Here's exactly how to..." format with numbered steps. **Best for**: saves, shares, demonstrating deep technical expertise.

### 3. Story → Lesson
Personal or client experience that extracts a universal insight. Narrative arc: situation → tension → resolution → takeaway. **Best for**: human connection, relatability, showing real-world results.

### 4. Listicle / Framework
"X things I learned about Y" or "The Z framework for W". Scannable, high-value, easy to bookmark. **Best for**: reach, saves, positioning stacx24 as a systematizer.

### 5. Industry Trend Analysis
Commentary on what's happening in n8n/automation, full stack, or AI. Takes a position on where things are heading. **Best for**: authority building, positioning stacx24 as tuned-in to the cutting edge.

## Content Calendar Mode

When the user asks for a content calendar or batch of posts, plan a balanced mix across the week:

- **40%** Hot Takes & Trend Analysis (authority building)
- **30%** Tactical How-Tos (practical value)
- **20%** Story → Lesson (human connection)
- **10%** Listicle / Framework (shareability)

Space topics across all three pillars so the feed doesn't feel one-dimensional. A good weekly rhythm might look like:

- **Monday**: Hot Take (gets the week started with engagement)
- **Wednesday**: Tactical How-To (mid-week value bomb)
- **Friday**: Story or Trend Analysis (reflection/forward-looking to close the week)

Save each planned post as a separate file in `../drafts/` with the target date in the filename.

## Quality Checklist

Before presenting any post to the user, verify every item:

- Hook stops the scroll — would you genuinely pause for this line?
- Body delivers on the hook's promise — no bait-and-switch
- One clear, actionable takeaway the reader can use today
- stacx24 expertise woven in naturally, not as a sales pitch
- Length is 800-1300 characters
- Closer drives engagement with a question or challenge
- Hashtags are relevant and specific to the niche
- Tone matches brand voice: professional + provocative
- No filler paragraphs — every line earns its spot
- Filename follows the `YYYY-MM-DD-topic-slug.md` convention

## Handling Edge Cases

- **User provides raw notes or bullet points**: Transform them into a polished post while preserving their core insights. Don't invent claims they didn't make.
- **User wants to repurpose content**: Adapt blog posts, presentations, or docs into LinkedIn-native format. Strip the corporate tone, add a hook, tighten everything.
- **User wants a carousel or visual post**: Draft the text content for each slide/frame, noting where visuals should go. Save as a special template in `../drafts/`.
- **Multiple posts at once**: Create each as a separate file in `../drafts/`, present a summary list to the user.
- **User uploads reference material**: Check `../references/` for any user-added files and incorporate those insights into the post.
