# Miki Writer

*[中文](README.md)*

**Turn a topic you've already thought through into a draft you can actually publish — short-form posts, personal-network updates, long-form articles, voiceover/video scripts, bilingual GitHub READMEs — one flow, start to finish.**

## What it does

- **Looks for material before writing, instead of waiting for you to supply it**: checks your Obsidian vault for daily notes relevant to the topic, to see what you already thought or said.
- **Sorts facts into five tiers**: verifiable-from-source, things you said yourself, third-party feedback, the model's own inference, and time-sensitive numbers — kept separate so an opinion never gets dressed up as settled fact, and nothing gets invented to fill a gap.
- **Asks when material is thin**: if it can't find relevant notes, or what's there doesn't support a full piece, it asks questions that would actually change the draft's direction, instead of padding one out.
- **No fixed template**: every piece finds its own throughline (what happened, how thinking shifted, what tradeoff got made) from the actual facts on hand.
- **Keeps your voice**: natural phrasing, self-deprecation, and real emotion stay in — no automatic pass toward one "elevated" tone.
- **Two-stage AI-tell calibration**: lists what reads as AI-written first, then fixes from the structural level down, rather than mechanically flipping every AI pattern into its opposite.
- **Protects a finished draft**: once you say "this is final," it only offers suggestions and stops touching the body text; nothing you cut reappears on its own.
- **Lightweight, self-evolving style memory**: after you hand-edit a draft, it compares your edit against its own version and updates a small style file — only from real differences.
- **Multiple output formats**: short-form social posts, personal-network updates, long-form articles, voiceover drafts/video scripts/teleprompter copy, technical writeups, and bilingual GitHub READMEs, each with its own format rules and compliance checks.
- **One-click multi-platform adaptation for technical writeups**: once a technical long-form draft is done, it can be rewritten to fit a long-form blog platform and a short-form social platform's conventions — facts and conclusions stay fixed, only phrasing and length adapt. Source material isn't limited to a code repo; it also covers experiment data, comments/feedback from links, and the author's own verbal explanation.
- **Image suggestions (text only, no image generation)**: for short-form posts, personal-network updates, and technical writeups, it can suggest what to pair with an image — an AI image-generation prompt, which screenshot to take, or what an infographic should contain. It never generates or picks the actual image.
- **Fiction**: helps turn a not-yet-developed idea into a premise, setting, and characters, then an outline, then chapters. This is the one mode not bound by the fact-boundary rules — plot and characters are meant to be invented here.
- **Interactive HTML**: a web version of a technical writeup, a runnable demo embedded in a README, or a standalone landing/intro page — delivered as a single self-contained `.html` file (real click-to-expand, tabs, hover charts where useful), no build tooling required, double-click to open. It doesn't deploy or publish anything on its own.

## Requires Obsidian

This skill is built around Obsidian — searching your Obsidian vault for material before drafting is its core step, and there's currently **no** generic adapter for other note-taking tools. Porting it elsewhere means rewriting the retrieval logic in `SKILL.md` yourself; it isn't plug-and-play. If you don't have Obsidian yet, see the setup steps below.

## Getting started (no AI experience required)

### Step 1: Install Obsidian

1. Go to [obsidian.md](https://obsidian.md) and download the build for your platform (Windows / Mac / Linux / mobile).
2. Open it and create a new vault (basically a folder Obsidian uses to hold your notes).
3. Menu wording may shift between versions — follow Obsidian's own current setup instructions if what you see doesn't match exactly.

### Step 2: Connect this skill to an AI tool

- **Claude** (web or desktop): look for a Skills / Capabilities section in settings and add this folder following that version's prompts.
- **Claude Code**: drop this folder into your project's `.claude/skills/` directory (or the user-level skills directory) — it gets picked up automatically.
- **Codex or other tools with skill support**: follow that tool's own instructions for adding a skill folder.
- **To use it directly inside Obsidian**: you'll need a community plugin that bridges Obsidian and an AI tool — search Obsidian's community plugin browser for one that connects to Claude, install it, and configure API access. Once that's set up, you can invoke the skill while editing a note.

Exact menu locations vary by tool and change over versions — check that tool's current documentation if something doesn't match what's described here.

### Step 3: Use it

Just describe what you want in plain language — e.g. "turn this project into a short post." You can also name it explicitly ("use miki-writer to help me write...") to make sure this skill fires rather than the model improvising on its own.

## What it won't do

- Never publishes, mass-sends, logs into a platform's backend, or handles account credentials — any of that needs your explicit go-ahead in conversation.
- Never invents experiences, data, reviews, or quotes; licensing claims follow whatever files actually exist in the repo.
- Won't write medical/legal/financial-guarantee advice, and refuses political-sensitive, hateful, or harassment-adjacent content.
- Won't fabricate a position when material is missing — it asks first.

## Privacy and portability

It reads material already organized in your Obsidian vault to find background context, but **no folder path is hardcoded** — any path or filename in `SKILL.md` is the original user's personal setup. Sharing this skill exposes none of the original user's note content or folder layout; whoever picks it up just points it at their own vault. `references/ip-signature.md` (signature lines, banned phrases) and `references/author-voice.md` (style memory) belong to the original user — swap in your own before using it on yourself.

## License status

This repository is licensed under [PolyForm Noncommercial License 1.0.0](LICENSE) — **noncommercial use only**; commercial use needs separate authorization. This matches the license of one of the projects it was originally distilled from, which is the safest choice available right now. It was originally distilled from a few open-source projects; their sources, the inheritance relationship, and each one's license status are in [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md) — one is confirmed MIT with its notice attached, the other is deliberately left an open question rather than assumed either way.

## Layout

```
miki-writer/
├── SKILL.md                          main workflow and task routing
├── THIRD_PARTY_NOTICES.md            third-party sources and license notes
└── references/
    ├── facts-and-writing.md          fact boundaries + writing method
    ├── de-ai-calibration.md          AI-tell calibration method
    ├── format-specs.md               per-format output rules (incl. one platform's banned-word list)
    ├── ip-signature.md                personal signature rules
    ├── author-voice.md                style memory + self-evolution rules
    ├── author-voice-signals.json      signal ledger for self-evolution (keep updating, don't wipe)
    └── test-scenarios.md              test scenarios
```

## Status

- Version: v0.2 (merged in a former sub-skill for voiceover/video scripts; narrowed to a single writing entry point).
- Confirmed boundaries: no auto-publishing/uploading; the banned-word list needs ongoing updates; signature style is settled only for video scripts so far.
- No real final draft has shipped through it yet; the first real test case is in progress.
