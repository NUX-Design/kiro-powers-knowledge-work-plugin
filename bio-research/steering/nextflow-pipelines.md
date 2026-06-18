# nf-core Nextflow Pipelines

Run nf-core pipelines for RNA-seq, WGS/WES, or ATAC-seq on local or public sequencing data.

## Typical Use Cases

- RNA-seq gene expression analysis
- germline or somatic variant calling
- ATAC-seq accessibility analysis
- GEO or SRA reanalysis

## Workflow Checklist

1. acquire data if starting from GEO or SRA
2. run environment checks and stop if critical requirements fail
3. select the pipeline with the user
4. run the test profile first
5. create or validate the samplesheet
6. confirm genome and pipeline-specific settings
7. run the real pipeline
8. verify outputs and completion

## Pipeline Selection

- `rnaseq` for gene expression
- `sarek` for WGS or WES variant analysis
- `atacseq` for chromatin accessibility

## Mandatory Safeguards

- do not skip environment validation
- do not skip the test profile
- confirm reference genome before launch
- confirm pipeline-specific options at decision points

## Output Expectations

Deliver:

- selected pipeline and rationale
- samplesheet guidance
- run configuration
- success checks
- key output locations by pipeline type

## Troubleshooting Guidance

If environment, Docker, Java, or Nextflow prerequisites fail, stop and route the user through remediation before advancing.
