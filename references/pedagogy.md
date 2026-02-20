# Pedagogy Guide

## Bloom's 2-Sigma Effect

Benjamin Bloom (1984) found that students tutored 1-on-1 with mastery learning performed 2 standard deviations above conventional classroom students. The two key ingredients:

1. **Mastery learning**: Don't advance until the current unit is truly understood
2. **1-on-1 tutoring**: Adapt pace, style, and content to the individual learner

## Socratic Method Integration

Never lecture. Instead:
- Ask questions that lead the learner to discover the answer
- When they're stuck, don't explain — ask a simpler question
- When they answer correctly, don't just confirm — ask them to explain why

## Question Design Patterns

### Diagnostic Questions (Step 1)

Purpose: Quickly map what the learner knows and doesn't know.

| Type | Example | Probes |
|------|---------|--------|
| Vocabulary check | "What does [term] mean to you?" | Do they know the words? |
| Concept sorting | "Which of these are examples of X?" (AskUserQuestion) | Can they categorize? |
| Prediction | "What do you think happens when...?" | Intuition level |
| Explain-back | "Explain [concept] as if to a 10-year-old" | Depth of understanding |

### Teaching Questions (Step 3)

| Pattern | When | Example |
|---------|------|---------|
| **Predict** | Introducing new behavior | "What will this code print?" |
| **Compare** | Distinguishing similar concepts | "How is X different from Y?" |
| **Debug** | Testing careful reading | "This code has a bug. Can you find it?" |
| **Extend** | Testing transfer | "Now how would you modify this to also handle...?" |
| **Teach-back** | Confirming mastery | "Explain to me how [concept] works" |
| **Connect** | Building knowledge graph | "How does [new concept] relate to [previous concept]?" |

### Mastery Check Questions (Step 3e)

These should be synthesis-level:
- Combine the current concept with 1-2 previous concepts
- Require application, not just recall
- Include at least one novel scenario not seen during teaching

## Mastery Scoring

Track per concept:
- Total questions asked
- Correct answers (full or partial)
- Score = correct / total (partial = 0.5)
- Threshold: >= 80% to advance

Qualitative signals of mastery:
- Learner can explain concept in their own words
- Learner can give novel examples
- Learner can identify errors in incorrect examples
- Learner can connect concept to broader context

## Adaptive Pacing

| Signal | Action |
|--------|--------|
| Answers quickly and correctly | Skip to harder questions, consider merging concepts |
| Answers correctly but slowly | Proceed normally, give time |
| Partially correct | Ask follow-up probing questions before moving on |
| Consistently wrong | Break down into sub-concepts, use more concrete examples |
| Frustrated | Switch to a visual aid, use analogy, acknowledge difficulty |
| Bored | Increase difficulty, introduce real-world application |

## Visual Aid Selection

Use the right format for the right purpose:

| Need | Format | When |
|------|--------|------|
| Show relationships | Excalidraw concept map | Concepts have dependencies or hierarchy |
| Walk through process | HTML step-by-step | Code execution, algorithm steps |
| Abstract idea | Generated image (nano-banana-pro) | Metaphors, mental models |
| Compare options | HTML table/grid | Feature comparison, trade-offs |
| Show flow/logic | Excalidraw flowchart | Decision trees, control flow |
| Summarize progress | HTML dashboard | Milestones, session end |

Don't generate visuals for every round — use them when they genuinely help understanding or when the learner seems stuck.
