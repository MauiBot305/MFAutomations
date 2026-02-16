# Claude Code Integration for Brain Dump

## Setup Instructions for Adrien

### Option 1: Add to your CLAUDE.md (Recommended)

Add this section to your `~/.claude/CLAUDE.md` or project `CLAUDE.md`:

```markdown
## Brain Dump Process

When the user says any of these:
- "Brain Dump: [topic]"
- "Let's do a Brain Dump on [topic]"
- "Brain Dump [topic]"
- "I need a Brain Dump for [topic]"

Follow the Brain Dump playbook at: `~/MFAutomations/playbooks/brain-dump.md`

This is a 6-phase systematic process for learning any subject to BEYOND Expert Level:
1. CAPTURE - Get topic, goal, and templates
2. DECOMPOSE - Break into subtopics (<4/10 difficulty each)
3. RESEARCH - Find free resources, establish dependencies
4. DOCUMENT - Create RAG-ready markdown (16 agents)
5. INTEGRATE - Load into RAG system (16 agents)
6. VALIDATE - Gap analysis and human sign-off (16 agents)

Storage:
- Knowledge/RAG: Frank @ /Users/adrienbird/knowledge/
- Backups: NAS @ 192.168.0.251:/shared/backups/
```

### Option 2: Clone the Repo

```bash
cd ~
git clone git@github.com:MauiBot305/MFAutomations.git
```

Then reference it when needed:
> "Read ~/MFAutomations/playbooks/brain-dump.md and follow it for [topic]"

### Option 3: Quick Reference

Just tell Claude Code:

> "I'm going to do a Brain Dump. The process is:
> 1. Ask me: What topic? What's the goal? Any templates?
> 2. Break into subtopics (each <4/10 difficulty)
> 3. Research free resources (Harvard, MIT, YouTube, etc.)
> 4. Document everything in markdown for RAG
> 5. Integrate into the RAG system on Frank
> 6. Validate with gap analysis
> 
> Start with the topic: [topic]"

---

## Full Playbook Location

GitHub: https://github.com/MauiBot305/MFAutomations/blob/main/playbooks/brain-dump.md

Local (after clone): `~/MFAutomations/playbooks/brain-dump.md`

Frank mirror: `/Users/adrienbird/MFAutomations/playbooks/brain-dump.md`
