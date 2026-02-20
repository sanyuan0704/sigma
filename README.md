# Sigma

Personalized 1-on-1 AI tutor skill for Claude Code. Based on Bloom's 2-Sigma mastery learning — the finding that students tutored one-on-one with mastery methods perform **2 standard deviations** above conventional classroom students.

Sigma guides you through any topic with Socratic questioning, adaptive pacing, and rich visual output (HTML dashboards, Excalidraw concept maps, generated images).

<p align="center">
  <img src="https://img.shields.io/badge/Claude_Code-Skill-blue" alt="Claude Code Skill" />
  <img src="https://img.shields.io/badge/Method-Bloom's_2--Sigma-green" alt="Bloom's 2-Sigma" />
  <img src="https://img.shields.io/badge/License-MIT-yellow" alt="MIT License" />
</p>

## Installation

```bash
npx claude-code-skill install sanyuan0704/sigma
```

Or manually clone and install:

```bash
# 1. Clone the repo
git clone https://github.com/sanyuan0704/sigma.git

# 2. Copy to your Claude Code skills directory
# Global (available in all projects):
cp -r sigma/ ~/.claude/skills/sigma/

# Or project-level (available in current project only):
cp -r sigma/ .claude/skills/sigma/
```

## Features

- **Socratic Questioning** — Never gives answers directly; guides you to discover them yourself
- **Mastery Learning** — Advances to the next concept only when you demonstrate ≥80% understanding
- **Adaptive Pacing** — Speeds up when you're flying, slows down when you're struggling
- **Visual Roadmap** — Live HTML dashboard tracking your progress through every concept
- **Concept Maps** — Excalidraw diagrams showing relationships between topics
- **Session Persistence** — Save and resume learning sessions anytime
- **Multilingual** — Follows your language automatically; technical terms stay in English with translation

## Usage

After installation, invoke in Claude Code:

```bash
/sigma Python decorators
/sigma 量子力学 --level beginner
/sigma React hooks --level intermediate --lang zh
/sigma linear algebra --resume    # Resume previous session
```

### Arguments

| Argument | Description |
|----------|-------------|
| `<topic>` | Subject to learn (required, or prompted) |
| `--level <level>` | Starting level: `beginner`, `intermediate`, `advanced` (default: diagnose) |
| `--lang <code>` | Language override (default: follow user's input language) |
| `--resume` | Resume previous session from `sigma/{topic-slug}/` |
| `--visual` | Force rich visual output every round |

## How It Works

```
Input → Parse Topic → Diagnose Level → Build Roadmap → Tutor Loop → Session End
                          ↑                                  |
                          |     (mastery < 80%)              |
                          +----------------------------------+
```

### 1. Diagnose

Sigma starts by probing your current understanding with 2-3 diagnostic questions — mixing multiple choice and open-ended — to calibrate exactly where you are.

### 2. Build Roadmap

Decomposes the topic into 5-15 atomic concepts ordered by dependency, then generates a visual HTML roadmap showing your learning path.

### 3. Tutor Loop

For each concept:
- **Introduce** with a question, not a lecture
- **Question cycle** alternating structured choices and open-ended questions
- **Respond adaptively** — harder follow-ups for correct answers, simpler sub-questions for gaps
- **Visual aids** when they genuinely help (Excalidraw diagrams, HTML walkthroughs, generated images)
- **Mastery check** after 3-5 rounds — advance at ≥80%, otherwise targeted remediation

### 4. Session Output

```
sigma/{topic-slug}/
├── session.md          # Learning state, mastery scores, history
├── roadmap.html        # Visual learning roadmap (updated every round)
├── concept-map/        # Excalidraw concept maps
├── visuals/            # HTML explanations, diagrams, images
└── summary.html        # Session summary (at milestones or end)
```

## Pedagogy

Based on three proven principles:

| Principle | Implementation |
|-----------|----------------|
| **Bloom's 2-Sigma** | 1-on-1 tutoring + mastery gating at 80% |
| **Socratic Method** | Questions only — never lecture, never hand-wave |
| **Adaptive Pacing** | Speed up for quick learners, break down for struggling ones |

Question types include: predict, compare, debug, extend, teach-back, and connect — keeping engagement high through variety.

## Structure

```
sigma/
├── SKILL.md                    # Core skill definition
├── README.md                   # This file
└── references/
    ├── pedagogy.md             # Bloom's 2-Sigma theory, question design, mastery criteria
    ├── html-templates.md       # Roadmap, summary, and visual HTML templates
    └── excalidraw.md           # Excalidraw diagram guide, element format, color palette
```

## References

- **pedagogy.md** — Bloom's 2-Sigma theory, Socratic questioning patterns, mastery scoring, adaptive pacing strategies
- **html-templates.md** — Premium dark UI templates for roadmap, summary, and visual explanations (glassmorphism, micro-animations)
- **excalidraw.md** — Excalidraw HTML template, element types, color palette, layout patterns for concept maps and flowcharts

## License

MIT
