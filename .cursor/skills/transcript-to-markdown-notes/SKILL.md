---
name: transcript-to-markdown-notes
description: >-
  Turns Artist Commons lecture transcripts (or extracted PDF text) into neutral class-style
  summary.md study notes (no speaker attribution). Use when the user asks for lecture notes, session summaries,
  transcript summaries, summary.md, cohort session documentation, workshop wrap-ups,
  interview notes, reading chapter summaries, or adapting transcript/PDF text to markdown
  in this repository.
disable-model-invocation: true
---

# Transcript to Markdown Notes (Artist Commons)

Convert raw capture into **scannable study notes** — not a cleaned transcript.

## When to use

- User points at `transcript.txt`, `transcript/transcript.txt`, or extracted `.txt` from a PDF
- User wants `summary.md` (or reading-folder `*-summary.md` / `book-summary.md`)
- New lecture folder needs documentation matching existing quarter_1 / quarter_2 patterns

## Inputs and outputs

| Input | Typical path | Output |
|-------|--------------|--------|
| Lecture transcript | `quarter_N/lectures/NNN_topic/transcript.txt` or `transcript/transcript.txt` | `summary.md` in lecture folder |
| PDF chapter | `reading/.../*.pdf` | Extract `.txt` sibling, then `*-summary.md` |
| Slides / takeaways | `documentation/`, `session_documentation/` | Supplement only — summarize from transcript first |

**Do not edit the transcript** unless the user asks for cleanup.

## Workflow

Copy this checklist and track progress:

```
- [ ] 1. Locate and read full source (chunk if long; outline first)
- [ ] 2. Infer title and topic (optional brief Context—no speaker names)
- [ ] 3. Classify session type → pick template in templates.md
- [ ] 4. Draft summary.md
- [ ] 5. Quality pass (below)
```

### 1. Read the source

- Timestamp format: `Speaker | 00:00` — **omit timestamps** in the summary
- For files over ~300 lines, read in sections and build a section outline before writing

### 2. Header (class notes)

Write as **class notes**, not a recap of who spoke. Do **not** include `**Speaker:**` / `**Host:**` lines or attribute ideas to individuals (`**Haiver** says…`, `**Jenn** emphasizes…`). Omit transcript speaker names unless a guest's identity is essential to the content (e.g. interview biography).

```markdown
# [Descriptive Title]

---

## Overview
2–4 sentences on what the session covers and why it matters.
```

Optional: one neutral `**Context:**` line about the topic or place in the program—no names.

**Title:** Derive from folder slug + opening lines (e.g. `123_how_approach_curator` → "How to Approach Curators and Galleries").

### 3. Classify session type

| Type | Emphasis | Repo examples |
|------|----------|---------------|
| **Workshop / presentation** | Projects, process, tools, artist quotes | `110_mccoy_workshop`, `106_mccoy_presentation` |
| **Interview / conversation** | Background, themes, Q&A threads | `111_conversation_Whitney_Hart`, `118_interview_alissa_wilkinson` |
| **Pedagogy / framework** | Agreements, steps, language norms | `109_crit` |
| **Academic** | Concepts, definitions, lineage | `107_philosophy_of_art`, `108_art_history_system` |
| **Practical advice** | Actionable steps, email/scripts, pitfalls | `113_portfolio`, `123_how_approach_curator` |
| **Reading** | Thesis, key concepts, anecdotes, takeaways | `Seven_Days…Crit-summary`, `book-summary.md` |

Hybrid sessions: use the **dominant** type (e.g. portfolio lecture with Q&A → practical).

Section skeletons: [templates.md](templates.md)

### 4. Body conventions

- Major sections: `##` with `---` between them
- Subtopics: `###`
- **Bold** key terms, names, frameworks
- Bullets for lists; short paragraphs for ideas that need 2–3 sentences
- Blockquotes (`>`) for principles or memorable lines — sparingly
- Tables only for schedules, comparisons, or step matrices
- End with **Takeaways** or **Practical notes** when advice- or process-heavy
- **No speaker attribution** — neutral class notes; use "the session," "the lecture," or state ideas directly
- Keep program vocabulary when relevant (cohort feedback sessions, etc.)
- **No emojis** in new summaries unless user requests
- Match [markdown-cheatsheet.md](../../../markdown-cheatsheet.md) syntax

**Tone:** Impersonal study notes (like classroom notes). Paraphrase spoken lines into clear claims; avoid "argues," "notes," or "says" tied to a named person.

### 5. PDF sources

If input is PDF only:

```bash
pdftotext -layout "path/to/file.pdf" "path/to/file.txt"
```

If `pdftotext` unavailable: `pip install pypdf` and extract per page with `PdfReader`.

Then summarize from `.txt` using the same workflow (reading template if book chapter).

## Quality pass

Before finishing, verify:

- [ ] Overview accurately frames the whole session (2–4 sentences)
- [ ] Sections are scannable (`##` / `###`, bullets, bold)
- [ ] No timestamp litter or verbatim transcript dumps
- [ ] Quotes only where they teach; otherwise paraphrase
- [ ] No Speaker/Host block; no "who said what" unless guest identity is required
- [ ] Takeaways / practical section present when applicable
- [ ] Filename and location match repo convention (`summary.md` in lecture folder)

## Anti-patterns

See [examples.md](examples.md). Avoid:

- Emoji-heavy wrap-ups (`103_lec_visual_analysis/summaries/lecture-wrap-up.md` — older style)
- Plain `summary.txt` unless user explicitly wants non-markdown
- Pasting long transcript blocks into the summary

## Golden references

Read one example matching your session type before writing: [examples.md](examples.md)
