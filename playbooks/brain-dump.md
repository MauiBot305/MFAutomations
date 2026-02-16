# 🧠 BRAIN DUMP

### A Systematic Process for Teaching AI New Subjects

**Version:** 1.0  
**Created:** February 16, 2026  
**Authors:** Patrick Chinery, Maui  
**Storage:** GitHub (MFAutomations) → Frank (RAG/Knowledge) → NAS (Backups)

---

## Overview

Brain Dump is a structured workflow for teaching an AI a new subject — comprehensively, systematically, and to **BEYOND Expert Level**.

The process uses a multi-agent swarm architecture to decompose, research, document, integrate, and validate knowledge until it's fully captured in a searchable RAG system.

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
   - "How do I know I've learned it?"

6. **Depth level**
   - Always **BEYOND Expert Level** (not negotiable)

7. **Estimate scope**
   - How many files/documents will this produce?

### Output:
- List of subtopics to research
- Learning sequence (what order to tackle them)
- Clear definition of "finished/done"

---

## PHASE 3: RESEARCH

**Purpose:** Find and consume all available knowledge

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

4. **Research Sources**
   - Free courses (Harvard, MIT, Stanford, Coursera free tier, YouTube)
   - Free textbooks / PDFs
   - Professional certifications to target (GIA, bar exam, etc.)
   - Practice materials, exercises, sample tests
   - Industry-standard tools and terminology

5. **Parallel Research**
   - Each subagent researches assigned subtopic
   - Respects dependency graph

### Output:
- Organized list of resources per subtopic
- Prioritized by quality/relevance
- Downloaded/saved where possible

---

## PHASE 4: DOCUMENT

**Purpose:** Turn research into structured, usable knowledge

### Agent Structure:
- 1 Opus 4.5 orchestrator
- 3 Opus 4.5 subagents
- 4 Sonnet 4.5 subagents per Opus subagent (12 Sonnet total)

**Total: 4 Opus + 12 Sonnet = 16 agents**

### Goal:
**Insanely well organized, RAG-ready**

### What Happens:

1. Write **README.md** with full curriculum overview

2. Create **subtopic files** (one per area)

3. Include **practical exercises and examples**

4. Add **assessment questions**
   - "Can I answer these? Then I know it."

5. Use **consistent formatting** across all files

6. **Cross-link related topics**

### Output:
- Complete documentation in markdown
- Structured for easy reference
- Ready for RAG ingestion

---

## PHASE 5: INTEGRATE

**Purpose:** Load knowledge into systems for actual use

### Agent Structure:
- 1 Opus 4.5 orchestrator
- 3 Opus 4.5 subagents
- 4 Sonnet 4.5 subagents per Opus subagent (12 Sonnet total)

**Total: 4 Opus + 12 Sonnet = 16 agents**

### Goal:
**Insanely well organized, RAG-ready**

### What Happens:

1. Add all documentation to **Frank's RAG system**

2. **Generate embeddings** for semantic search

3. Update **MEMORY.md** with key learnings summary

4. Create **skill file** if appropriate (for OpenClaw skills)

5. **Register in RAG registry** (per standing rule)

6. **Verify search/retrieval works**

### Output:
- Knowledge searchable via RAG
- Memory updated
- Registered and tracked

---

## PHASE 6: VALIDATE

**Purpose:** Confirm knowledge was captured correctly

### Agent Structure:
- 1 Opus 4.5 orchestrator
- 3 Opus 4.5 subagents
- 4 Sonnet 4.5 subagents per Opus subagent (12 Sonnet total)

**Total: 4 Opus + 12 Sonnet = 16 agents**

### What Happens:

1. **Show summary** of what was created (files, RAG entries, etc.)

2. **Run test queries** against RAG to verify retrieval

3. **Ask human:**
   - "Did I miss anything?"
   - "Ask me 3-4 questions about the information you need to build your core for the project you had me learn"

4. **Gap Analysis:**
   - Look at real-world use cases people might have
   - Test if RAG can answer these use cases
   - **If gaps found → go back to school and add to RAG**

5. **Allow edits/additions** if needed

6. **Confirm completion**

7. **Archive/backup to NAS**

### Output:
- Human sign-off
- Tell human:
  - **Name** of this Brain Dump
  - **Where** it lives in RAG
  - **Branches** of knowledge it contains
- Backup created
- Brain Dump marked **COMPLETE**

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

## Quick Start

When you want to Brain Dump a new topic:

1. Say: **"Brain Dump: [topic]"**
2. Answer the 3 capture questions
3. Let the swarm work
4. Review and validate
5. Done — knowledge is in RAG

---

**End of Brain Dump v1.0**
