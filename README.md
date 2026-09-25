# Wleefa content skill

One skill for every piece of Wleefa copy: landing pages, blog, social posts, emails, newsletters, tutor-facing content. It carries the Wleefa Content Writer Guide (voice, terms, channel rules, approved examples) and the no-ai-slop writing rules, so a writer or an AI tool runs one command and gets both.

Source of truth for the brand rules is the Wleefa Content Writer Guide deck (Google Slides, v1.0, September 2026). When the deck changes, update `skills/wleefa-content/SKILL.md` and `examples.md` and bump the version in `.claude-plugin/plugin.json`.

## Install in Claude Code

Add the marketplace once, then install the plugin:

```bash
claude plugin marketplace add AAA-codes/wleefa-content-skill
claude plugin install wleefa-content@wleefa
```

Update later with:

```bash
claude plugin update wleefa-content@wleefa
```

Inside a session, `/wleefa-content` invokes it. Claude also picks it up on its own when a request mentions Wleefa copy.

## Use in claude.ai

Writers on claude.ai cannot pull from GitHub. Upload the `skills/wleefa-content` folder as a skill in claude.ai (Settings, Capabilities, Skills), and re-upload it whenever this repo changes.

## What is inside

| File | Purpose |
|---|---|
| `skills/wleefa-content/SKILL.md` | The rules: what Wleefa is, voice, terms, channels, workflow |
| `skills/wleefa-content/examples.md` | Approved avoid/use pairs for every channel |
| `skills/wleefa-content/writing-quality.md` | The no-ai-slop rules, applied after the brand rules |
| `skills/wleefa-content/eval.md` | The checklist every draft passes before it is returned |

## How to use it

Give the skill three things: the channel, the audience category, and what the reader should do afterwards. Then either ask for new copy, paste a draft to edit, or paste a draft to check. Every result ends with a reminder that a human must approve the content before it is published.

Owner: Abdulrahman Javaid. Approval: the marketing lead.
