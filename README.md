# AI Knows Ball 🏀🤖

> Teaching AI to talk like a real one. No cap.

**AI Knows Ball** is the ultimate skill pack to stop your AI from being an NPC. It trains assistants to understand, speak, and detect Gen Z language — fr fr. Built on the [Antigravity Skills](https://github.com/guanyang/antigravity-skills) format so you can plug it in and slay immediately.

---

## ✨ The Skills

| Skill | Vibe Check |
|---|---|
| [`@genz-translator`](skills/genz-translator/SKILL.md) | Translates boomer speak ↔ Gen Z bops |
| [`@genz-detector`](skills/genz-detector/SKILL.md) | Scores the authenticity (0–10). Don't be mid. |

---

## 📂 The Setup

```
AI Knows Ball/
├── skills/
│   ├── genz-translator/
│   │   ├── SKILL.md              # Core skill definition
│   │   ├── examples/             # Usage examples
│   │   └── resources/
│   │       └── slang_dict.json   # Master Gen Z slang dictionary
│   └── genz-detector/
│       ├── SKILL.md              # Core skill definition
│       └── examples/             # Usage examples
├── data/
│   └── training_conversations.jsonl  # Training input/output pairs
├── skills_index.json             # Skills metadata registry
└── README.md
```

---

## 🚀 Getting it Started

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

> 💡 Tip: For maximum compatibility, copy into `.agent/skills/` — most tools auto-discover it.

---

## 🎮 Usage

Once installed, invoke in your AI assistant:

```
@genz-translator I am very tired and don't want to attend this meeting.
```
```
→ i'm so cooked fr fr, can't even think abt that meeting rn 💀
```

```
@genz-translator Explain this: "no ❤️"
```
```
→ A "soft" no — using the heart emoji to lessen the blow of a rejection or disagreement.
```

```
@genz-detector "Our new product is totally bussin and on fleek! YOLO!"
```
```
→ Authenticity Score: 2/10 | Verdict: Corporate-trying-to-be-cool. Major L.
```

```
@genz-translator What does "delulu" mean?
```
```
→ Delusional — believing something unrealistic. Still very active slang.
```

---

## 📊 Dataset

The `data/` folder contains structured training data:

- **`training_conversations.jsonl`** — 40+ input/output translation pairs (JSONL format)
- **`slang_dict.json`** — 50+ terms with meanings, examples, authenticity scores, and active/expired status (including Gen Z emoji meanings)

### Data Schema

**slang_dict.json entry:**
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

**training_conversations.jsonl entry:**
```json
{
  "input": "I am very tired today.",
  "output": "i'm so cooked fr fr 💀",
  "type": "normal_to_genz",
  "notes": "lowercase, fr fr for emphasis, 💀 for exhaustion"
}
```

**Translation types:**
- `normal_to_genz` — Standard English → Gen Z
- `genz_to_normal` — Gen Z slang → plain English explanation
- `corporate_to_genz` — Corporate speak → Gen Z

---

## 🤝 Pull Up (Contribute)

Got new slang? Don't gatekeep, drop a PR!

1. Add new terms to `skills/genz-translator/resources/slang_dict.json`
2. Add training pairs to `data/training_conversations.jsonl`
3. Follow the existing JSON schema
4. Make sure the term is actually current (check `authenticity_score` — expired terms score 0-2)

---

## 📜 The Fine Print (License)

MIT — free to use, modify, and distribute. Just don't be mid about it.

---

*Built by [@saxrasm](https://github.com/saxrasm) · AI Knows Ball 🏀*
