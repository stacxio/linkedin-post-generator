# Listicle / Framework Template

## Structure

```
[HOOK — the number + what you learned/built/discovered, framed as valuable]

[Brief context — why this list matters]

1. [Item] — [One-line explanation]
2. [Item] — [One-line explanation]
3. [Item] — [One-line explanation]
4. [Item] — [One-line explanation]
5. [Item] — [One-line explanation]

[Wrap-up — the meta-insight that ties them all together]

[CTA — ask what they'd add or which resonates most]

#hashtag1 #hashtag2 #hashtag3
```

## Example

```
5 n8n workflow patterns I use on every single project:

After building 50+ automation workflows, these are the patterns I never skip:

1. Error-first design — Every workflow starts with "what happens when this breaks?" before "what happens when this works?"

2. Idempotent triggers — If the same webhook fires twice, the workflow handles it gracefully. No duplicate records. No double-sends.

3. Notification layering — Critical failures go to PagerDuty. Warnings go to Slack. Info goes to a log. Not everything needs to wake someone up.

4. Test data nodes — A "mock input" node at the top of every workflow so I can test without triggering production APIs.

5. Version comments — Every node has a one-line comment explaining WHY it's there, not WHAT it does.

The common thread: Every pattern is about making the workflow survivable when you're not looking at it.

Which pattern would make the biggest difference in your current workflows?

#n8n #WorkflowAutomation #AutomationPatterns #stacx24
```

## Tips
- 3-7 items is the sweet spot (more than 7 and it's a blog post)
- Each item should stand alone — readers scan these
- The wrap-up insight is what elevates a list into a framework
- Numbers in the hook increase click-through on LinkedIn
