# 🧠 BRAIN DUMP

### A Systematic Process for Teaching AI New Subjects

**Version:** 1.1  
**Created:** February 16, 2026  
**Updated:** February 16, 2026  
**Authors:** Patrick Chinery, Maui  
**Storage:** GitHub (MFAutomations) → Frank (RAG/Knowledge) → NAS (Backups)

---

## Overview

Brain Dump is a structured workflow for teaching an AI a new subject — comprehensively, systematically, and to **EXPERT MASTERY** level.

The process uses a multi-agent swarm architecture to decompose, research, document, integrate, and validate knowledge until it's fully captured in a searchable RAG system.

---

## ⚠️ CORE PRINCIPLE: EXPERT MASTERY

**This is non-negotiable.**

Brain Dump does NOT produce:
- ❌ Surface-level overviews
- ❌ "Good enough" knowledge
- ❌ High-level summaries
- ❌ Beginner or intermediate content

Brain Dump ONLY produces:
- ✅ **EXPERT MASTERY** — the level where you could teach professionals
- ✅ **Certification-passing depth** — know it well enough to pass the hardest exams
- ✅ **Practitioner-level detail** — the nuances that separate experts from amateurs
- ✅ **Complete coverage** — no gaps, no "we'll skip this part"

**Every single subtopic gets EXPERT MASTERY treatment. No exceptions.**

If the knowledge coming into the RAG isn't at mastery level, it doesn't belong there.

---

## Trigger Phrases

Any of these will start the Brain Dump process:

- `Brain Dump: [topic]`
- `Let's do a Brain Dump on [topic]`
- `Brain Dump [topic]`
- `I need a Brain Dump for [topic]`

---

## Storage Architecture

| What | Where | Access |
|------|-------|--------|
| **Playbooks/Workflows** | GitHub: `MFAutomations` | Patrick, Adrien (BirdDigital), Maui |
| **Playbooks/Workflows (mirror)** | Frank: `/Users/adrienbird/MFAutomations/` | Frank, Maui, Adrien's machines |
| **Knowledge Bases & RAGs** | Frank: `/Users/adrienbird/knowledge/` | Frank, Maui, Adrien's machines |
| **Backups & Archives** | NAS: `192.168.0.251:/shared/backups/` | Everyone on network |

---

## Agent Model Reference

| Model | Role | Use Case |
|-------|------|----------|
| **Opus 4.5** | Orchestrator / Heavy lifting | Coordination, complex synthesis, quality control |
| **Sonnet 4.5** | Main subtopic research | Deep research on specific areas |
| **Haiku 4.5** | Granular breakdown | Small chunks, simple tasks, parallel volume |

---

# THE 6 PHASES

---

## PHASE 1: CAPTURE

**Purpose:** Get the full picture of what needs to be learned

### Questions to Ask:

1. **"What topic/subject do you want ME to learn about?"**

2. **"What's the end goal?"**
   - Pass a certification without taking it?
   - Build a practical skill?
   - Create handoff-ready documentation for a team?

3. **"Any existing templates or patterns to follow?"**
   - (e.g., "same structure as the lawyer agents")

### Auto-Handled:
- Documentation automatically lives in Frank's RAG directory (no need to ask)

### Output:
- Clear understanding of topic, goal, and any templates to follow

---

## PHASE 2: DECOMPOSE

**Purpose:** Break the topic into learnable chunks

### Agent Structure:
- 1 Opus 4.5 orchestrator
- Sonnet 4.5 subagents (one per main subtopic)
- Haiku 4.5 sub-subagents (for further breakdown)

### What Happens:

1. **Break topic into subtopics**
   - Create manageable list (e.g., "Law" → 10 lawyer types)

2. **Difficulty-based decomposition**
   - If any subtask is **≥4/10 difficulty** to learn, break it down further
   - Continue until every chunk is **<4/10 difficulty**
   - Assign Haiku 4.5 subagent to each granular chunk

3. **Resource priority**
   - Focus on **FREE** knowledge sources
   - Note what paid access would cost (for reference only)

4. **Identify prerequisites**
   - "What do I need to know first?"

5. **Define success criteria**
   - "How do I know I've achieved EXPERT MASTERY?"
   - Must be able to answer expert-level questions
   - Must understand edge cases and nuances
   - Must know what professionals know

6. **Depth level**
   - Always **EXPERT MASTERY** (not negotiable)
   - Not "high knowledge" — MASTERY
   - The standard: "Could I teach this to a professional?"

7. **Estimate scope**
   - How many files/documents will this produce?

### Output:
- List of subtopics to research (each to MASTERY level)
- Learning sequence (what order to tackle them)
- Clear definition of "finished/done" at MASTERY level

---

## PHASE 3: RESEARCH

**Purpose:** Find and consume all available knowledge to EXPERT MASTERY level

### Agent Structure:
- 1 Opus 4.5 orchestrator
- Sonnet 4.5 subagents (one per main subtopic)
- Haiku 4.5 sub-subagents (for further breakdown)

### What Happens:

1. **Decomposition (same rules as Phase 2)**
   - Break into manageable subtopic list
   - If ≥4/10 difficulty, break down until <4/10

2. **⚠️ Establish Dependencies**
   - Agents run in **parallel WHERE POSSIBLE**
   - Some must **wait for others to finish** (learning order matters)
   - Orchestrator manages the dependency graph
   - Prerequisites must complete before dependent topics begin

3. **Resource Priority**
   - Focus on **FREE** knowledge sources
   - Note paid access costs (for reference only)

4. **Research Sources (MASTERY-LEVEL ONLY)**
   - Free courses (Harvard, MIT, Stanford, Coursera free tier, YouTube)
   - Free textbooks / PDFs — focus on authoritative sources
   - Professional certifications to target (GIA, bar exam, etc.)
   - Practice materials, exercises, sample tests — including HARD ones
   - Industry-standard tools and terminology
   - **Expert-level content** — not beginner tutorials
   - **Edge cases and exceptions** — what trips up non-experts
   - **Real-world applications** — how practitioners actually use this

5. **Parallel Research**
   - Each subagent researches assigned subtopic to MASTERY
   - Respects dependency graph
   - **Quality bar: Expert Mastery or it doesn't go in**

### Output:
- Organized list of MASTERY-level resources per subtopic
- Prioritized by quality/relevance/depth
- Downloaded/saved where possible

---

## PHASE 4: DOCUMENT

**Purpose:** Turn research into structured, EXPERT MASTERY knowledge

### Agent Structure:
- 1 Opus 4.5 orchestrator
- 3 Opus 4.5 subagents
- 4 Sonnet 4.5 subagents per Opus subagent (12 Sonnet total)

**Total: 4 Opus + 12 Sonnet = 16 agents**

### Goal:
**Insanely well organized, RAG-ready, EXPERT MASTERY content**

### What Happens:

1. Write **README.md** with full curriculum overview
   - Must reflect MASTERY-level depth

2. Create **subtopic files** (one per area)
   - Each file is EXPERT MASTERY level
   - Not summaries — comprehensive mastery content

3. Include **practical exercises and examples**
   - Include HARD examples, not just easy ones
   - Real-world scenarios experts face

4. Add **assessment questions**
   - Expert-level questions, not basic recall
   - "Can I answer these at a MASTERY level?"
   - Include edge cases and trick questions

5. Use **consistent formatting** across all files

6. **Cross-link related topics**
   - Show how expert knowledge connects

7. **Include what separates experts from amateurs**
   - Common mistakes
   - Nuances professionals know
   - "Insider" knowledge

### Output:
- Complete documentation in markdown at EXPERT MASTERY level
- Structured for easy reference
- Ready for RAG ingestion
- **No surface-level content — MASTERY only**

---

## PHASE 5: INTEGRATE

**Purpose:** Load EXPERT MASTERY knowledge into systems for actual use

### Agent Structure:
- 1 Opus 4.5 orchestrator
- 3 Opus 4.5 subagents
- 4 Sonnet 4.5 subagents per Opus subagent (12 Sonnet total)

**Total: 4 Opus + 12 Sonnet = 16 agents**

### Goal:
**Insanely well organized, RAG-ready, EXPERT MASTERY knowledge base**

### What Happens:

1. Add all MASTERY-level documentation to **Frank's RAG system**

2. **Generate embeddings** for semantic search

3. Update **MEMORY.md** with key learnings summary
   - Note this is MASTERY-level knowledge

4. Create **skill file** if appropriate (for OpenClaw skills)

5. **Register in RAG registry** (per standing rule)
   - Tag as EXPERT MASTERY level

6. **Verify search/retrieval works**
   - Test with EXPERT-level queries, not basic ones

### Output:
- EXPERT MASTERY knowledge searchable via RAG
- Memory updated
- Registered and tracked as MASTERY-level content

---

## PHASE 6: VALIDATE

**Purpose:** Confirm EXPERT MASTERY knowledge was captured correctly

### Agent Structure:
- 1 Opus 4.5 orchestrator
- 3 Opus 4.5 subagents
- 4 Sonnet 4.5 subagents per Opus subagent (12 Sonnet total)

**Total: 4 Opus + 12 Sonnet = 16 agents**

### What Happens:

1. **Show summary** of what was created (files, RAG entries, etc.)

2. **Run test queries** against RAG to verify retrieval
   - Use EXPERT-level queries
   - Test edge cases
   - Verify depth of answers

3. **Ask human:**
   - "Did I miss anything?"
   - "Ask me 3-4 EXPERT-LEVEL questions about this topic"
   - "Test me on the hard stuff, not the basics"

4. **Gap Analysis:**
   - Look at real-world use cases EXPERTS would have
   - Test if RAG can answer EXPERT-level questions
   - Check for missing nuances, edge cases, exceptions
   - **If gaps found → go back to school and add MASTERY-level content to RAG**

5. **Mastery Verification:**
   - Could this content pass a professional certification exam?
   - Could this content teach a professional something new?
   - Are the edge cases and exceptions covered?
   - **If NO to any → not done yet**

6. **Allow edits/additions** if needed

7. **Confirm completion** — at MASTERY level

8. **Archive/backup to NAS**

### Output:
- Human sign-off on EXPERT MASTERY level
- Tell human:
  - **Name** of this Brain Dump
  - **Where** it lives in RAG
  - **Branches** of knowledge it contains
  - **Mastery level achieved**
- Backup created
- Brain Dump marked **COMPLETE — EXPERT MASTERY**

---

## Summary: Agent Totals Per Phase

| Phase | Opus 4.5 | Sonnet 4.5 | Haiku 4.5 |
|-------|----------|------------|-----------|
| 1. Capture | — | — | — |
| 2. Decompose | 1 | As needed | As needed |
| 3. Research | 1 | As needed | As needed |
| 4. Document | 4 | 12 | — |
| 5. Integrate | 4 | 12 | — |
| 6. Validate | 4 | 12 | — |

---

## Quality Standard Reminder

**EVERY Brain Dump produces EXPERT MASTERY knowledge.**

| Level | Acceptable? |
|-------|-------------|
| Beginner | ❌ NO |
| Intermediate | ❌ NO |
| Advanced | ❌ NO |
| High Knowledge | ❌ NO |
| Expert | ❌ ALMOST — but not enough |
| **EXPERT MASTERY** | ✅ YES — this is the standard |

The only acceptable output is knowledge at a level where:
- You could pass the hardest professional certification
- You could teach experts something new
- You know the edge cases, exceptions, and nuances
- You understand what separates masters from amateurs

---

## Quick Start

When you want to Brain Dump a new topic:

1. Say: **"Brain Dump: [topic]"**
2. Answer the 3 capture questions
3. Let the swarm work
4. Review and validate at MASTERY level
5. Done — EXPERT MASTERY knowledge is in RAG

---

## Changelog

### v1.1 (February 16, 2026)
- Added CORE PRINCIPLE section emphasizing EXPERT MASTERY
- Updated all phases to explicitly require MASTERY-level content
- Added Quality Standard Reminder section
- Clarified that "high knowledge" is NOT enough — must be MASTERY
- Added mastery verification step to Phase 6

### v1.0 (February 16, 2026)
- Initial release

---

**End of Brain Dump v1.1**
