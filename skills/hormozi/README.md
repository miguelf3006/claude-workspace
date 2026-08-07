# hormozi — one skill, three books, 54 chapters

Merged from four separate skills (`hormozi-offers`, `hormozi-leads`, `hormozi-money-models`,
`hormozi-acquisition-system`) into a single skill with one entry point.

## Install

```bash
# Claude Code
cp -r hormozi ~/.claude/skills/

# Codex CLI
cp -r hormozi ~/.codex/skills/

# Cursor / Gemini CLI / Copilot / Amp (cross-agent)
cp -r hormozi ~/.agents/skills/
```

Remove the four old skills first so they don't compete for triggering:

```bash
rm -rf ~/.claude/skills/hormozi-offers ~/.claude/skills/hormozi-leads \
       ~/.claude/skills/hormozi-money-models ~/.claude/skills/hormozi-acquisition-system
```

## Structure

```
hormozi/
├── SKILL.md                        router + master diagnostic + cross-book synthesis (~188 lines)
├── agents/openai.yaml              Codex-only metadata
└── references/
    ├── topic-index.md              107 topics → exact chapter, across all four sections
    ├── system/                     cross-book synthesis · 8 chapters
    ├── offers/                     $100M Offers · 16 chapters
    ├── leads/                      $100M Leads · 16 chapters
    └── money-models/               $100M Money Models · 14 chapters
```

Each section folder has `overview.md` (core frameworks + chapter index), `chapters/`,
`glossary.md`, `patterns.md`, and `cheatsheet.md`.

## What changed in the merge

- **One trigger instead of four.** The description covers all three books plus plain-language
  growth symptoms, so it fires whether the user names a framework or just says "my leads are
  too expensive."
- **Unified topic index.** The four separate topic indexes are merged into one A–Z list, so
  a topic like *Guarantees* now shows all five chapters across three books on a single line
  instead of being split across four skills.
- **Cross-references rewritten.** Text that pointed at companion skills (`` `hormozi-leads` ch10 ``)
  now points at real paths inside this skill.
- **Same progressive disclosure.** Only the description sits in context at startup; SKILL.md
  loads on trigger (~2.7k tokens); chapters load only when actually read.

## Source note

Built from **audiobook transcripts**, not print editions. The *$100M Money Models* transcript
is an **abridged narration** and lacks the client-financed-acquisition / LTGP:CAC vocabulary
of the print edition; that terminology comes from the *$100M Leads* source and is captured in
`references/leads/chapters/ch10-paid-ads-money.md`. Where the print editions go further, these
files say nothing rather than inventing it.
