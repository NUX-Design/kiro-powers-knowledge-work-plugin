---
name: "bio-research"
displayName: "Bio Research"
description: "Life sciences research workflows for literature review, single-cell analysis, nf-core pipelines, Allotrope conversion, and scientific project strategy."
keywords: ["biology", "research", "single-cell", "scRNA-seq", "nextflow", "nf-core", "allotrope", "life-sciences", "pubmed", "genomics"]
author: "NUX DESIGN"
---

# Bio-Research

Guided MCP power for early-stage life sciences and preclinical research. It combines external research and data sources with practical analysis workflows for literature discovery, single-cell analysis, sequencing pipelines, instrument data standardization, and scientific problem selection.

This power is most effective when the relevant MCP tools are connected, but several analysis workflows also remain useful when the user already has local data, project context, or research ideas ready to work from.

## Steering Index

- `steering/start-and-orientation.md`: Check available research tools, survey workflows, and choose a starting path.
- `steering/single-cell-rna-qc.md`: Run scRNA-seq quality control with scverse-oriented defaults and MAD-based filtering.
- `steering/scvi-tools.md`: Apply deep learning workflows for single-cell and multi-omic integration, mapping, and modeling.
- `steering/nextflow-pipelines.md`: Run nf-core RNA-seq, variant calling, and ATAC-seq pipelines on local or GEO/SRA data.
- `steering/instrument-data-to-allotrope.md`: Convert instrument output into Allotrope ASM or flattened CSV for lab data standardization.
- `steering/scientific-problem-selection.md`: Structure research ideation, project evaluation, troubleshooting, and strategic problem choice.

## When To Use Which Workflow

- Use `start-and-orientation.md` when first assessing available research connectors and deciding which workflow fits the task.
- Use `single-cell-rna-qc.md` when filtering low-quality cells, reviewing QC metrics, or preparing single-cell data for downstream analysis.
- Use `scvi-tools.md` when the work involves scVI, scANVI, totalVI, PeakVI, MultiVI, DestVI, veloVI, sysVI, or related deep learning methods.
- Use `nextflow-pipelines.md` when running nf-core pipelines on local FASTQs or public sequencing datasets from GEO/SRA.
- Use `instrument-data-to-allotrope.md` when standardizing instrument exports for LIMS, ELN, or data engineering handoff.
- Use `scientific-problem-selection.md` when exploring new research directions, diagnosing stuck projects, or making strategic scientific decisions.

## Standalone Versus Supercharged

This power can work standalone for several workflows:

- single-cell QC and scvi-tools guidance when the user already has local `.h5ad`, `.h5`, or related analysis inputs
- Nextflow planning and validation when the user already has local sequencing data
- research strategy and scientific problem selection based on project context alone
- Allotrope conversion guidance when instrument files are already available locally

With MCP connected, it becomes much stronger for discovery and evidence gathering:

- `~~literature`: biomedical literature, preprints, and AI-assisted research synthesis
- `~~journal access`: full-text or publication access workflows
- `~~clinical trials`: clinical study discovery
- `~~chemical database`: compound and bioactivity discovery
- `~~drug targets`: target prioritization and discovery
- `~~data repository`: collaborative research data access
- `~~scientific illustration`: figure and diagram creation
- `~~AI research`: specialized AI biology tooling

Optional binary MCP additions mentioned in the source plugin, such as 10X Genomics and ToolUniverse, are conceptually relevant but are not included in `mcp.json` here because they require separate binary installation flows.

## Scripts And References

The source plugin includes substantial scripts and reference material for several workflows, especially:

- scRNA-seq QC helpers and plotting utilities
- scvi-tools pipeline scripts
- nf-core environment, acquisition, and samplesheet helpers
- Allotrope conversion, validation, flattening, and parser export scripts
- scientific problem selection reference modules

This power preserves those workflows conceptually in steering form but does not copy the executable plugin scripts.

## Best Practices

- Confirm data modality, organism, and downstream goal before choosing an analysis path.
- Distinguish between workflow planning and validated scientific conclusions; review outputs with domain experts where needed.
- For computational workflows, validate environment and inputs before launching large analyses.
- For data standardization, ask when field mappings or semantic classifications are ambiguous instead of guessing.
- Use literature and structured databases to pressure-test research ideas, not just to support preferred hypotheses.
