# Design System

Audit, document, or extend your design system — components, tokens, patterns.

## Modes

```
audit                       # Full system audit
document [component]        # Document a component
extend [pattern]            # Design a new component or pattern
```

## Components of a Design System

### Design Tokens
- Colors (brand, semantic, neutral)
- Typography (scale, weights, line heights)
- Spacing (scale, component padding)
- Borders (radius, width)
- Shadows (elevation levels)
- Motion (durations, easings)

### Components
Reusable UI elements with:
- Variants (primary, secondary, ghost)
- States (default, hover, active, disabled, loading, error)
- Sizes (sm, md, lg)
- Behavior (interactions, animations)
- Accessibility (ARIA, keyboard)

### Patterns
Common UI solutions combining components:
- Forms (input groups, validation, submission)
- Navigation (sidebar, tabs, breadcrumbs)
- Data display (tables, cards, lists)
- Feedback (toasts, modals, inline messages)

## Principles

1. **Consistency over creativity** — The system exists so teams don't reinvent the wheel
2. **Flexibility within constraints** — Components should be composable, not rigid
3. **Document everything** — If it's not documented, it doesn't exist
4. **Version and migrate** — Breaking changes need migration paths

## Output: Audit

```markdown
## Design System Audit

### Summary
**Components reviewed:** [X] | **Issues found:** [X] | **Score:** [X/100]

### Naming Consistency
| Issue | Components | Recommendation |
|-------|------------|----------------|
| [Inconsistency] | [List] | [Standard to adopt] |

### Token Coverage
| Category | Defined | Hardcoded Values Found |
|----------|---------|----------------------|
| Colors | [X] | [X] instances |
| Spacing | [X] | [X] instances |
| Typography | [X] | [X] instances |

### Component Completeness
| Component | States | Variants | Docs | Score |
|-----------|--------|----------|------|-------|
| Button | OK | OK | Partial | 8/10 |

### Priority Actions
1. [Most impactful improvement]
2. [Second priority]
3. [Third priority]
```

## Output: Document

```markdown
## Component: [Name]

### Description
[What this component is and when to use it]

### Variants
| Variant | Use When |
|---------|----------|
| Primary | Main actions |
| Secondary | Supporting actions |

### Props / Properties
| Property | Type | Default | Description |
|----------|------|---------|-------------|
| [prop] | [type] | [default] | [description] |

### States
| State | Visual | Behavior |
|-------|--------|----------|
| Default | [description] | — |
| Hover | [description] | [interaction] |
| Disabled | [description] | Non-interactive |

### Accessibility
- **Role**: [ARIA role]
- **Keyboard**: [Tab, Enter, Escape behavior]
- **Screen reader**: [Announced as...]

### Do's and Don'ts
| Do | Don't |
|----|-------|
| [Best practice] | [Anti-pattern] |
```

## Output: Extend

```markdown
## New Component: [Name]

### Problem
[What user need or gap this addresses]

### Related Components
| Component | Similarity | Why Not Enough |
|-----------|-----------|----------------|
| [Existing] | [Shared] | [Gap] |

### Proposed API
| Property | Type | Default | Description |
|----------|------|---------|-------------|
| [prop] | [type] | [default] | [description] |

### Tokens Used
- Colors: [tokens]
- Spacing: [tokens]
- Typography: [tokens]

### Accessibility
- **Role**: [ARIA role]
- **Keyboard**: [Expected interactions]
```

## With Figma MCP

If Figma is connected:
- Audit components directly — check naming, variants, and token usage
- Pull component properties and layer structure for documentation

## Tips

1. **Start with an audit** — Know where you are before deciding where to go
2. **Document as you build** — Easier to document while designing than after
3. **Prioritize coverage** — 80% documented beats 100% of 10 components
