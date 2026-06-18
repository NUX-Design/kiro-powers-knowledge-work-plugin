---
name: "legal"
displayName: "Legal"
description: "Legal operations workflows for contract review, NDA triage, compliance checks, briefings, response templates, vendor agreement visibility, risk assessment, signature routing, and meeting prep."
keywords: ["legal", "contracts", "nda", "compliance", "privacy", "risk", "briefing", "vendor-management", "esignature"]
author: "Anthropic"
---

# Legal Power

A legal productivity power for Kiro focused on in-house legal workflows. It helps with contract review, NDA triage, compliance checks, legal briefings, templated responses, vendor agreement status checks, legal risk assessments, signature routing, and meeting preparation.

This power works standalone with pasted text, uploaded documents, screenshots, and user-provided context. It becomes stronger when you connect chat, document, project, e-signature, and office-suite MCP tools.

## Available Steering Files

| File | Use When |
|------|----------|
| `brief.md` | Building daily, topic, or incident briefings for legal work |
| `compliance-check.md` | Checking a product, process, or initiative for regulatory and policy exposure |
| `legal-response.md` | Drafting templated responses to common legal inquiries with escalation checks |
| `legal-risk-assessment.md` | Scoring, documenting, and escalating legal risk consistently |
| `meeting-briefing.md` | Preparing meeting briefs and tracking follow-up actions |
| `review-contract.md` | Reviewing a contract against a playbook or fallback market standards |
| `signature-request.md` | Running a pre-signature checklist and preparing routing for execution |
| `triage-nda.md` | Screening NDAs into approve, review, or escalate buckets |
| `vendor-check.md` | Building a consolidated agreement-status report for a vendor |

## When to Use Each Workflow

- Use `review-contract.md` when you need clause-by-clause review, redlines, negotiation priorities, or business-impact framing.
- Use `triage-nda.md` when an NDA needs a quick GREEN / YELLOW / RED routing decision.
- Use `compliance-check.md` when product, marketing, privacy, or operations teams propose something with regulatory implications.
- Use `brief.md` for morning briefs, internal topic research, or fast incident context gathering.
- Use `legal-response.md` when replying to recurring inquiry types such as DSRs, NDA requests, litigation holds, vendor questions, subpoenas, or insurance notices.
- Use `vendor-check.md` when you need to know what agreements exist with a vendor, what is missing, and what is expiring.
- Use `legal-risk-assessment.md` when classifying risk severity, likelihood, and escalation paths for a matter.
- Use `meeting-briefing.md` when preparing for negotiations, board updates, vendor calls, compliance reviews, or other legal-relevant meetings.
- Use `signature-request.md` when a document is finalized and needs execution setup or a pre-send validation pass.

## Standalone vs Supercharged

Every workflow can run without integrations:

| Workflow | Standalone | Supercharged With |
|----------|-----------|-------------------|
| Contract review | Upload or paste the contract and share context | Document storage, CLM, knowledge-base tools |
| NDA triage | Upload or paste the NDA | Document storage and approval systems |
| Compliance check | Describe the initiative and jurisdictions | Policy docs, trackers, and collaboration tools |
| Briefings | Provide the topic or incident manually | Email, calendar, chat, CLM, CRM |
| Response templates | Provide the inquiry details | Email, calendar, document libraries |
| Vendor check | Provide the vendor name and any documents you have | CLM, CRM, email, chat, document storage |
| Risk assessment | Describe the matter and exposure | Matter history, trackers, knowledge bases |
| Signature routing | Provide the final document and signer list | E-signature and CLM tools |
| Meeting prep | Share the meeting details manually | Calendar, email, chat, docs, CRM, CLM |

## Optional MCP Integrations

This power is still useful without MCP, but these integrations add practical value:

| Category | Examples | What It Enables |
|----------|----------|-----------------|
| Chat | Slack | Intake, context gathering, team escalations |
| Cloud storage | Box, Egnyte | Playbooks, templates, agreements, precedent files |
| Project tracker | Atlassian | Matter tracking, approvals, linked work items |
| E-signature | DocuSign | Execution routing and status tracking |
| Office suite | Google Workspace, Microsoft 365 | Email, calendar, docs, and meeting context |

See [mcp.json](/Users/Niwat.yah/Kiro Powers/legal/mcp.json) for optional server definitions. All included servers are disabled by default so users opt in explicitly.

## Best Practices

1. Customize the workflow to your jurisdiction, contract playbook, and risk tolerance before relying on results.
2. State your role and business context clearly. Vendor-side and customer-side analysis are materially different.
3. Treat generated outputs as draft working products, not legal advice or final legal conclusions.
4. Prefer structured inputs: contract type, deadline, focus areas, jurisdictions, and decision deadlines improve output quality.
5. Be explicit about missing sources. If email, CLM, or document systems are unavailable, note the gap instead of overstating confidence.
6. Review escalations promptly. Matters involving regulators, litigation, board exposure, criminal risk, or novel jurisdictions should not be handled as routine templates.
