# ADHD Academic Tutor

An explicit-trigger Codex skill for ADHD-friendly academic literature reading and writing.

This skill is designed for learners who get stuck on English-language papers, lack field structure, and need a tutor to take over session planning once explicitly invoked. It pre-digests academic topics, assigns carefully selected source-reading slices, calibrates realistic reading time from feedback, and maintains local memory for continuity.

## What it does

- Stays silent unless explicitly invoked with `$adhd-academic-tutor`
- Runs guided thematic literature surveys
- Assigns targeted deep-reading segments instead of whole papers
- Adds a Read-First Base before source reading
- Uses generous early time ranges and calibrates from feedback
- Validates completion with low-pressure checks
- Records evidence-backed achievements for confidence rebuilding
- Maintains local Markdown/JSON memory outside the skill

## Install

Copy or symlink the skill folder into your Codex skills directory:

```bash
ln -s /path/to/adhd-academic-tutor/adhd-academic-tutor ~/.codex/skills/adhd-academic-tutor
```

Then start a new Codex session and invoke:

```text
Use $adhd-academic-tutor start
```

## First-time memory setup

On each new machine, create the private local memory directory before first use:

```bash
python3 adhd-academic-tutor/scripts/init_memory.py
```

By default this creates:

```text
~/.adhd-academic-tutor/memory/
```

To use a custom private memory location:

```bash
python3 adhd-academic-tutor/scripts/init_memory.py --memory-dir /path/to/private/memory
```

The skill will run first-time onboarding if `user_cognitive_profile.md` says `Status: not onboarded`.

## Repository layout

```text
adhd-academic-tutor/
├── SKILL.md
├── agents/openai.yaml
├── scripts/init_memory.py
└── references/
    ├── memory_schema.md
    ├── report_templates.md
    └── session_protocols.md

adhd-academic-tutor-full-description.md
```

The `state/` directory is intentionally ignored. It contains local learner memory and should not be committed.

## License

MIT
