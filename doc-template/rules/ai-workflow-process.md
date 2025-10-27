---
title: "AI Workflow Process"
description: "Complete workflow process for AI agents from ideation to implementation and documentation updates."
tags: [rules, ai-workflow, process]
intent: policy
last_modified: 2025-10-27
schema_version: 1
---

# AI Workflow Process

## Purpose

This document outlines the complete workflow process that AI agents should follow when working on projects, from initial ideation to implementation and documentation updates.

## Complete Workflow Overview

```
1. Receive Requirements → 2. High-Level Planning → 3. User Review →
4. Detailed Planning → 5. User Review → 6. Implementation →
7. User Evaluation → 8. Documentation Update → 9. Repeat as needed
```

## Critical Workflow Sequence (MUST FOLLOW)

**IMPORTANT**: AI agents MUST follow this exact sequence. Do not skip steps or change the order:

1. **REQUIREMENTS FIRST**: Always start by reading and understanding requirements from [`reference/requirement.md`](../reference/requirement.md)
2. **HIGH-LEVEL PLAN**: Create only the high-level plan in [`plan/README.md`](../plan/README.md) first
3. **USER APPROVAL**: Get explicit user approval on the high-level plan BEFORE creating detailed plans
4. **DETAILED PLANS**: Only after user approval, create detailed plans in [`plan-detail/`](../plan-detail/) directory
5. **CONTINUE**: Proceed with implementation only after both high-level and detailed plans are approved

**DO NOT**:
- Create detailed plans before getting approval on high-level plan
- Skip the user review step between high-level and detailed planning
- Work on multiple documentation directories simultaneously in the wrong order
- Copy structure from doc-template to docs before following the proper workflow

## Detailed Workflow Steps

### Step 1: Receive Requirements

**Objective**: Understand and document the initial requirements from the user.

**Process**:
1. **Gather Requirements**
   - Receive and document user requirements
   - Ask clarifying questions to ensure understanding
   - Document all constraints, assumptions, and success criteria

2. **Confirm Understanding**
   - Summarize requirements back to the user for confirmation
   - Identify any ambiguities or missing information
   - Get user approval that requirements are correctly understood

**Deliverables**: Confirmed and documented requirements

### Step 2: High-Level Ideation

**Objective**: Generate and brainstorm high-level functional concepts based on requirements.

**Process**:
1. **Brainstorm Functions**
   - Generate high-level functional concepts to meet requirements
   - Consider different approaches and architectural patterns
   - Evaluate feasibility and complexity of each approach

2. **Create High-Level Overview**
   - Document the main functional areas and features
   - Create rough sketches or diagrams if helpful
   - Identify major components and their relationships

3. **Present to User**
   - Present the high-level functional concepts to the user
   - Explain the rationale behind each approach
   - Get user feedback and approval on the direction

**Deliverables**: User-approved high-level functional concept

### Step 3: User Review (High-Level Concepts)

**Objective**: Get user feedback and approval on the high-level functional concepts.

**Process**:
1. **Present Concepts**
   - Share the high-level functional concepts with the user
   - Explain the benefits and trade-offs of each approach
   - Highlight how each concept meets the requirements

2. **Collect Feedback**
   - Listen carefully to user preferences and concerns
   - Document all feedback for consideration
   - Ask clarifying questions if needed

3. **Iterate if Necessary**
   - Modify concepts based on user feedback
   - Address any concerns or issues raised
   - Re-present updated concepts until approved

**Deliverables**: User-approved high-level functional concept

### Step 4: Planning

**Objective**: Create comprehensive project plans and detailed implementation steps.

**Process**:
1. **Create High-Level Plan** ([`plan/README.md`](../plan/README.md))
   - Break down the project into logical phases based on work volume
   - Define high-level tasks for each phase
   - Follow guidelines in [`ai-guidelines-plan-structure.md`](./ai-guidelines-plan-structure.md)
   - Use checklist in [`ai-content-creation-checklist.md`](./ai-content-creation-checklist.md)

2. **Create Detailed Plans** ([`plan-detail/`](../plan-detail/))
   - Create detailed breakdown for each phase
   - Provide specific implementation steps
   - Include dependencies and success criteria
   - Ensure proper cross-references with main plan

3. **Create Additional Related Documents**
   - Create any other necessary documentation (e.g., technical specifications, API documentation)
   - Ensure all documents are properly cross-referenced
   - Follow established documentation standards

4. **Review Plan Structure**
   - Verify all relationships between plan and plan-detail
   - Check for consistency in numbering and terminology
   - Ensure all references are correct

**Deliverables**: Complete plan, plan-detail, and related documentation

### Step 5: User Review (Plans and Documentation)

**Objective**: Get user feedback and approval on the created plans and documentation.

**Process**:
1. **Present Plans and Documentation**
   - Share the complete plan, plan-detail, and related documents with the user
   - Highlight key phases and critical dependencies
   - Explain the rationale behind the proposed approach

2. **Collect Feedback**
   - Listen carefully to user concerns and suggestions
   - Document all feedback for consideration
   - Ask clarifying questions if needed

3. **Iterate if Necessary**
   - Modify plans and documentation based on user feedback
   - Address any concerns or issues raised
   - Re-present updated plans until approved

**Deliverables**: User-approved plans and documentation

### Step 6: Implementation

**Objective**: Implement the functionality according to the approved plans.

**Process**:
1. **Preparation**
   - Review [`rules/README.md`](./README.md) for development guidelines
   - Set up development environment as needed
   - Review relevant reference materials

2. **Implementation by Phase**
   - Follow the sequence defined in the approved plan
   - Refer to corresponding plan-detail for specific steps
   - Adhere to coding standards and best practices
   - Test each component as it's implemented

3. **Progress Tracking**
   - Mark completed tasks in the plan
   - Document any deviations from the original plan
   - Note any issues or challenges encountered

**Deliverables**: Implemented functionality according to specifications

### Step 7: User Evaluation

**Objective**: Get user feedback on the implemented functionality.

**Process**:
1. **Demonstrate Functionality**
   - Present the implemented features to the user
   - Explain how the implementation meets the requirements
   - Highlight any deviations from the original plan and reasons

2. **Collect Evaluation Feedback**
   - Document user's assessment of the functionality
   - Note any issues, concerns, or suggested improvements
   - Clarify any misunderstandings about the implementation

3. **Address Issues if Needed**
   - Fix any bugs or issues identified
   - Make adjustments based on user feedback
   - Re-present updated functionality if significant changes were made

**Deliverables**: User-evaluated and approved functionality

### Step 8: Documentation Update

**Objective**: Update documentation to reflect the actual implementation.

**Process**:
1. **Assess Documentation Needs**
   - Compare actual implementation with original plans
   - Identify any discrepancies or changes made during implementation
   - Determine which documents need updates

2. **Ask User Confirmation**
   - Present a summary of proposed documentation changes
   - Ask for user approval before making updates
   - Explain why each update is necessary

3. **Update Documentation if Approved**
   - Update [`plan/README.md`](../plan/README.md) to reflect actual progress
   - Update relevant [`plan-detail/`](../plan-detail/) files with implementation notes
   - Update [`reference/`](../reference/) materials if technical details changed
   - Ensure all cross-references remain accurate

4. **Adjust Functionality if Needed**
   - If user requests changes to functionality instead of documentation updates
   - Implement the requested adjustments
   - Return to Step 7 for user evaluation

**Deliverables**: Updated documentation reflecting actual implementation or adjusted functionality

### Step 9: Repeat Cycle

**Objective**: Continue the iterative process as needed for additional features or improvements.

**Process**:
1. **Evaluate Next Steps**
   - Determine if additional features or improvements are needed
   - Assess if the current implementation meets all requirements
   - Plan for any remaining work

2. **Restart Workflow**
   - Begin again at Step 1 for new features
   - Or start at appropriate step for minor adjustments
   - Maintain consistency with established processes

3. **Repeat Documentation Update Process**
   - After each implementation cycle, always ask if documentation needs updating
   - Follow Step 8 process for documentation updates
   - Continue this cycle until all requirements are met

**Deliverables**: Continuous improvement and feature development

## Workflow Decision Points

### When to Modify Plans
- If user feedback requires significant changes to approach
- If technical constraints prevent following original plan
- If new requirements are introduced during implementation

### When to Update Documentation
- After completing each phase
- When implementation deviates from original plan
- When user requests documentation updates
- Before starting new phases that depend on completed work

### When to Escalate Issues
- If requirements are unclear or conflicting
- If technical constraints cannot be resolved
- If user feedback contradicts original requirements
- If implementation is significantly behind schedule

## Workflow Best Practices

### Communication
- Always seek user approval at key decision points
- Provide clear explanations for any deviations from plans
- Document all decisions and their rationale
- Keep stakeholders informed of progress and challenges

### Documentation
- Keep documentation synchronized with implementation
- Use consistent terminology across all documents
- Maintain accurate cross-references between files
- Update timestamps in front-matter when making changes

### Quality Assurance
- Test implementations thoroughly before user evaluation
- Review documentation for accuracy and completeness
- Verify that all requirements have been addressed
- Ensure that implementation follows established guidelines

## References

- [`ai-guidelines-plan-structure.md`](./ai-guidelines-plan-structure.md): Guidelines for creating plan and plan-detail
- [`ai-content-creation-checklist.md`](./ai-content-creation-checklist.md): Checklist for content creation
- [`../examples/plan-structure-example.md`](../examples/plan-structure-example.md): Examples of proper plan structure
- [`../plan/README.md`](../plan/README.md): Plan template
- [`../plan-detail/README.md`](../plan-detail/README.md): Plan-detail overview
- [`../reference/requirement.md`](../reference/requirement.md): Project requirements

## Workflow Checklist (Mandatory)

### Phase 1: Requirements Analysis
- [ ] **Read requirements first**: Review [`../reference/requirement.md`](../reference/requirement.md) before starting any work
- [ ] **Confirm understanding**: Summarize requirements back to user for confirmation
- [ ] **Document requirements**: Ensure all requirements are properly documented

### Phase 2: High-Level Planning
- [ ] **Create high-level plan only**: Create/update only [`../plan/README.md`](../plan/README.md) with high-level phases and tasks
- [ ] **Do NOT create detailed plans yet**: Do not touch [`../plan-detail/`](../plan-detail/) directory at this stage
- [ ] **Focus on phases only**: Include only phase descriptions and high-level tasks

### Phase 3: User Approval (High-Level)
- [ ] **Present high-level plan**: Show the user the high-level plan from [`../plan/README.md`](../plan/README.md)
- [ ] **Get explicit approval**: User must explicitly approve the high-level plan
- [ ] **Wait for confirmation**: Do not proceed until user confirms approval

### Phase 4: Detailed Planning
- [ ] **Create detailed plans**: Only after high-level approval, create/update files in [`../plan-detail/`](../plan-detail/) directory
- [ ] **Reference high-level plan**: Ensure detailed plans align with approved high-level plan
- [ ] **Cross-reference properly**: Add proper cross-references between plan and plan-detail files

### Phase 5: User Approval (Detailed)
- [ ] **Present detailed plans**: Show the user the detailed plans from [`../plan-detail/`](../plan-detail/) directory
- [ ] **Get explicit approval**: User must explicitly approve the detailed plans
- [ ] **Wait for confirmation**: Do not proceed with implementation until user confirms approval

### Phase 6: Implementation
- [ ] **Follow approved plans**: Implement according to both approved high-level and detailed plans
- [ ] **Track progress**: Mark completed tasks in the plan files
- [ ] **Document deviations**: Note any deviations from the original plan with reasons

## Common Mistakes to Avoid

### ❌ DO NOT:
- Create detailed plans before getting approval on high-level plan
- Skip user review steps between planning phases
- Work on multiple documentation directories simultaneously in wrong order
- Copy structure from doc-template to docs before following proper workflow
- Start implementation before getting approval on both high-level and detailed plans

### ✅ DO:
- Always start with requirements analysis
- Get explicit user approval at each review stage
- Follow the exact sequence: Requirements → High-Level Plan → Approval → Detailed Plan → Approval → Implementation
- Update documentation to reflect actual implementation after each phase