# Wleefa skills

Claude Code skills for the Wleefa team. Each skill is a folder at the root of this repo and installs as its own plugin from the `wleefa` marketplace.

| Folder | Plugin | What it does |
|---|---|---|
| `content-skill` | `content-skill@wleefa` | Write, edit, or audit Wleefa copy in the Wleefa voice, with the no-ai-slop writing rules built in |

## Install in Claude Code

Add the marketplace once:

```bash
claude plugin marketplace add AAA-codes/wleefa-skills
```

Install a skill:

```bash
claude plugin install content-skill@wleefa
```

Update later:

```bash
claude plugin update content-skill@wleefa
```

## Use in claude.ai

Writers on claude.ai cannot pull from GitHub. Upload the skill's `SKILL.md` (for content, `content-skill/skills/wleefa-content/SKILL.md`) as a skill in claude.ai under Settings, Capabilities, Skills, and re-upload it when the repo changes.

## Content skill

`content-skill/skills/wleefa-content/SKILL.md` holds what Wleefa is, the voice, terms, channel rules, approved examples, the no-ai-slop writing rules, and the check every draft passes before it is returned. In a session, `/wleefa-content` invokes it, and Claude also picks it up when a request mentions Wleefa copy.

Give it three things: the channel, the audience category, and what the reader should do afterwards. Then ask for new copy, paste a draft to edit, or paste a draft to check. Every result ends with a reminder that a human must approve the content before it is published.

The source of truth for the brand rules is the Wleefa Content Writer Guide deck (Google Slides, v1.0, September 2026). When the deck changes, update the SKILL.md and bump the version in `content-skill/.claude-plugin/plugin.json`.

Owner: Abdulrahman Javaid. Approval: the marketing lead.
