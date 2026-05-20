# 03: Digital Storyboards

![Storyboard](https://img.shields.io/badge/section-storyboard-f97316)

## Lesson Purpose

This lesson teaches you to plan visual and multimedia content — explainer videos, slide lessons, product demos, and training sequences — using AI as a planning tool before production begins.

A storyboard is a scene-by-scene plan that tells a visual story. It is not a script. It is not a shot list. It is the bridge between an idea and the production team or tool that will build it.

The key principle here is the same as in blog writing: plan structure before generating content. An unplanned AI-generated video script produces a talking-head monologue with no visual thinking. A structured storyboard prompt produces something a production team can actually use.

## Lesson Overview

| Activity | Outcome |
| --- | --- |
| Define the story goal | You identify what the viewer should think or do after watching |
| Choose the narrative structure | You build a clear opening problem, solution, and resolution |
| Create the storyboard table | You specify visual, text, narration, and production notes |
| Add review criteria | You check pacing, clarity, and risk |
| Revise a weak scene | You improve one specific scene before production |
| Compare before and after | You see how revision changes quality |

---

## What a Storyboard Is For

A storyboard solves a specific problem: it forces the team to think visually before they spend money on production.

Without a storyboard, videos often suffer from:
- Too much narration, not enough visual story.
- No clear moment where the viewer learns the main idea.
- Scenes that repeat the same concept without adding new information.
- Missing review or safety steps in content about sensitive topics.
- Visuals that production cannot realistically deliver.

A storyboard that answers these questions before production begins saves significant rework:

| Question | Why it matters |
| --- | --- |
| What does the viewer see in each scene? | Identifies whether the concept is actually visual |
| What is the one job of each scene? | Prevents scenes that just repeat information |
| What does the narrator say? | Ensures narration adds to the visual rather than just describing it |
| Is there a human review step? | Critical for AI, legal, financial, or compliance content |
| Can this be produced realistically? | Prevents beautiful plans with impossible visuals |

---

## Narrative Structure for Short Video

Most effective explainer videos follow a three-part structure:

**Part 1 — The Problem (25% of scenes):**
Show the situation the viewer recognizes. This is not about your product or course. It is about the viewer's current reality.

**Part 2 — The Solution (50% of scenes):**
Show the workflow, product, or approach that changes the situation. Be specific. Generic advice disappears.

**Part 3 — The Resolution and Next Step (25% of scenes):**
Show what life or work looks like after the change, and give a specific, simple next action.

A 60-second video with five scenes at these proportions:
- Scene 1: The problem (the before state)
- Scenes 2–3: The solution (the workflow in practice)
- Scene 4: The human review — always present in responsible AI content
- Scene 5: The resolution and call to action

---

## The Storyboard Table Fields

| Field | Purpose |
| --- | --- |
| Scene number | Keeps the sequence organized and reviewable |
| Scene goal | Defines the single job this scene must do |
| Visual description | Describes exactly what the viewer sees — specific, not vague |
| On-screen text | Short visible text only — not full sentences |
| Narration | The spoken or written words — adds context the visual cannot carry |
| Production notes | Risks, sources, privacy concerns, or special requirements |

> **Tip:** "On-screen text" and "narration" should never say the same thing. If the narration restates what is on screen, one of them is unnecessary. Visual storytelling is about contrast and layering — the visual shows, the text anchors, the narration explains.

---

## Scenario: The Weekly Update Workflow

A company wants a 60-second explainer video:

**Title:** How AI Can Help Prepare a Weekly Project Update

**Audience:** Managers and corporate employees who are not sure whether AI is safe to use for internal reporting.

**Core message:** AI can organize a draft from your existing notes — but you remain responsible for every word before it is sent.

**What the video must accomplish:**
- Show the real problem (messy notes → late, incomplete updates).
- Show the prompt-based workflow (not a sales pitch — show the actual steps).
- Show the review step prominently (this is the trust-building scene).
- Show the result (clean, organized update in less time).
- End with a clear next step (try the prompt template or register for the workshop).

---

## Storyboard Prompt

```text
Act as a digital storyboard planner.

Create a storyboard for a 60-second explainer video.

Target audience:
[describe the viewer: role, situation, level of familiarity]

Video goal:
[what should the viewer think or do after watching?]

Core message:
[the one idea the video must communicate]

Required elements:
- Scene 1 must show the viewer's current problem (not our solution).
- At least one scene must show an actual workflow or process (not just describe it).
- One scene must include a human review step.
- The final scene must have a specific, actionable next step.

Rules:
- Use plain English for all narration.
- No personal names.
- No unsupported outcome claims.
- On-screen text must be short — three to seven words per line.
- Narration must add information that the visual cannot carry alone.
- Each scene has one job only.

Format:
Return a table with exactly these columns:
Scene | Goal | Visual | On-screen text | Narration | Production notes
```

---

## Example: Full Storyboard

| Scene | Goal | Visual | On-screen text | Narration | Production notes |
| --- | --- | --- | --- | --- | --- |
| 1 | Show the problem | Cluttered notes, chat threads, task list | Weekly updates can get messy | A good update covers decisions, progress, risks, and next steps. Most start as scattered notes. | Avoid showing real private data — use placeholder text |
| 2 | Introduce the workflow | Empty prompt window with structured input | Give AI a clear job | Start with four elements: task, context, constraints, and format. | Show the prompt briefly — not too fast to read |
| 3 | Show AI organizing the draft | Notes being structured into sections | Draft — not final | AI can sort and summarize your notes. It cannot verify them — that is still your job. | Label output clearly as "draft for review" |
| 4 | Show the review step | Checklist next to draft, items being checked | Review before sending | Check accuracy, ownership, deadlines, and anything sensitive before this leaves your desk. | This scene must feel serious — not rushed |
| 5 | Show the result and next step | Clean, organized update with clear sections | Clear updates. Less time. | A better weekly update helps the whole team — and this workflow usually takes under ten minutes. | End with soft call to action — one line |

---

## The Review Prompt

After generating a storyboard, run this quality check before sharing it with a production team:

```text
Review this storyboard.

For each scene, check:
1. Does the scene have one clear job — or is it trying to do too much?
2. Does the on-screen text duplicate the narration, or do they layer?
3. Is the visual description specific enough to brief a designer or video editor?
4. Is there a scene where a human reviews AI output — and is it prominent?
5. Is the final call to action specific and achievable?
6. Are there any scenes that repeat the same idea without adding new information?

Return a table with:
Scene | Issue | Severity (high/medium/low) | Fix
```

---

## Revising a Weak Scene

Take Scene 3 from the example above — the AI draft scene. Here is a weak version and an improved version:

**Weak:**
| Field | Content |
| --- | --- |
| Visual | AI output on a screen |
| On-screen text | The draft is ready |
| Narration | AI has created a draft of your update |

**Improved:**
| Field | Content |
| --- | --- |
| Visual | Notes transformed into labeled sections: Decisions, Progress, Risks, Next Steps |
| On-screen text | Draft — not final |
| Narration | AI can sort and summarize your notes into sections — but it cannot verify them. That step is yours. |

The improved version shows specifically what changed (the structure), reminds the viewer of their responsibility (verification), and uses on-screen text and narration to carry different information.

> **Note:** In content about AI tools, the human review scene is not optional. It is the scene that makes the whole video trustworthy. Rushing or skipping it signals to the viewer that the product does not take accuracy seriously.

---

## Common Storyboard Mistakes

- **Visuals described as "person using computer"** — too vague to produce. Specify what is on the screen.
- **On-screen text as full sentences** — if it is more than seven words, it belongs in the narration.
- **Every scene uses the same visual style** — variation helps pacing and attention.
- **No review scene for AI content** — always show the human-in-the-loop step.
- **Scene goals that say "explain X"** — not a goal. "Show the viewer what the draft looks like" is a goal.
- **Scenes that repeat each other** — every scene must advance the story.

---

## From Storyboard to AI Video Brief

A storyboard defines what should happen in each scene. An AI video brief tells a video generation tool how to produce it. If your team uses an AI video tool, each storyboard scene needs to be translated into a production prompt.

Two prompt formats are widely used:

**Format 1: Single-line descriptive prompt**

Write one sentence per scene that includes shot type, subject, setting, action, and any audio cues. Keep it specific and visual — vague descriptions produce generic footage.

```text
[Shot type] of [subject] [action] in [setting]. [Key visual details]. [Audio note if any.]
```

Example for Scene 4 of the weekly update storyboard:

```text
Close-up of a manager at a clean desk, checking items on a printed review checklist
next to a visible document draft. Soft office lighting, no clutter on desk.
She marks two items and pauses on a third. No dialogue. Calm ambient office sound.
```

**Format 2: Structured JSON prompt**

For tools that accept structured input, a JSON format lets you control camera movement, environment, and subject action as separate variables. This makes it easy to adjust one field without rewriting the whole scene.

```json
{
  "prompt": "A manager reviews a structured AI-generated report at a clean desk.",
  "config": {
    "camera": {
      "angle": "medium shot",
      "movement": "slow push-in toward the document"
    },
    "environment": {
      "setting": "modern open-plan office",
      "elements": "soft ambient light, minimal desk, one plant in background",
      "vibe": "calm, professional, focused"
    },
    "subject": {
      "type": "office worker",
      "action": "reading a structured document",
      "detail": "highlights one section with a checkmark, pauses to think"
    }
  }
}
```

> **Tip:** Check whether the AI video tool your team uses accepts plain-text prompts, JSON input, or both. The descriptive format is more portable across tools. The structured JSON format gives finer control when the tool supports it.

**Production rule:** Treat AI video output as a draft — just as you treat AI text output as a draft. Check that scenes are in the correct order, that no private or confidential information appears on screen, and that the human review scene is clearly visible before sharing with anyone outside your team.

---

## Practice

- A product launch explainer (60 seconds).
- A course or workshop promotion (90 seconds).
- A customer onboarding walkthrough (60 seconds).
- A student study guide introduction (45 seconds).
- An internal AI policy training sequence (5 slides).

Produce and submit:

1. A story goal statement (one sentence).
2. A narrative structure map (Part 1 / Part 2 / Part 3 — scenes assigned to each).
3. A full storyboard table (five to seven scenes).
4. A review table with at least three issues identified.
5. A revised version of your weakest scene.

---

## Review Checklist

- [ ] Does each scene have exactly one goal?
- [ ] Are visual descriptions specific enough for a designer or editor to act on?
- [ ] Do on-screen text and narration carry different information?
- [ ] Is there a prominent human review scene?
- [ ] Does the final scene have a specific, actionable next step?
- [ ] Have you removed any scenes that repeat without adding new information?
