---
title: "Documentation Overview"
description: "Structure, rules, and authoring conventions optimized for AI Agents to find and use docs with minimal context."
tags: [docs, index, ai-agent, conventions]
intent: overview
last_modified: 2025-10-27
schema_version: 1
---

# Overview

This directory contains all technical documentation and development guidelines for the project. The documentation is organized into key directories to help AI Agents track and execute tasks efficiently.

## Documentation Structure

```
docs/
├── old/                          # Deprecated or archived documentation
├── examples/                      # Reference examples and templates (DO NOT copy to actual project)
├── [`plan/README.md`](./plan/README.md)                         # Project plans and phases (AI Agents follow this)
├── [`plan-detail/README.md`](./plan-detail/README.md)                  # Detailed breakdown of plans (AI Agents check for specifics)
├── [`plan-detail/phase-1.md`](./plan-detail/phase-1.md)                  # Detailed breakdown of Phase 1
├── [`rules/README.md`](./rules/README.md)                        # Mandatory rules and regulations (AI Agents must adhere)
└── [`reference/README.md`](./reference/README.md)                    # Reference materials and detailed guides (use when needed)
```

## Authoring and Retrieval Conventions
- Front-matter (required on every .md):
  - title, description (1–2 sentences), tags, intent, last_modified, schema_version
  - optional: aliases (array of alternate names), see_also (array of links)
- Naming:
  - kebab-case; prefix with category: plan-*, plan-detail-*, rules-*, reference-*, guide-* (if applicable)
  - examples: plan-phase-2.md, rules-contribution.md, reference-api-auth.md
- Chunking:
  - default: 600–1000 tokens per section (conservative, model-agnostic)
  - short-context models (≤8k tokens): 400–800 tokens per section
  - long-context models (≥32k tokens): you may increase to 1200–2000 tokens when content is cohesive
  - very-long-context models (≥200k tokens, e.g., 204,800): 1500–3000 tokens per section; cap a single file at ~6k–12k and prefer linking over oversized sections
  - rule of thumb: target ~0.5%–1.5% of the model’s context window per section
  - keep semantic boundaries; add headings every 3–5 paragraphs
  - start each file with a 1–2 sentence summary for quick skim
- Cross-linking:
  - link related docs via a short “See also” list; avoid content duplication
- Directory-first organization:
  - Keep the current folder tree; do not flatten files.
  - Each directory should have its own README.md with front-matter that sets default tags/intent for files inside.
  - Subfolders may refine or override these defaults in their own README.md.
- Directory-to-intent/tag hints (non-destructive defaults):
  - plan → intent: plan, tags: [plan, roadmap]
  - plan-detail → intent: plan-detail, tags: [plan, detail]
  - rules → intent: policy, tags: [rules, process]
  - reference → intent: reference, tags: [api, howto, guide]
  - old → intent: archive, tags: [deprecated]
  - Note: Nested directories inherit the nearest parent directory defaults unless overridden by their own README front-matter.

## How to Use the Documentation

1. **Read the plan first**: Check `plan/README.md` to understand the next tasks.
2. **Adhere to rules**: Read `rules/README.md` before implementing any features (mandatory regulations and workflows).
3. **Reference materials**: Use `reference/` only for detailed information when necessary (optional guides and best practices).
4. **Avoid old docs**: Do not use files in `old/` as they are outdated.

## Workflow for AI Agents (Must follow)

**CRITICAL**: AI agents MUST follow the exact sequence outlined below. Do not skip steps or change the order.

Follow the complete workflow process outlined in [`rules/ai-workflow-process.md`](./rules/ai-workflow-process.md) and use the mandatory checklist in [`rules/ai-workflow-checklist.md`](./rules/ai-workflow-checklist.md):

1. **Receive Requirements**: Understand and document initial requirements from the user.
2. **High-Level Planning**: Create ONLY the high-level plan in [`plan/README.md`](./plan/README.md).
3. **User Review**: Get user approval on high-level plan BEFORE creating detailed plans.
4. **Detailed Planning**: Only after approval, create detailed plans in [`plan-detail/`](./plan-detail/) directory.
5. **User Review**: Get user approval on detailed plans.
6. **Implementation**: Execute tasks according to approved plans.
7. **User Evaluation**: Get user feedback on implemented functionality.
8. **Documentation Update**: Update documentation to reflect actual implementation (with user confirmation) or adjust functionality if requested.
9. **Repeat**: Continue the cycle for additional features or improvements.

**IMPORTANT SEQUENCE RULES**:
- Always read requirements from [`reference/requirement.md`](./reference/requirement.md) first
- Create high-level plan BEFORE detailed plans
- Get user approval at each review stage
- Do NOT proceed to next step without explicit user approval

For specific guidance on creating plan and plan-detail documents, refer to:
- [`rules/ai-workflow-process.md`](./rules/ai-workflow-process.md): Complete workflow process with mandatory checklist
- [`rules/ai-guidelines-plan-structure.md`](./rules/ai-guidelines-plan-structure.md)
- [`rules/ai-content-creation-checklist.md`](./rules/ai-content-creation-checklist.md)
- [`examples/plan-structure-example.md`](./examples/plan-structure-example.md): Reference examples for plan and plan-detail structure (DO NOT copy to actual project).

## AI Agent Retrieval Tips
- Prefer files whose front-matter intent/tags match your task before reading full content.
- Read only the front-matter description and the first section to decide relevance.
- Use directory intent hints to narrow search; avoid old/ unless explicitly required.

## Search (manifest optional)
- Primary: rely on per-file front-matter and directory defaults for discovery.
- Optional: create docs/manifest.json only if you need a machine index for external search/embeddings.
- Default policy: do not create or maintain a manifest unless explicitly requested.
- If created later: index metadata only (no full content) and regenerate on add/rename/remove or front-matter changes.

## Maintenance

### Regular Updates
- Plans are updated per phase.
- Rules are updated when processes change.
- References are updated for technical changes.

### Quality Assurance
- Ensure documentation is consistent and readable.
- Check for broken links and references.
- Keep docs in sync with current code.

## General Rules
- **LANGUAGE REQUIREMENT**: All documents MUST be written in English by default, except for specific documents that explicitly require a different language.
- **NO VIETNAMESE CONTENT**: Do NOT write content in Vietnamese unless specifically requested for that particular document.
- **ENGLISH TEMPLATES**: Use the English templates provided in this directory as the basis for all new documents.
- All regulations and rules in this file are of the highest priority and must be followed in every action performed by AI Agents.

## Documentation Management Rules
- When adding or updating documentation, identify the correct directory and file (e.g., `plan/` for tasks and phases, `rules/` for guidelines, `reference/` for detailed guides). Update only the relevant file to avoid duplication.
- Avoid adding the same content in multiple files. If content overlaps, consolidate it into the most appropriate location and reference it from other files if needed.
- Before updating, check for existing similar content in other directories to ensure consistency and prevent redundancy.
- After updates, verify links and references to maintain documentation integrity.

## References
- [`plan/README.md`](./plan/README.md): Project plans and phases.
- [`plan-detail/README.md`](./plan-detail/README.md): Overview of plan details directory.
- [`rules/README.md`](./rules/README.md): Mandatory rules and regulations.
- [`reference/README.md`](./reference/README.md): Reference materials and guides.
- [`old/README.md`](./old/README.md): Archived documentation.
- [`plan-detail/phase-1.md`](./plan-detail/phase-1.md): Detailed breakdown of Phase 1.
- [`rules/ai-workflow-process.md`](./rules/ai-workflow-process.md): Complete workflow process with mandatory checklist.
- [`rules/ai-guidelines-plan-structure.md`](./rules/ai-guidelines-plan-structure.md): Guidelines for AI agents on plan and plan-detail structure.
- [`rules/ai-content-creation-checklist.md`](./rules/ai-content-creation-checklist.md): Checklist for AI agents when creating content.
- [`examples/plan-structure-example.md`](./examples/plan-structure-example.md): Reference examples for plan and plan-detail structure (for reference only).

## Front-matter template (copy/paste)
```yaml
title: "Short, specific title"
description: "One-sentence summary that states purpose and scope."
tags: [tag1, tag2]
intent: plan|plan-detail|policy|reference|overview
last_modified: "YYYY-MM-DD"
schema_version: 1
aliases: []
see_also:
  - ./reference/README.md
```

## Per-directory README front-matter (template)
```yaml
title: "Directory: <name>"
description: "Scope and default metadata for files in this directory."
tags: [<default-tag-1>, <default-tag-2>]
intent: <default-intent-for-this-directory>
last_modified: "YYYY-MM-DD"
schema_version: 1
# These defaults describe typical content inside; individual files can override.
```
