# Miki Writer

*[中文](README.md)*

**Turn a topic you've already thought through into a draft you can actually publish — short-form posts, personal-network updates, long-form articles, voiceover/video scripts, bilingual READMEs — one flow, start to finish.**

## What it does

- **Looks for material before writing**: checks your Obsidian vault for daily notes relevant to the topic, instead of waiting for you to supply everything.
- **Sorts facts into five tiers**: verifiable-from-source, things you said yourself, third-party feedback, the model's own inference, and time-sensitive numbers — so an opinion never becomes settled fact and nothing gets invented.
- **Asks when material is thin**: questions that would actually change the draft's direction, instead of padding one out.
- **No fixed template**: every piece finds its own throughline from the actual facts on hand.
- **Keeps your voice**: natural phrasing, self-deprecation, and real emotion stay in — no automatic pass toward one "elevated" tone.
- **Two-stage AI-tell calibration**: lists what reads as AI-written first, then fixes from the structural level down.
- **Protects a finished draft**: once you say "this is final," it only offers suggestions and stops touching the body text.
- **Lightweight, self-evolving style memory**: updates from real differences between your edits and its drafts.
- **Multiple output formats**: short-form social posts, personal-network updates, long-form articles, voiceover drafts/video scripts/teleprompter copy, technical writeups, and bilingual GitHub READMEs.
- **One-click multi-platform adaptation for technical writeups**: one draft rewritten to fit a long-form blog platform and a short-form social platform, facts unchanged. Source material includes experiment data, comments/feedback from links, and verbal explanation, not just a code repo.
- **Image suggestions**: text-only ideas for what to pair with an image — a generation prompt, which screenshot to take, what an infographic should contain. Never generates or picks the actual image.
- **Fiction**: turns an idea into a premise, setting, and characters, then an outline, then chapters. The one mode not bound by the fact-boundary rules.
- **Interactive HTML**: a web version of a technical writeup, a runnable demo for a README, or a standalone landing page — a single self-contained `.html` file with real interactivity, double-click to open, no auto-deploy.

## Requires Obsidian

Searching your Obsidian vault for material before drafting is this skill's core step. There's currently no adapter for other note-taking tools — porting it elsewhere means rewriting the retrieval logic in `SKILL.md` yourself.

## Getting started

### 1. Install Obsidian

Go to [obsidian.md](https://obsidian.md), download the build for your platform, and create a vault.

### 2. Connect this skill to an AI tool

- **Claude** (web/desktop): add this folder via the Skills / Capabilities settings.
- **Claude Code**: drop it into `.claude/skills/` (project or user level) — picked up automatically.
- **Codex or other skill-aware tools**: follow that tool's own instructions.
- **Inside Obsidian directly**: install a community plugin that bridges Obsidian and an AI tool.

### 3. Use it

Describe what you want in plain language, or name it explicitly ("use miki-writer to...") to make sure this skill fires.

## What it won't do

- Never publishes, mass-sends, or handles account credentials without your explicit go-ahead.
- Never invents experiences, data, reviews, or quotes; licensing claims follow the actual repo files.
- Won't write medical/legal/financial-guarantee advice; refuses political-sensitive, hateful, or harassment content.
- Won't fabricate a position when material is missing — it asks first.

## Privacy and portability

Any path or filename in `SKILL.md` is the original user's personal setup, not hardcoded. Sharing this skill exposes none of the original user's note content or folder layout. `references/ip-signature.md` and `references/author-voice.md` belong to the original user — swap in your own.

## License

[PolyForm Noncommercial License 1.0.0](LICENSE) — **noncommercial use only**; commercial use needs separate authorization. Third-party sources and their licenses are in [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md).

## Layout

```
miki-writer/
├── SKILL.md                          main workflow and task routing
├── LICENSE                           PolyForm Noncommercial 1.0.0
├── THIRD_PARTY_NOTICES.md            third-party sources and license notes
└── references/
    ├── facts-and-writing.md          fact boundaries + writing method
    ├── de-ai-calibration.md          AI-tell calibration method
    ├── format-specs.md               per-format output rules
    ├── ip-signature.md                personal signature rules
    ├── author-voice.md                style memory + self-evolution rules
    ├── author-voice-signals.json      signal ledger for self-evolution
    ├── fiction-writing.md            fiction-writing method
    ├── interactive-html.md           interactive HTML method
    └── test-scenarios.md              test scenarios
```
