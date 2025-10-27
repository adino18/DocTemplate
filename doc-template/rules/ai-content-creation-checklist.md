---
title: "AI Content Creation Checklist"
description: "Comprehensive checklist for AI agents to follow when creating plan and plan-detail content."
tags: [rules, ai-guidelines, checklist]
intent: policy
last_modified: 2025-10-27
schema_version: 1
---

# AI Content Creation Checklist

## Purpose

This checklist helps AI agents ensure they create proper plan and plan-detail content that follows the established structure and relationships.

## Pre-Creation Checklist

### Before Creating Any Content
- [ ] Have I read the existing plan and plan-detail files to understand the current structure?
- [ ] Have I reviewed the guidelines in [`ai-guidelines-plan-structure.md`](./ai-guidelines-plan-structure.md)?
- [ ] Have I checked the examples in [`../examples/plan-structure-example.md`](../examples/plan-structure-example.md)?
- [ ] Do I understand the difference between plan (WHAT) and plan-detail (HOW)?

## Plan Content Creation Checklist (`plan/README.md`)

### Structure Requirements
- [ ] Does the file have proper front-matter with intent: plan?
- [ ] Is the content organized into logical phases based on work volume?
- [ ] Does each phase have a clear, brief description?
- [ ] Are tasks numbered consistently (e.g., 1.1, 1.2, 2.1, 2.2)?

### Content Requirements
- [ ] Are task descriptions high-level and action-oriented?
- [ ] Do tasks focus on WHAT needs to be done, not HOW to do it?
- [ ] Are implementation details avoided in plan content?
- [ ] Is the content concise and easy to scan?

### Reference Requirements
- [ ] Does each phase reference its corresponding detail file?
- [ ] Are all references using proper markdown link format?
- [ ] Is there a References section at the end of the file?

### Validation Questions
- [ ] Can someone understand the project flow without reading implementation details?
- [ ] Are phases organized logically based on dependencies and work volume?
- [ ] Is there a clear progression from one phase to the next?

## Plan-Detail Content Creation Checklist (`plan-detail/phase-X.md`)

### Structure Requirements
- [ ] Does the file have proper front-matter with intent: plan-detail?
- [ ] Is the file name correctly formatted (e.g., phase-1.md for Phase 1)?
- [ ] Does the file reference back to the main plan?
- [ ] Are sections numbered to match the corresponding tasks in plan?

### Content Requirements
- [ ] Does each section expand on a specific task from the corresponding phase?
- [ ] Are implementation steps specific and actionable?
- [ ] Are dependencies and prerequisites clearly identified?
- [ ] Are success criteria defined where applicable?

### Reference Requirements
- [ ] Does the file reference back to the main plan?
- [ ] Are all references using proper markdown link format?
- [ ] Is the see_also front-matter property correctly set?

### Validation Questions
- [ ] Can someone implement the tasks using only this document?
- [ ] Are the steps detailed enough to be executed directly?
- [ ] Is there a clear relationship between this file and the corresponding phase in plan?

## Relationship Validation Checklist

### Cross-Reference Validation
- [ ] Does each phase in plan have a corresponding detail file?
- [ ] Do task numbers match between plan and plan-detail?
- [ ] Are references bidirectional (plan → detail, detail → plan)?
- [ ] Is there consistency in terminology between plan and plan-detail?

### Content Hierarchy Validation
- [ ] Does plan contain high-level tasks without implementation details?
- [ ] Does plan-detail contain specific implementation steps?
- [ ] Is there no content duplication between plan and plan-detail?
- [ ] Is the level of detail appropriate for each document type?

## Common Issues to Check

### Content Issues
- [ ] No implementation details in plan
- [ ] No high-level overview in plan-detail
- [ ] No actionable steps in plan-detail
- [ ] No clear progression between phases

### Structure Issues
- [ ] No missing references between files
- [ ] No inconsistent numbering
- [ ] No broken links
- [ ] No missing front-matter properties

### Relationship Issues
- [ ] No orphaned phases (phase in plan without corresponding detail file)
- [ ] No orphaned detail files (detail file without corresponding phase in plan)
- [ ] No mismatched task numbers between plan and plan-detail

## Final Review Checklist

### Before Submitting Content
- [ ] Have I reviewed all checklists above?
- [ ] Have I tested all links to ensure they work correctly?
- [ ] Have I verified that the content follows the established guidelines?
- [ ] Have I ensured that the content is clear, concise, and actionable?

### After Creating Content
- [ ] Have I updated any related files that might be affected by these changes?
- [ ] Have I informed stakeholders about the new or updated content?
- [ ] Have I documented any decisions or assumptions made during creation?

## Quick Reference

### Plan Content Focus
- WHAT needs to be done
- High-level tasks
- Phase organization
- Project flow

### Plan-Detail Content Focus
- HOW to do it
- Specific implementation steps
- Dependencies and prerequisites
- Success criteria

### Key Relationship Rules
- One phase in plan = one file in plan-detail
- Plan references plan-detail for details
- Plan-detail references plan for context
- Consistent numbering between files

## References

- [`ai-guidelines-plan-structure.md`](./ai-guidelines-plan-structure.md): Detailed guidelines for plan structure
- [`../examples/plan-structure-example.md`](../examples/plan-structure-example.md): Complete examples
- [`../plan/README.md`](../plan/README.md): Plan template
- [`../plan-detail/README.md`](../plan-detail/README.md): Plan-detail overview