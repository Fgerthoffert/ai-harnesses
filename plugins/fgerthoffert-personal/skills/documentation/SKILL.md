---
name: documentation
description: Generates documentation following Francois Gerthoffert's preferred structure and style when working in an Agentic context.
---

# Placeholder: Documentation Generation Skill

> **Note:** This skill is a placeholder. More detailed documentation generation guidelines will be added in a future update.

When generating documentation for Francois Gerthoffert via an Agentic workflow, follow these principles:

## Purpose

This skill guides Copilot agents to produce documentation that is consistent with Francois Gerthoffert's preferred style and structure. It should be combined with the `writing-style` skill to ensure tone and language consistency.

## Documentation Types

- **README files:** Provide a brief project description, prerequisites, installation steps, usage examples, and a contribution/license section.
- **API documentation:** Document each endpoint or function with a description, parameters, return values, and usage example.
- **Architecture Decision Records (ADRs):** Use the standard ADR format: title, status, context, decision, and consequences.
- **How-to guides:** Lead with the goal, list prerequisites, provide numbered steps, and finish with a verification step.
- **Release notes / changelogs:** Follow Keep a Changelog format (Added, Changed, Deprecated, Removed, Fixed, Security).

## Structure Guidelines

1. Start every document with a clear title and a one-paragraph summary of what the document covers.
2. Use Markdown formatting throughout.
3. Include code blocks with appropriate language tags for all code samples.
4. Add a "Further reading" or "See also" section when relevant external resources exist.

## Agentic Workflow Notes

- When invoked from an Agent, infer the documentation type from the context (e.g., new project → README, new API endpoint → API docs).
- Ask clarifying questions before generating if the context is ambiguous.
- After generating, offer to refine specific sections or adjust the tone.

## Additional Notes

<!-- TODO: Add concrete documentation templates and examples tailored to Francois Gerthoffert's projects and domains. -->
