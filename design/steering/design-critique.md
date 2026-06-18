# Design Critique

Get structured design feedback across multiple dimensions.

## Input

Provide one of:
- Figma URL (if Figma MCP connected, pull the design directly)
- Screenshot or image
- Detailed description of the design

Include context: What is this? Who is it for? What stage (exploration, refinement, final)?

## Critique Framework

### 1. First Impression (2 seconds)
- What draws the eye first? Is that correct?
- What's the emotional reaction?
- Is the purpose immediately clear?

### 2. Usability
- Can the user accomplish their goal?
- Is the navigation intuitive?
- Are interactive elements obvious?
- Are there unnecessary steps?

### 3. Visual Hierarchy
- Is there a clear reading order?
- Are the right elements emphasized?
- Is whitespace used effectively?
- Is typography creating the right hierarchy?

### 4. Consistency
- Does it follow the design system?
- Are spacing, colors, and typography consistent?
- Do similar elements behave similarly?

### 5. Accessibility
- Color contrast ratios
- Touch target sizes
- Text readability
- Alternative text for images

## Feedback Principles

- **Be specific**: "The CTA competes with the navigation" not "the layout is confusing"
- **Explain why**: Connect feedback to design principles or user needs
- **Suggest alternatives**: Don't just identify problems, propose solutions
- **Acknowledge what works**: Good feedback includes positive observations
- **Match the stage**: Early exploration gets different feedback than final polish

## Output Format

```markdown
## Design Critique: [Design Name]

### Overall Impression
[1-2 sentence first reaction]

### Usability
| Finding | Severity | Recommendation |
|---------|----------|----------------|
| [Issue] | Critical / Moderate / Minor | [Fix] |

### Visual Hierarchy
- **What draws the eye first**: [Element] — [Is this correct?]
- **Reading flow**: [How does the eye move?]
- **Emphasis**: [Are the right things emphasized?]

### Consistency
| Element | Issue | Recommendation |
|---------|-------|----------------|
| [Item] | [Inconsistency] | [Fix] |

### Accessibility
- **Color contrast**: [Pass/fail for key text]
- **Touch targets**: [Adequate size?]
- **Text readability**: [Font size, line height]

### What Works Well
- [Positive observation 1]
- [Positive observation 2]

### Priority Recommendations
1. **[Most impactful change]** — [Why and how]
2. **[Second priority]** — [Why and how]
3. **[Third priority]** — [Why and how]
```

## With Figma MCP

If Figma is connected:
- Pull the design directly and inspect components, tokens, and layers
- Compare against the existing design system for consistency

## Tips

1. **Share the context** — "This is a checkout flow for a B2B SaaS" helps give relevant feedback
2. **Specify your stage** — Early exploration gets different feedback than final polish
3. **Ask to focus** — "Just look at the navigation" gives more depth on one area
