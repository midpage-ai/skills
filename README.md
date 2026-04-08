# Midpage Skills

A collection of public Midpage skills for AI agents. Skills are packaged
instructions and reference material that extend agent capabilities.

Skills follow the [Agent Skills](https://agentskills.io/) format.

## Available Skills

### legal-brief-drafter

Draft and format legal briefs, motions, memoranda, complaints, and appellate
filings using court-specific formatting rules and filing conventions.

**Use when:**
- "draft a brief"
- "write a motion"
- "format this for [court name]"
- "finalize my filing"
- "review this brief and make it filing-ready"

**Workflow covered:**
- Identify the court, judge, and filing type before drafting
- Find the current local rules and judge-specific rules
- Draft or review the filing using the correct structure for that document type
- Apply formatting defaults and docx conventions where rules are silent
- Validate page limits, required sections, and filing readiness before delivery

**Supporting references:**
- `references/court-rules-guide.md` for rule sources, formatting defaults, caption
  conventions, and docx layout patterns

## Installation

Skills are distributed as folders with `SKILL.md` entrypoints.

### Claude Code

```bash
cp -r legal-brief-drafter ~/.claude/skills/
```

### Other skills-compatible agents

Copy the skill folder into the agent's skills directory, or import `SKILL.md`
plus any referenced files according to that client's instructions.

### Midpage MCP

Midpage MCP exposes this skill as:
- Prompt: `legal-brief-drafter`
- Resource: `resource://midpage/skills/legal-brief-drafter`
- Resource: `resource://midpage/skills/legal-brief-drafter/court-rules-guide`

This repository is the canonical source for those MCP-served skill documents.

## Usage

Skills are intended to be loaded on demand when the task matches the skill's
description.

**Examples:**

```text
draft a motion to dismiss for the southern district of new york
```

```text
review this appellate brief and make it filing-ready
```

```text
format this memorandum for delaware chancery court
```

## Skill Structure

Each skill directory may contain:
- `SKILL.md` - the primary instructions for the agent
- `references/` - supporting documentation loaded only when needed
- `scripts/` - helper scripts for automation, if the skill needs them

Current repository contents:
- `legal-brief-drafter/`
- `legal-brief-drafter/references/`
