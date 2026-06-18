# Research Synthesis

Synthesize user research data into actionable insights.

## Input

Accepts:
- Interview transcripts or notes
- Survey results (CSV, pasted data)
- Usability test recordings or notes
- Support tickets or feedback
- NPS/CSAT responses
- App store reviews

## Output Format

```markdown
## Research Synthesis: [Study Name]
**Method:** [Interviews / Survey / Usability Test] | **Participants:** [X]
**Date:** [Date range]

### Executive Summary
[3-4 sentence overview of key findings]

### Key Themes

#### Theme 1: [Name]
**Prevalence:** [X of Y participants]
**Summary:** [What this theme is about]
**Supporting Evidence:**
- "[Quote]" — P[X]
- "[Quote]" — P[X]
**Implication:** [What this means for the product]

### Insights -> Opportunities

| Insight | Opportunity | Impact | Effort |
|---------|-------------|--------|--------|
| [What we learned] | [What we could do] | High/Med/Low | High/Med/Low |

### User Segments Identified
| Segment | Characteristics | Needs | Size |
|---------|----------------|-------|------|
| [Name] | [Description] | [Key needs] | [Rough %] |

### Recommendations
1. **[High priority]** — [Why, based on which findings]
2. **[Medium priority]** — [Why]
3. **[Lower priority]** — [Why]

### Questions for Further Research
- [What we still don't know]
```

## With User Feedback MCP

If user feedback tools (Intercom, Productboard) are connected:
- Pull support tickets, feature requests, and NPS responses to supplement data
- Cross-reference themes with real user complaints

## With Product Analytics MCP

If analytics (Amplitude, Mixpanel) are connected:
- Validate qualitative findings with usage data
- Quantify the impact of identified pain points

## Tips

1. **Include raw quotes** — Direct participant quotes make insights credible
2. **Separate observations from interpretations** — "5 of 8 clicked wrong button" is observation; "placement is confusing" is interpretation
3. **Quantify where possible** — "7 of 10 users" is specific; "most users" is vague
