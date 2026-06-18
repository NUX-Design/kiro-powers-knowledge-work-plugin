# Design Handoff

Generate comprehensive developer handoff documentation from a design.

## Input

Provide one of:
- Figma URL (best — pulls exact measurements and tokens)
- Screenshot or image
- Detailed description of the design

Mention edge cases, tech stack, and responsive requirements.

## What to Include

### Visual Specifications
- Exact measurements (padding, margins, widths)
- Design token references (colors, typography, spacing)
- Responsive breakpoints and behavior
- Component variants and states

### Interaction Specifications
- Click/tap behavior
- Hover states
- Transitions and animations (duration, easing)
- Gesture support (swipe, pinch, long-press)

### Content Specifications
- Character limits
- Truncation behavior
- Empty states
- Loading states
- Error states

### Edge Cases
- Minimum/maximum content
- International text (longer strings)
- Slow connections
- Missing data

### Accessibility
- Focus order
- ARIA labels and roles
- Keyboard interactions
- Screen reader announcements

## Principles

1. **Don't assume** — If it's not specified, the developer will guess
2. **Use tokens, not values** — Reference `spacing-md` not `16px`
3. **Show all states** — Default, hover, active, disabled, loading, error, empty
4. **Describe the why** — Helps developers make good judgment calls

## Output Format

```markdown
## Handoff Spec: [Feature/Screen Name]

### Overview
[What this does, user context]

### Design Tokens Used
| Token | Value | Usage |
|-------|-------|-------|
| `color-primary` | #hex | CTA buttons, links |
| `spacing-md` | Xpx | Between sections |

### Components
| Component | Variant | Props | Notes |
|-----------|---------|-------|-------|
| [Name] | [Variant] | [Props] | [Behavior] |

### States and Interactions
| Element | State | Behavior |
|---------|-------|----------|
| CTA Button | Hover | Background darken 10% |
| CTA Button | Loading | Spinner, disabled |
| Form | Error | Red border, message below |

### Responsive Behavior
| Breakpoint | Changes |
|------------|---------|
| Desktop (>1024px) | Default layout |
| Tablet (768-1024px) | [Changes] |
| Mobile (<768px) | [Changes] |

### Edge Cases
- **Empty state**: [What to show]
- **Long text**: [Truncation rules]
- **Loading**: [Skeleton or spinner]
- **Error**: [Error state]

### Animation / Motion
| Element | Trigger | Animation | Duration | Easing |
|---------|---------|-----------|----------|--------|
| [Element] | [Trigger] | [Desc] | [ms] | [easing] |

### Accessibility Notes
- Focus order
- ARIA labels needed
- Keyboard interactions
```

## With Figma MCP

If Figma is connected:
- Pull exact measurements, tokens, and component specs
- Export assets and generate a complete spec sheet

## Tips

1. **Share the Figma link** — Exact measurements, tokens, and component info
2. **Mention edge cases** — "What happens with 100 items?" helps spec boundaries
3. **Specify tech stack** — "React + Tailwind" gives relevant implementation notes
