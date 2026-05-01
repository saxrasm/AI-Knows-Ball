<div align="center">
  
# AI Knows Ball

*Teaching your AI to talk like a real one. No cap.*

[![Antigravity Skills](https://img.shields.io/badge/Antigravity-Compatible-blue.svg)](https://github.com/guanyang/antigravity-skills)
[![Slang Words](https://img.shields.io/badge/Slang%20Dictionary-250%2B%20Terms-green.svg)](#dataset)
[![Version](https://img.shields.io/badge/Version-2.0.0-purple.svg)]()

</div>

---

**AI Knows Ball** is the ultimate skill pack to stop your AI from being an NPC. It trains assistants to understand, speak, and vibe with Gen Z language naturally. Built on the **Antigravity Skills** format so you can plug it in and slay immediately.

We ditched the complex "translators" and "detectors". Now, it's just one unified skill that simply *gets it*.

---

## The Skill

| Skill | Vibe Check |
|---|---|
| [`@genz`](skills/genz/SKILL.md) | Makes your AI authentically understand and speak Gen Z culture. |

---

## Getting it Started

### Works with any AI assistant, periodt:

**Gemini / Antigravity**
```bash
mkdir -p ~/.gemini/antigravity/skills
cp -r skills/* ~/.gemini/antigravity/skills/
```

**Claude**
```bash
mkdir -p ~/.claude/skills
cp -r skills/* ~/.claude/skills/
```

**Cursor / Windsurf / Copilot**
```bash
mkdir -p .agent/skills
cp -r skills/* .agent/skills/
```

> **Tip:** For maximum compatibility, copy into `.agent/skills/` — most tools auto-discover it.

---

## Usage

Once installed, simply invoke `@genz` in your AI assistant:

```text
@genz What does "skibidi" even mean?
```
> **AI:** It's a nonsensical Gen Z/Gen Alpha slang term that originated from a weird YouTube series. Depending on context, it can mean something is bad, crazy, or it's just used as filler. 

```text
@genz Tell my boss I can't come to work today because I'm exhausted, but make it Gen Z.
```
> **AI:** "hey i'm absolutely cooked today ngl. gonna have to take a bed rot day fr fr."

---

## Dataset

The `data/` folder contains structured training data that powers the skill:

- **`slang_dict.json`** — **250+ terms** with meanings, examples, authenticity scores, and active/expired status (including Gen Z emoji meanings)
- **`training_conversations.jsonl`** — **45+** input/output conversation pairs for AI fine-tuning

### Data Schema Example

```json
{
  "term": "rizz",
  "meaning": "Natural charisma or ability to attract others",
  "category": "compliment",
  "usage": "Praising someone's natural charm",
  "example": "Bro walked in and had instant rizz",
  "status": "active",
  "authenticity_score": 10
}
```

---

## Pull Up (Contribute)

Got new slang? Don't gatekeep, drop a PR!

1. Add new terms to `skills/genz/resources/slang_dict.json`
2. Add training pairs to `data/training_conversations.jsonl`
3. Make sure the term is actually current (check the vibe).

---

## The Fine Print (License)

MIT — free to use, modify, and distribute. Just don't be mid about it.

