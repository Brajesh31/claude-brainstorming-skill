# Claude Brainstorming Skill

A structured discovery and design skill for clarifying what a user actually wants before creative or implementation work begins. It guides a conversation from initial intent through alternatives, a written design, and approval before building.

## What It Covers

- **Requirements discovery:** Identify goals, motivations, constraints, and success criteria.
- **Project context:** Inspect existing code, documents, and prior decisions before asking questions.
- **Approach comparison:** Present and evaluate two or three viable approaches, including trade-offs.
- **Design playback:** Summarize understood requirements and identify gaps for correction.
- **Design documentation:** Produce a short design for a small change or a fuller design document for a project.
- **Approval gate:** Require approval of the design before implementation proceeds.
- **Planning handoff:** Connect approved project designs to implementation planning.
- **Mockups and spikes:** Use small exploratory artifacts when they help resolve uncertainty.

## Installation

Clone this repository into your Claude skills directory:

```bash
git clone https://github.com/Brajesh31/claude-brainstorming-skill.git ~/.claude/skills/brainstorming
```

## Using the Skill

Example request:

```text
Use the brainstorming skill to help define a new application.
Start by understanding the goal, inspect the available project context,
compare approaches, and prepare a design before implementation.
```

The skill is designed to run before substantial creative or build work. It asks one focused question at a time when information is missing, and it avoids asking for details already available in the project or supplied context.

## Operating Principle

The central rule is that implementation must not begin until the proposed design has been approved. Reading, exploration, and explicitly agreed exploratory mockups or throwaway spikes can happen earlier, but retaining or extending a spike becomes implementation work and returns to the approval gate.

## Repository Resources

- [SKILL.md](SKILL.md) contains the full discovery process, conversation guidance, design workflow, hard gate, and red flags.
- `references/builder-check.md` provides the builder review checklist used for project design documents.

## Good Practices

Keep user requirements distinct from proposed assumptions, document trade-offs, and preserve unresolved decisions. For small fully specified tasks, follow the skill's stated exception rather than adding unnecessary discovery steps.
