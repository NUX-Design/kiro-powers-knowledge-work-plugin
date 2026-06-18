---
name: "design"
displayName: "Design"
description: "Accelerate design workflows — critique, design system management, UX writing, accessibility audits, research synthesis, and developer handoff. From exploration to pixel-perfect specs."
keywords: ["design-critique", "design-system", "ux-writing", "accessibility-review", "design-handoff", "user-research", "figma"]
author: "NUX DESIGN"
---

# Design Power

A design productivity power for Kiro. Provides structured workflows for design critique, system management, UX writing, accessibility audits, research synthesis, and developer handoff.

Works standalone with your input (descriptions, screenshots, pasted content). Supercharged when you connect Figma and other MCP tools.

## Onboarding

Start with one of these inputs:

- a Figma URL
- a screenshot or mockup
- pasted research notes or transcripts
- a written description of the screen, flow, or design system

Best results come from adding context up front:

- product type and audience
- stage of work: exploration, refinement, or handoff
- platform: web, mobile, desktop, or multi-platform
- constraints such as brand, accessibility, responsiveness, or engineering limits

## Available Steering Files

This power organizes domain expertise into focused steering files. Load only what you need:

| File | Use When |
|------|----------|
| `design-critique.md` | Reviewing a design for usability, hierarchy, consistency |
| `design-system.md` | Auditing, documenting, or extending a design system |
| `design-handoff.md` | Generating developer handoff specs from designs |
| `ux-copy.md` | Writing or reviewing UX copy, microcopy, error messages |
| `accessibility-review.md` | Running WCAG 2.1 AA accessibility audits |
| `user-research.md` | Planning, conducting, or analyzing user research |
| `research-synthesis.md` | Synthesizing research data into actionable insights |

## When to Use Each Workflow

- **"Review this design"** / **"Critique this mockup"** -> `design-critique.md`
- **"Audit our design system"** / **"Document this component"** -> `design-system.md`
- **"Generate handoff specs"** / **"Spec this for dev"** -> `design-handoff.md`
- **"Write copy for..."** / **"What should this button say?"** -> `ux-copy.md`
- **"Check accessibility"** / **"Is this WCAG compliant?"** -> `accessibility-review.md`
- **"Plan user research"** / **"Create interview guide"** -> `user-research.md`
- **"Synthesize these interviews"** / **"What are the themes?"** -> `research-synthesis.md`

## Standalone vs Supercharged

Every workflow works without integrations:

| Workflow | Standalone | Supercharged With |
|----------|-----------|-------------------|
| Design critique | Describe or share screenshot | Figma MCP (pull designs directly) |
| Design system | Describe your system | Figma MCP (audit component library) |
| Handoff specs | Describe or share screenshot | Figma MCP (exact measurements, tokens) |
| UX copy | Describe the context | Knowledge base MCP (brand voice guidelines) |
| Accessibility | Describe or share screenshot | Figma MCP + analytics for real usage data |
| Research synthesis | Paste transcripts/data | User feedback tools (pull raw data) |

## Available MCP Servers

This power includes one MCP server definition in [mcp.json](/Users/Niwat.yah/Kiro Powers/design/mcp.json):

| Server | Status | Purpose |
|--------|--------|---------|
| `figma` | Disabled by default | Pull designs, inspect components, review tokens, and improve critique and handoff accuracy |

## Optional MCP Integrations

Connect these for a richer experience (configure separately in your workspace or user mcp.json):

| Category | Examples | What It Enables |
|----------|----------|-----------------|
| Design tool | Figma | Pull designs, inspect components, access design tokens |
| User feedback | Intercom, Productboard | Raw feedback, feature requests, NPS data |
| Project tracker | Linear, Asana, Jira | Link designs to tickets, track implementation |
| Knowledge base | Notion | Brand guidelines, design principles, research repository |
| Product analytics | Amplitude, Mixpanel | Usage data for research synthesis and design decisions |

## Configuration

The bundled `mcp.json` is intentionally minimal and disabled by default.

To use Figma with this power:

1. enable the `figma` server from this power's `mcp.json`, or copy it into your workspace/user MCP config
2. authenticate the Figma MCP server in Kiro if prompted
3. provide a Figma file or node URL when asking for critique, handoff, or design-system work

If you do not enable MCP, the power still works from screenshots, pasted copy, and written design context.

## Best Practices

1. **Be specific about context** — "Checkout flow for a B2B SaaS targeting enterprise PMs" beats "a form"
2. **Specify the stage** — Early exploration gets different feedback than final polish
3. **Share the design system** — Mention your existing tokens, typography, and patterns
4. **Include user context** — Who is using this? What's their goal? How are they feeling?
5. **Use connectors** — Figma MCP dramatically improves critique, handoff, and system management

## Troubleshooting

### Figma context is missing

- make sure the Figma MCP server is enabled and authenticated
- provide a direct Figma URL instead of only a file name
- fall back to screenshots or pasted specs if MCP access is unavailable

### Feedback is too generic

- include the product type, user goal, and stage of work
- specify whether you want critique, copy, accessibility review, handoff, or synthesis
- mention constraints such as brand voice, design system, or platform limitations
