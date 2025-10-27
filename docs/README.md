# Overview

This directory contains all technical documentation and development guidelines for the project. The documentation is organized into key directories to help AI Agents track and execute tasks efficiently.

## Documentation Structure

```
docs/
├── old/                          # Deprecated or archived documentation
├── [`plan/README.md`](./plan/README.md)                         # Project plans and phases (AI Agents follow this)
├── [`plan-detail/phase-1.md`](./plan-detail/phase-1.md)                  # Detailed breakdown of plans
├── [`rules/README.md`](./rules/README.md)                        # Mandatory rules and regulations (AI Agents must adhere)
└── [`reference/README.md`](./reference/README.md)                    # Reference materials and detailed guides (use when needed)
```

## How to Use the Documentation

1. **Read the plan first**: Check `plan/README.md` to understand the next tasks.
2. **Adhere to rules**: Read `rules/README.md` before implementing any features (mandatory regulations and workflows).
3. **Reference materials**: Use `reference/` only for detailed information when necessary (optional guides and best practices).
4. **Avoid old docs**: Do not use files in `old/` as they are outdated.

## Workflow for AI Agents

1. **Read plan**: Check `plan/README.md` for upcoming tasks.
2. **Read rules**: Review relevant rules in `rules/`.
3. **Reference if needed**: Consult `reference/` for detailed info.
4. **Implement**: Follow the defined workflows.
5. **Request confirmation**: After implementation, ask the user if they want to update related documentation (e.g., plans or references). Only update if confirmed to avoid unnecessary revisions.
6. **Update progress**: Update plans upon completion (if confirmed).

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
- All documents in this directory are written in English by default, except for specific documents that require a different language.
- All regulations and rules in this file are of the highest priority and must be followed in every action performed by AI Agents.
