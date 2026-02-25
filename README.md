# Claude Voice Editor

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Claude Code](https://img.shields.io/badge/Claude_Code-Skill-blue)](https://claude.ai)

A Claude Code skill for editing AI-generated content to match your voice profile.

## The Problem

AI output often sounds generic even with good prompts. The result:

- Content that reads like it was written by a committee
- Loss of your distinctive voice and personality
- Readers noticing "this doesn't sound like you"
- Heavy editing required to make it authentic

This skill provides a systematic 6-pass editing workflow to transform generic AI output into voice-matched writing.

## How It Works

The skill applies six editing passes to any content:

| Pass | Focus | What It Does |
|------|-------|--------------|
| 1. Structure | Organization | Fix openings, flow, conclusions |
| 2. Voice | Profile matching | Align with VOICE.md characteristics |
| 3. Slop | AI tells | Remove generic phrases and patterns |
| 4. Specificity | Depth | Replace generic with specific |
| 5. Rhythm | Flow | Read-aloud test, sentence variation |
| 6. Authenticity | Final check | "Would readers recognize this as mine?" |

## The 30-40% Rule

Even with a perfect style guide, expect to edit 30-40% of AI output. This isn't a bug - it's the feature.

- **If editing >50%:** Your style guide or prompts need work
- **If editing <20%:** You might be accepting too much generic content
- **30-40% is the sweet spot:** Significant time savings while maintaining voice

## Installation

### Option 1: Copy to your Claude Code skills directory

```bash
# Clone the repository
git clone https://github.com/aplaceforallmystuff/claude-voice-editor.git

# Copy to your Claude Code skills directory
cp -r claude-voice-editor/skills/voice-editor ~/.claude/skills/
```

### Option 2: Clone directly to skills directory

```bash
git clone https://github.com/aplaceforallmystuff/claude-voice-editor.git ~/.claude/skills/voice-editor
```

### Option 3: Manual installation

1. Create the directory: `mkdir -p ~/.claude/skills/voice-editor`
2. Download [SKILL.md](skills/voice-editor/SKILL.md) to that directory

## Usage

The skill activates when you ask Claude to:

- "Edit this to match my voice"
- "Apply my voice profile to this draft"
- "Make this sound more like me"
- "Run voice editing on this content"

### Prerequisites

You need a VOICE.md profile. Create one with the companion skill:
- [claude-voice-analyzer](https://github.com/aplaceforallmystuff/claude-voice-analyzer)

### Editing Modes

| Mode | When to Use | Expected Edit % |
|------|-------------|-----------------|
| **Light** | Content close to voice, needs polish | 10-20% |
| **Standard** | Typical AI output with style guide | 30-40% |
| **Heavy** | Generic AI, no style guide used | 50-70% |
| **Rescue** | Fundamentally off but has good bones | Rewrite |

### Example Output

```markdown
## Edited Content

[Your edited content here]

---

## Edit Summary

**Passes completed:** 6/6
**Estimated edit percentage:** 35%
**Voice match confidence:** High

### Major Changes
1. Cut throat-clearing intro, started with the core insight
2. Added characteristic phrase "Here's the thing"
3. Broke uniform sentence lengths into varied rhythm

### Slop Removed
- "It's worth noting that" (3 instances)
- "In today's landscape" (1 instance)
- Staccato fragment spam (paragraphs 2, 5)

### Voice Elements Added
- Conversational asides
- Specific examples replacing generic claims
- Characteristic humor in closing
```

## Common Problems Fixed

| Problem | Symptom | Fix Applied |
|---------|---------|-------------|
| Too formal | Reads like a memo | Add contractions, conversational asides |
| Too uniform | Same sentence lengths | Vary rhythm deliberately |
| Too hedged | Everything qualified | Delete vague hedging, commit to claims |
| Too balanced | All sections equal weight | Let structure reflect priorities |
| Voice drift | Starts strong, gets generic | Re-inject voice markers throughout |

## Related Skills

This skill works best as part of a workflow:

```
[Draft] → slop-detector → voice-editor → slop-detector → [Final]
```

Related skills:
- **voice-analyzer** - Create the VOICE.md profile this skill uses
- **slop-detector** - Identify AI patterns before/after editing

## License

MIT License - see [LICENSE](LICENSE)

---

**The goal: Transform AI's generic output into writing readers recognize as authentically yours.**
