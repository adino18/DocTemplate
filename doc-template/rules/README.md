---
title: "Development Rules"
description: "Essential development guidelines, regulations, and workflows for AI agents to follow during project tasks."
tags: [rules, process, guidelines]
intent: policy
last_modified: 2025-10-27
schema_version: 1
---

**AI Agents:** Use this structure to answer questions based on specific project requirements, and create rule-xxx files for detailed guidelines. Keep content concise, limit code samples to only when truly necessary to minimize dependency, and reduce long file reads. Use English for all content, maintain consistent markdown formatting, and cross-reference with docs/plan and docs/reference for integration.

## Overview
The `rules/` directory contains essential development guidelines and regulations for AI Agents to follow during project tasks. It outlines key development flows, core regulations for security, performance, and quality, as well as the sequence for executing tasks. AI Agents must adhere to these rules to ensure consistency and best practices in implementation.

**Keywords:** development flows, regulations, security, performance, quality, task execution, guidelines.

## Key Development Flows
- What are the main backend development steps?
- What are the frontend development processes?
- How should API development be structured?
- What is the database change workflow?

## Core Regulations
- What security measures are required?
- What performance standards must be met?
- What quality assurance rules apply?

## Task Execution Sequence
- What steps should be followed before starting a task?
- How to integrate with reference and plan documents?
- What is the order for implementation, testing, and deployment?

## References
- [`README.md`](./README.md): Main overview of development rules (this file).
- [`docs/README.md`](../README.md): Main documentation overview.
- [`plan/README.md`](../plan/README.md): Project plans and phases.
- [`reference/README.md`](../reference/README.md): Reference materials.
- For specific requirements (e.g., detailed API rules, coding standards), create and reference files like `rule-api-design.md`, `rule-coding-standards.md`, etc., in this directory. AI Agents should check for these files when needed.

## Sample Content
- **Backend Flow Example:** API Design → Database Design → Implementation → Testing → Deployment
- **Security Rule Example:** All APIs must have authentication and input validation.
- **Sequence Example:** 1. Read rules, 2. Check reference, 3. Refer to plan, 4. Implement, 5. Test, 6. Deploy.

---

*Note: AI Agents must read these regulations before performing any task. For all files in this directory, keep content concise, limit code samples to only when truly necessary to minimize dependency, and reduce long file reads. Review and update files periodically to maintain relevance.*