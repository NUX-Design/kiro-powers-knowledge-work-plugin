# Single-Cell RNA-seq Quality Control

Perform quality control on single-cell RNA-seq data using scverse-aligned practices with MAD-based filtering and supporting visualizations.

## Supported Inputs

- `.h5ad`
- `.h5` from 10X-style outputs

Default to the complete QC pipeline unless the user clearly requests custom filtering or a non-standard workflow.

## Recommended Workflow

### Approach 1: Complete QC Pipeline

Use the convenience workflow for:

- standard QC
- exploratory review
- quick reproducible filtering
- batch processing

The workflow should:

1. calculate QC metrics
2. detect MAD-based outliers
3. filter genes and cells
4. produce before and after plots
5. save filtered and annotated outputs

### Approach 2: Modular Workflow

Use a custom or partial workflow when the user needs:

- only metric calculation or visualization
- tissue-specific or subset-specific thresholds
- integration into a larger analysis pipeline
- non-standard filtering logic

## Best Practices

- keep thresholds permissive by default
- inspect plots before accepting filters
- account for tissue- and species-specific mitochondrial patterns
- confirm gene annotation conventions
- iterate parameters when biological context requires it

## Output Expectations

Produce:

- QC summaries
- threshold rationale
- before and after visualizations
- filtered analysis-ready data
- notes on next downstream steps such as ambient RNA correction, doublet detection, normalization, and clustering
