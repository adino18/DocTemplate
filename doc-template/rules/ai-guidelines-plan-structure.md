---
title: "AI Guidelines: Plan and Plan-Detail Structure"
description: "Specific guidelines for AI agents to understand and properly create plan and plan-detail documentation with correct relationship and hierarchy."
tags: [rules, ai-guidelines, plan-structure]
intent: policy
last_modified: 2025-10-27
schema_version: 1
---

# AI Guidelines: Plan and Plan-Detail Structure

## Purpose

This document provides specific guidelines for AI agents to understand the relationship between `plan/` and `plan-detail/` directories and how to properly create content for each.

## Core Concept: Hierarchy and Relationship

### Plan Directory (`plan/README.md`)
- **Purpose**: High-level project roadmap with phases and major tasks
- **Content**: Brainstorming checklist of general work items organized by phases
- **Scope**: Overview of what needs to be done, not how to do it
- **Audience**: AI agents needing to understand project flow and next steps

### Plan-Detail Directory (`plan-detail/`)
- **Purpose**: Detailed breakdown of specific phases mentioned in plan
- **Content**: Step-by-step implementation details for each phase
- **Scope**: How to execute specific tasks, including dependencies and success criteria
- **Audience**: AI agents implementing specific work items

## Key Relationship Rules

1. **One-to-Many Relationship**: 
   - One phase in `plan/README.md` corresponds to one file in `plan-detail/`
   - Each phase in plan should have a corresponding detail file

2. **Content Hierarchy**:
   - `plan/` contains WHAT needs to be done (general tasks)
   - `plan-detail/` contains HOW to do it (specific steps)

3. **Cross-Reference Requirements**:
   - Each phase in plan must reference its corresponding detail file
   - Each detail file must reference back to the main plan

## Content Creation Guidelines

### When Creating Plan Content (`plan/README.md`)

1. **Phase Structure**:
   ```
   ### Phase X: [Brief Description]
   - [ ] X.1: [High-level task description]
   - [ ] X.2: [High-level task description]
   - [ ] X.3: [High-level task description]
   ```

2. **Task Description Rules**:
   - Keep descriptions brief and action-oriented
   - Focus on WHAT needs to be accomplished, not HOW
   - Group related tasks under the same phase
   - Base phase organization on work volume and logical grouping

3. **Reference Requirements**:
   - Always include reference to corresponding detail file
   - Example: `Refer to [plan-detail/phase-X.md](../plan-detail/phase-X.md) for detailed implementation steps`

### When Creating Plan-Detail Content (`plan-detail/phase-X.md`)

1. **File Structure**:
   ```
   # Phase X: [Detailed Description]
   
   ## X.1: [Detailed Task Description]
   - [Specific step 1]
   - [Specific step 2]
   - [Specific step 3]
   
   ## X.2: [Detailed Task Description]
   - [Specific step 1]
   - [Specific step 2]
   ```

2. **Detail Requirements**:
   - Expand on each task from the corresponding phase in plan
   - Provide actionable steps that can be executed directly
   - Include dependencies, prerequisites, and success criteria
   - Add implementation guidance specific to the task

3. **Reference Requirements**:
   - Always reference back to the main plan file
   - Example: `This file provides detailed breakdown for Phase X as outlined in [plan/README.md](../plan/README.md)`

## Common Mistakes to Avoid

1. **Content Duplication**: Do not repeat the same content in both plan and plan-detail
2. **Level Mismatch**: Don't put implementation details in plan or high-level overview in plan-detail
3. **Missing References**: Always maintain bidirectional references between plan and plan-detail
4. **Inconsistent Numbering**: Ensure task numbers match between plan and plan-detail (e.g., 1.1 in plan corresponds to 1.1 in detail)

## Validation Checklist

Before finalizing plan or plan-detail content:

### For Plan (`plan/README.md`):
- [ ] Each phase has a clear, brief description
- [ ] Tasks are high-level and action-oriented
- [ ] No implementation details included
- [ ] References to corresponding detail files are present
- [ ] Phase organization makes logical sense based on work volume

### For Plan-Detail (`plan-detail/phase-X.md`):
- [ ] File name matches the phase number (e.g., phase-1.md for Phase 1)
- [ ] Content expands on tasks from the corresponding phase
- [ ] Implementation steps are specific and actionable
- [ ] Reference back to main plan is included
- [ ] Dependencies and success criteria are clearly defined

## Examples

### Correct Plan Example:
```
### Phase 1: Project Setup
- [ ] 1.1: Initialize project structure
- [ ] 1.2: Configure development environment
- [ ] 1.3: Set up version control

*Refer to [plan-detail/phase-1.md](../plan-detail/phase-1.md) for detailed implementation steps.*
```

### Correct Plan-Detail Example:
```
# Phase 1: Project Setup

*This file provides detailed breakdown for Phase 1 as outlined in [plan/README.md](../plan/README.md)*

## 1.1: Initialize Project Structure
- Create main project directory
- Set up subdirectories for components, services, and utilities
- Initialize package.json with required dependencies
- Create basic configuration files

## 1.2: Configure Development Environment
- Install development dependencies
- Set up linting and formatting configurations
- Configure build scripts
- Set up debugging environment
```

## References

- [`plan/README.md`](../plan/README.md): Main project plan
- [`plan-detail/README.md`](../plan-detail/README.md): Overview of plan details
- [`../README.md`](../README.md): Documentation structure overview