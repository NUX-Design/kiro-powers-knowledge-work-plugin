# scvi-tools Deep Learning Workflows

Guide deep learning-based single-cell and multi-omic analysis using the scvi-tools ecosystem.

## When To Use

Use this workflow for:

- scVI or scANVI integration
- totalVI for CITE-seq
- PeakVI for scATAC-seq
- MultiVI for multiome
- DestVI for spatial deconvolution
- scArches mapping
- veloVI for RNA velocity
- sysVI or related batch-correction problems

## Workflow

1. identify the data modality and target task
2. choose the model that matches the use case
3. prepare raw count-based inputs correctly
4. validate compatibility before training
5. run training, embedding, clustering, and downstream interpretation

## Model Selection

- scRNA-seq unsupervised integration: scVI
- scRNA-seq with labels or transfer: scANVI
- RNA plus protein: totalVI
- ATAC only: PeakVI
- RNA plus ATAC: MultiVI
- spatial plus reference: DestVI
- transcriptional dynamics: veloVI

## Critical Requirements

- retain raw integer counts
- specify batch information when integration is needed
- select appropriate highly variable genes when relevant
- validate `AnnData` structure before training

## Output Expectations

Typical outputs include:

- latent embeddings
- clustered and visualized datasets
- transferred labels
- differential expression or marker tables
- integration-quality observations

## Escalation Paths

When the issue is installation, GPU, versioning, or convergence related, surface environment and troubleshooting needs explicitly rather than pretending the model choice alone solves the problem.
