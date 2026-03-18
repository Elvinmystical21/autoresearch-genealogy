# autoresearch-genealogy

Structured prompts, vault templates, and research workflows for AI-assisted genealogy research. Built for Claude Code, adaptable to any AI tool or manual workflow.

This project extracts and generalizes methods developed during a real genealogy research effort that produced 105 files spanning 9 generations across 6 family lines, using Claude Code's autonomous research capabilities.

## Who This Is For

- **Genealogy researchers** who want to use AI to accelerate their family history work without sacrificing source rigor
- **AI/tech enthusiasts** who want a concrete example of autonomous research loops applied to a humanities domain
- **Anyone** who has a box of old photos, a DNA test, and unanswered questions about their family

## Quick Start

1. Clone this repo
2. Copy the `vault-template/` folder into your Obsidian vault (or any markdown editor)
3. Fill in `Family_Tree.md` with what you already know (start with yourself, work backward)
4. Scan any physical documents you have (certificates, photos, letters)
5. Open Claude Code, paste the contents of `prompts/01-tree-expansion.md`, and run it
6. Review the results, then run `prompts/02-cross-reference-audit.md` to verify

See `workflows/getting-started.md` for the full walkthrough.

## What's Included

### Prompts (`prompts/`)

Autoresearch prompts designed for Claude Code's `/autoresearch` command. Each prompt defines a Goal, Metric, Direction, Verify condition, Guard rails, Iterations, and Protocol. They run autonomously, making web searches, updating your vault, and verifying their own work.

| Prompt | Purpose |
|---|---|
| 01-tree-expansion | Push every branch of your family tree as far back as possible using web research |
| 02-cross-reference-audit | Find and fix every discrepancy between your family tree and source documents |
| 03-findagrave-sweep | Locate Find a Grave memorials for every deceased ancestor |
| 04-gedcom-completeness | Ensure your GEDCOM file matches your vault data |

### Vault Template (`vault-template/`)

A starter kit for organizing your genealogy research in Obsidian. Plain markdown with YAML frontmatter, readable anywhere. Includes:

- **Core files**: Family tree, research log, open questions tracker, data inventory, timeline
- **Templates**: Person files, document transcriptions, regional research notes

### Reference Guides (`reference/`)

Methodology documents covering confidence tiers, source hierarchies, DNA interpretation guardrails, and the case for using autonomous AI loops in genealogy research.

### Workflows (`workflows/`)

Step-by-step guides for common research tasks: getting started with your first research session, running an OCR pipeline for scanned documents.

## Philosophy

**Structured autonomous research with mechanical verification, not AI guessing.**

Genealogy is different from most AI tasks. There is no compiler. Sources disagree with each other. Confidence is probabilistic, not binary. A name that appears as "Sakkarias" in one record and "Zacharias" in another might both be correct. A date listed as 1820 in one source and 1925 in another is almost certainly wrong somewhere.

The autoresearch approach adapts to this by:

- **Defining measurable metrics** (count of sourced claims, count of resolved questions, count of remaining discrepancies)
- **Requiring verification after every iteration** (cross-reference audit, not just accumulation)
- **Logging negative results** (what you searched for and did not find is as important as what you found)
- **Maintaining confidence tiers** (Strong Signal / Moderate Signal / Speculative) rather than treating all claims as equal

This is inspired by Andrej Karpathy's autoresearch concept: autonomous goal-directed loops where the AI modifies, verifies, keeps or discards, and repeats. Applied to genealogy, the "compiler" is replaced by cross-referencing independent sources.

## License

MIT. See `LICENSE`.

## Contributing

Contributions welcome. If you have prompts, workflows, or archive guides that worked for your research, open a PR. Please ensure all examples use placeholder names (no real family data).
