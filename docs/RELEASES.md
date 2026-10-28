# Dataset releases and reproducibility

The complete dataset is delivered through the corresponding author. A repository revision identifies a change to project documentation; it does not by itself identify a release of the image dataset.

## Release identification

Each supplied archive is accompanied by a release identifier, release date, class mapping, image inventory, split manifests, checksum list and release notes. The delivery record states whether it corresponds to the experiments reported in the paper.

## Benchmark comparisons

Use the release and train / validation / test manifests supplied for the relevant experiment. Report the release identifier in publications. If a custom partition, additional dataset, changed label or revised image is used, describe that change separately.

## Suggested delivery record

| Item | What is recorded |
| :--- | :--- |
| Release | Identifier and date of the supplied data snapshot |
| Scope | Class definitions and included images |
| Splits | Training, validation and test image IDs |
| Provenance | Available source and grouping information, with documented limits |
| Integrity | Archive or file SHA-256 checksums |
| Change log | Additions, removals or corrections relative to the preceding release |
| Rights | Applicable permissions, attribution and third-party conditions |

Actual values are provided with the approved delivery. No image release is created by this documentation alone.

The [split documentation](SPLITS.md) provides the manuscript reference distribution, folder convention and manifest fields.
