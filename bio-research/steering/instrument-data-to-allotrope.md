# Instrument Data To Allotrope

Convert laboratory instrument output into Allotrope Simple Model representations or flattened CSV suitable for LIMS, ELN, or data engineering handoff.

## Use Cases

- standardize PDF, CSV, Excel, or TXT instrument exports
- prepare data for LIMS or data lake ingestion
- generate flattened tabular output for analysis or imports
- export parser logic for engineering handoff

## Workflow

1. detect or confirm instrument type
2. prefer native Allotrope parsing support when available
3. fall back to flexible parsing only when native support is unavailable
4. generate one or more outputs:
   - ASM JSON
   - flattened CSV
   - parser code handoff
5. validate output before delivery

## Core Rules

- separate raw measurements from calculated values
- preserve traceability for calculated data
- ask the user when field classification is ambiguous
- validate semantics and identifiers before finalizing

## Output Options

- ASM JSON for semantic structure and archival compatibility
- flattened CSV for human-friendly or import-friendly workflows
- parser code for data engineering teams

## Common Mistakes To Avoid

- guessing field classes without clarification
- treating calculated data as raw measurements
- skipping validation
- collapsing too many measurements into one undifferentiated record
