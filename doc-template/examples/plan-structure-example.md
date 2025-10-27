---
title: "Plan Structure Example"
description: "Reference examples showing proper structure and relationship between plan and plan-detail documentation."
tags: [example, plan-structure, reference, template]
intent: reference
last_modified: 2025-10-27
schema_version: 1
---

# Plan Structure Example

**IMPORTANT**: This document is for REFERENCE ONLY. It provides examples of how plan and plan-detail should be structured and related to each other. Do NOT copy this entire structure to your actual project - use it as a guide for creating your own project-specific documentation.

## Purpose of Examples Directory

The `examples/` directory contains:
- Reference templates and examples for documentation structure
- Illustrations of proper formatting and content organization
- Samples of correct relationships between different document types
- Best practices for creating project documentation

**DO NOT**: Copy the entire examples directory to your actual project
**DO**: Use these examples as reference when creating your own project-specific documentation

## Example Scenario

Let's consider a project to build a web application with user authentication and data management features.

## Plan Example (`plan/README.md`)

```markdown
---
title: "Project Plans"
description: "Overview of project phases, goals, and subtasks for AI agents to follow."
tags: [plan, roadmap, phases]
intent: plan
last_modified: 2025-10-27
schema_version: 1
---

**Important:** This file focuses solely on project plans and required functions. Do not add unrelated content, especially code samples. Only include descriptions of goals, phases, and subtasks.

## Overview
**Keywords:** phases, subtasks, goals, project breakdown, tasks.

**What specific work needs to be done? Break down the project into phases and detailed tasks.**

For each phase, answer:
- What is the goal of this phase?
- What subtasks need to be completed to achieve the goal?

**Note:** For detailed breakdown of each phase, refer to the corresponding files in docs/plan-detail, such as phase-1.md for Phase 1.

### Phase 1: Project Foundation and Setup
- [ ] 1.1: Initialize project structure and configuration
- [ ] 1.2: Set up development environment and tools
- [ ] 1.3: Configure version control and CI/CD pipeline

### Phase 2: Backend Development
- [ ] 2.1: Design and implement database schema
- [ ] 2.2: Create authentication and authorization system
- [ ] 2.3: Develop core API endpoints

### Phase 3: Frontend Development
- [ ] 3.1: Set up frontend framework and routing
- [ ] 3.2: Implement user interface components
- [ ] 3.3: Connect frontend to backend APIs

### Phase 4: Testing and Deployment
- [ ] 4.1: Implement comprehensive testing suite
- [ ] 4.2: Configure production environment
- [ ] 4.3: Deploy application and monitor performance

## References
- [`plan-detail/phase-1.md`](../plan-detail/phase-1.md): Detailed breakdown of Phase 1.
- [`plan-detail/phase-2.md`](../plan-detail/phase-2.md): Detailed breakdown of Phase 2.
- [`plan-detail/phase-3.md`](../plan-detail/phase-3.md): Detailed breakdown of Phase 3.
- [`plan-detail/phase-4.md`](../plan-detail/phase-4.md): Detailed breakdown of Phase 4.
- [`docs/README.md`](../README.md): Main overview of documentation structure.
```

## Plan-Detail Example (`plan-detail/phase-1.md`)

```markdown
---
title: "Phase 1: Project Foundation and Setup"
description: "Detailed breakdown of Phase 1 tasks and steps for project implementation."
tags: [plan, detail, phase-1]
intent: plan-detail
last_modified: 2025-10-27
schema_version: 1
aliases: []
see_also:
  - ../plan/README.md
---

# Phase 1: Project Foundation and Setup

**Important:** This file focuses solely on detailed plans and required functions for Phase 1. Do not add unrelated content, especially code samples. Only include descriptions of goals, steps, and actionable tasks.

**Note:** This file provides detailed breakdown for Phase 1 as outlined in docs/plan/README.md.

**Guidance:** This phase focuses on establishing the technical foundation for the project, including project structure, development environment, and version control setup.

## 1.1: Initialize Project Structure and Configuration

**Guidance:** Set up the basic project directory structure and configuration files needed for development.

- Create main project directory with appropriate naming convention
- Set up subdirectories: src/, tests/, docs/, config/
- Initialize package.json with project metadata and dependencies
- Create configuration files for build tools and development environment
- Set up project documentation structure following established conventions
- Create README.md with project overview and setup instructions

## 1.2: Set Up Development Environment and Tools

**Guidance:** Configure all necessary development tools and environments for team collaboration.

- Install and configure code editor with necessary extensions
- Set up linting and formatting tools (ESLint, Prettier)
- Configure debugging environment and breakpoints
- Set up local development server with hot reload
- Configure environment variables for different deployment stages
- Install and configure database tools for local development
- Set up API testing tools (Postman, Insomnia)

## 1.3: Configure Version Control and CI/CD Pipeline

**Guidance:** Establish version control workflow and automated deployment pipeline.

- Initialize Git repository with appropriate .gitignore
- Set up branching strategy (main, develop, feature branches)
- Configure commit message conventions and hooks
- Set up GitHub/GitLab repository with appropriate permissions
- Configure CI/CD pipeline with automated testing and deployment
- Set up code review process and pull request templates
- Configure automated dependency updates and security scanning
```

## Key Relationship Points

1. **Numbering Consistency**:
   - Phase 1 in plan corresponds to phase-1.md in plan-detail
   - Function 1.1 in plan corresponds to section 1.1 in plan-detail

2. **Content Hierarchy**:
   - Plan states "User registration with email verification" (WHAT function)
   - Plan-detail breaks this down into specific implementation steps like "Create registration form", "Implement email verification service", etc. (HOW to implement)

3. **Cross-References**:
   - Plan references plan-detail files for detailed implementation steps
   - Plan-detail references back to the main plan for context

4. **Level of Detail**:
   - Plan focuses on WHAT functions will be implemented (checklist format)
   - Plan-detail focuses on HOW to implement each function with specific steps

5. **Brainstorming Connection**:
   - Plan functions are derived from brainstorming sessions based on requirements
   - Each function represents a user-facing feature or capability

## Common Mistakes to Avoid

### Incorrect Plan Example (Too Technical):
```markdown
### Phase 1: Backend Setup
- [ ] 1.1: Create database schema with user table
- [ ] 1.2: Implement JWT authentication middleware
- [ ] 1.3: Set up REST API endpoints
```
*Problem: Too technical - these are implementation details, not user-facing functions*

### Incorrect Plan Example (Too Vague):
```markdown
### Phase 1: Authentication
- [ ] 1.1: Set up auth
- [ ] 1.2: Handle users
- [ ] 1.3: Login stuff
```
*Problem: Too vague - doesn't clearly describe what functions will be implemented*

### Correct Plan Example:
```markdown
### Phase 1: User Authentication
- [ ] Function 1.1: User registration with email verification
- [ ] Function 1.2: User login with password reset
- [ ] Function 1.3: Social media login integration
```
*Good: Clear, user-facing functions that can be marked as completed*

### Incorrect Plan-Detail Example:
```markdown
# Phase 1: Project Setup

## Overview
This phase will set up the project structure and development environment.

## Tasks
- Initialize project structure
- Set up development environment
- Configure version control
```
*Problem: Not enough detail - this repeats the plan without providing specific implementation steps*

## References

- [`rules/ai-guidelines-plan-structure.md`](../rules/ai-guidelines-plan-structure.md): Guidelines for creating plan and plan-detail content
- [`plan/README.md`](../plan/README.md): Main project plan template
- [`plan-detail/README.md`](../plan-detail/README.md): Overview of plan details directory