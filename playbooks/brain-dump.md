# 🧠 BRAIN DUMP

### A Systematic Process for Teaching AI New Subjects

**Version:** 1.2  
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

---

## ⚡ TOKEN CONSCIOUSNESS

Brain Dump achieves EXPERT MASTERY while being cost-efficient.

### Available Cloud Models (API)

The orchestrator has access to these models and should route tasks to the cheapest capable option:

#### Anthropic
| Model | Alias | Tier | Best For |
|-------|-------|------|----------|
| claude-opus-4-6 | `opus` | 💎 Premium | Complex reasoning, final QA, orchestration |
| claude-opus-4-5 | — | 💎 Premium | Complex reasoning, orchestration |
| claude-sonnet-4-5 | `sonnet` | 🔷 Mid | Research, synthesis, writing |
| claude-haiku-4-5 | — | 🟢 Budget | Simple tasks, formatting, chunking |

#### OpenAI
| Model | Alias | Tier | Best For |
|-------|-------|------|----------|
| gpt-5.3-codex | — | 💎 Premium | Code generation |
| gpt-5.3-codex-spark | — | 💎 Premium | Code with creativity |
| gpt-5.2-pro | — | 💎 Premium | Complex reasoning |
| gpt-5.2 | `gpt` | 🔷 Mid | General tasks |
| gpt-5.1 | — | 🔷 Mid | General tasks |
| gpt-5 | — | 🔷 Mid | General tasks |
| gpt-5.2-codex | — | 🔷 Mid | Code tasks |
| gpt-4o | — | 🟢 Budget | Simple tasks, fast |

#### Google
| Model | Alias | Tier | Best For |
|-------|-------|------|----------|
| gemini-3-pro-preview | `gemini` | 🔷 Mid | Research, long context |
| gemini-2.5-pro | — | 🔷 Mid | General tasks |
| gemini-3-flash-preview | `gemini-flash` | 🟢 Budget | Fast, cheap, simple tasks |
| gemini-2.5-flash | — | 🟢 Budget | Fast, simple tasks |
| gemini-1.5-pro | — | 🟢 Budget | Long context, cheap |

#### Other
| Model | Alias | Tier | Best For |
|-------|-------|------|----------|
| kimi-coding/k2p5 | `Kimi K2.5` | 🔷 Mid | Coding tasks |

### Routing Rules

```
TASK COMPLEXITY          →  MODEL TIER
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
Simple (formatting, chunking)     →  🟢 Budget (Haiku, GPT-4o, Gemini Flash)
Medium (research, writing)        →  🔷 Mid (Sonnet, GPT-5.2, Gemini Pro)
Complex (orchestration, QA)       →  💎 Premium (Opus) — USE SPARINGLY
```

### Cost Tiers (Approximate)
| Tier | Cost/Run | When to Use |
|------|----------|-------------|
| 🟢 Budget | ~$0.01-0.05 | Default for most tasks |
| 🔷 Mid | ~$0.10-0.20 | When quality matters |
| 💎 Premium | ~$0.50-1.00 | Only orchestration + final QA |

### Token Budget Per Phase
| Phase | Budget | Alert At |
|-------|--------|----------|
| Decompose | 50k | 40k |
| Research | 200k | 150k |
| Document | 150k | 120k |
| Integrate | 50k | 40k |
| Validate | 50k | 40k |
| **TOTAL** | **500k** | **390k** |

**NO PAUSES** — Alert at threshold, keep going. Only stop if human explicitly says stop.

### Default Worker Model

**Gemini 3 Pro (`gemini`)** is the default for all worker agents unless the orchestrator explicitly assigns a different model.

- Orchestrator runs on Opus (complex coordination)
- Workers default to Gemini 3 Pro (cost-effective, good quality)
- Orchestrator CAN override and assign Sonnet/Haiku/etc. when needed

### Before Any Task
1. ✅ Check existing RAG — don't re-learn what we know
2. ✅ Check if another agent covered it — no duplicates
3. ✅ Route to cheapest capable model
4. ✅ Batch related tasks when possible

---

## 🗂️ RAG REGISTRY REQUIREMENT

**MANDATORY: Update the RAG Registry every time new knowledge is added.**

After ANY Brain Dump (or any phase that adds to the RAG):

1. Update `memory/rag-registry.md` with:
   - New branch name
   - What it contains
   - Routing keywords
   - Size/document count
   
2. No exceptions — if it's not in the registry, it can't be found.

3. Registry format:
```markdown
## [Branch Name]
- **Purpose:** What this knowledge covers
- **Location:** Path on Frank
- **Documents:** Count
- **Keywords:** routing, keywords, for, queries
- **Created:** Date
- **Brain Dump:** Name of the Brain Dump that created it
```

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
| **Playbooks/Workflows (mirror)** | Frank: `/Users/motherfuckingpatrick/MFAutomations/` | Frank, Maui, Adrien's machines |
| **Knowledge Bases & RAGs** | Frank: `/Users/adrienbird/knowledge/` | Frank, Maui, Adrien's machines |
| **RAG Registry** | `memory/rag-registry.md` | All agents |
| **Backups & Archives** | NAS: `192.168.0.251:/shared/backups/` | Everyone on network |

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
- 1 Opus orchestrator (💎 Premium — justified for coordination)
- Route subtasks to 🟢 Budget or 🔷 Mid models

### What Happens:

1. **Break topic into subtopics**
   - Create manageable list (e.g., "Law" → 10 lawyer types)

2. **Difficulty-based decomposition**
   - If any subtask is **≥4/10 difficulty** to learn, break it down further
   - Continue until every chunk is **<4/10 difficulty**
   - Assign tasks to cheapest capable model

3. **Resource priority**
   - Focus on **FREE** knowledge sources
   - Note what paid access would cost (for reference only)

4. **Identify prerequisites**
   - "What do I need to know first?"

5. **Define success criteria**
   - "How do I know I've achieved EXPERT MASTERY?"

6. **Depth level**
   - Always **EXPERT MASTERY** (not negotiable)

7. **Estimate scope & cost**
   - How many files/documents will this produce?
   - Estimated token budget

### Output:
- List of subtopics to research (each to MASTERY level)
- Learning sequence (what order to tackle them)
- Model assignments (which model handles what)
- Estimated token cost

---

## PHASE 3: RESEARCH

**Purpose:** Find and consume all available knowledge to EXPERT MASTERY level

### Agent Structure:
- 1 Opus orchestrator (💎 Premium)
- Route research tasks to 🔷 Mid models (Sonnet, GPT-5.2, Gemini Pro)
- Route simple lookups to 🟢 Budget models

### What Happens:

1. **Check existing RAG first**
   - Don't research what we already know
   - Build on existing knowledge

2. **Decomposition (same rules as Phase 2)**
   - Break into manageable subtopic list
   - If ≥4/10 difficulty, break down until <4/10

3. **⚠️ Establish Dependencies**
   - Agents run in **parallel WHERE POSSIBLE**
   - Some must **wait for others to finish** (learning order matters)
   - Orchestrator manages the dependency graph

4. **Resource Priority**
   - Focus on **FREE** knowledge sources
   - Note paid access costs (for reference only)

5. **Research Sources (MASTERY-LEVEL ONLY)**
   - Free courses (Harvard, MIT, Stanford, Coursera free tier, YouTube)
   - Free textbooks / PDFs — focus on authoritative sources
   - Professional certifications to target
   - Practice materials, exercises, sample tests — including HARD ones
   - Expert-level content — not beginner tutorials

6. **Parallel Research with Smart Routing**
   - 🔷 Mid models do the heavy research
   - 🟢 Budget models handle formatting, summarizing
   - 💎 Premium only for orchestration

### Output:
- Organized list of MASTERY-level resources per subtopic
- Prioritized by quality/relevance/depth
- Downloaded/saved where possible
- Token usage report

---

## PHASE 4: DOCUMENT

**Purpose:** Turn research into structured, EXPERT MASTERY knowledge

### Agent Structure:
- 1 Opus orchestrator (💎 Premium)
- 🔷 Mid models for writing (Sonnet, GPT-5.2)
- 🟢 Budget models for formatting, cross-linking

### Goal:
**Insanely well organized, RAG-ready, EXPERT MASTERY content**

### What Happens:

1. Write **README.md** with full curriculum overview

2. Create **subtopic files** (one per area)
   - Each file is EXPERT MASTERY level

3. Include **practical exercises and examples**
   - Include HARD examples, not just easy ones

4. Add **assessment questions**
   - Expert-level questions, not basic recall

5. Use **consistent formatting** across all files

6. **Cross-link related topics**

7. **Include what separates experts from amateurs**

### Output:
- Complete documentation in markdown at EXPERT MASTERY level
- Structured for easy reference
- Ready for RAG ingestion
- Token usage report

---

## PHASE 5: INTEGRATE

**Purpose:** Load EXPERT MASTERY knowledge into systems for actual use

### Agent Structure:
- 1 Opus orchestrator (💎 Premium)
- 🟢 Budget models for embedding, indexing

### What Happens:

1. Add all MASTERY-level documentation to **Frank's RAG system**

2. **Generate embeddings** for semantic search

3. Update **MEMORY.md** with key learnings summary

4. Create **skill file** if appropriate (for OpenClaw skills)

5. **🗂️ UPDATE RAG REGISTRY** (MANDATORY)
   - Add new branch to `memory/rag-registry.md`
   - Include: purpose, location, doc count, keywords, date

6. **Verify search/retrieval works**
   - Test with EXPERT-level queries

### Output:
- EXPERT MASTERY knowledge searchable via RAG
- Memory updated
- **RAG Registry updated** ✅
- Registered and tracked

---

## PHASE 6: VALIDATE

**Purpose:** Confirm EXPERT MASTERY knowledge was captured correctly

### Agent Structure:
- 1 Opus orchestrator (💎 Premium)
- 🔷 Mid models for gap analysis (Sonnet)

### What Happens:

1. **Show summary** of what was created (files, RAG entries, tokens used, cost)

2. **Run test queries** against RAG to verify retrieval
   - Use EXPERT-level queries
   - Test edge cases

3. **Ask human:**
   - "Did I miss anything?"
   - "Ask me 3-4 EXPERT-LEVEL questions about this topic"

4. **Gap Analysis:**
   - Look at real-world use cases EXPERTS would have
   - Test if RAG can answer EXPERT-level questions
   - **If gaps found → go back to school and add to RAG**

5. **Mastery Verification:**
   - Could this content pass a professional certification exam?
   - Could this content teach a professional something new?
   - **If NO → not done yet**

6. **Verify RAG Registry is updated**

7. **Confirm completion**

8. **Archive/backup to NAS**

### Output:
- Human sign-off on EXPERT MASTERY level
- Tell human:
  - **Name** of this Brain Dump
  - **Where** it lives in RAG
  - **Branches** of knowledge it contains
  - **RAG Registry entry** confirmed
  - **Total tokens used**
  - **Total cost**
- Backup created
- Brain Dump marked **COMPLETE — EXPERT MASTERY**

---

## Summary: Model Routing Per Phase

**Default Worker Model: Gemini 3 Pro (`gemini`)**

Orchestrator can override when needed.

| Phase | Orchestrator | Default Workers | Override When |
|-------|--------------|-----------------|---------------|
| 1. Capture | — | — | — |
| 2. Decompose | 💎 Opus | 🔷 Gemini Pro | Complex logic → Sonnet |
| 3. Research | 💎 Opus | 🔷 Gemini Pro | Deep synthesis → Sonnet |
| 4. Document | 💎 Opus | 🔷 Gemini Pro | Technical writing → Sonnet |
| 5. Integrate | 💎 Opus | 🔷 Gemini Pro | Simple tasks → Gemini Flash |
| 6. Validate | 💎 Opus | 🔷 Gemini Pro | Final QA → Sonnet |

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

---

## Quick Start

When you want to Brain Dump a new topic:

1. Say: **"Brain Dump: [topic]"**
2. Answer the 3 capture questions
3. Let the swarm work (token-conscious routing)
4. Review and validate at MASTERY level
5. Confirm RAG Registry is updated
6. Done — EXPERT MASTERY knowledge is in RAG

---

## Changelog

### v1.2 (February 16, 2026)
- Added TOKEN CONSCIOUSNESS section with full model inventory
- Added model routing rules (Budget → Mid → Premium)
- Added token budgets per phase
- Added RAG REGISTRY REQUIREMENT (mandatory updates)
- Updated all phases with model routing guidance
- Added cost tracking to outputs

### v1.1 (February 16, 2026)
- Added CORE PRINCIPLE section emphasizing EXPERT MASTERY
- Updated all phases to explicitly require MASTERY-level content
- Added Quality Standard Reminder section

### v1.0 (February 16, 2026)
- Initial release

---

**End of Brain Dump v1.2**
