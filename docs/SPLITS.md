# Dataset statistics and split documentation

[← Dataset overview](../README.md)

## Manuscript reference distribution

FSBench-40K denotes **Foggy Smoke Benchmark-40K**. The current manuscript reports the following **40,579-image** distribution, with a target split of **80% training, 10% validation and 10% test**. Integer class counts produce small deviations from the target percentages.

| Split | Normal | Fog | Smoke | SmokeFog | Total |
| :--- | ---: | ---: | ---: | ---: | ---: |
| Train | 8,290 | 7,304 | 8,815 | 8,053 | 32,462 |
| Validation | 1,036 | 913 | 1,101 | 1,006 | 4,056 |
| Test | 1,037 | 913 | 1,103 | 1,008 | 4,061 |
| **Total** | **10,363** | **9,130** | **11,019** | **10,067** | **40,579** |

This is the distribution reported in the current manuscript. The fixed image inventory, actual counts and split membership of a supplied dataset version are recorded in its release materials.

## Evaluation protocol

1. Learn model parameters on the training subset.
2. Select configurations and checkpoints using the validation subset.
3. Fix the model and evaluation settings before computing the final test metrics.
4. Use the same released split for methods being compared and report the release identifier.

Additional data, custom partitions or relabelling are described separately when reporting results.

## Source groups and related images

Release records document the applicable partition protocol and the source groups established during dataset preparation. For a **source-independent partition**, images linked to the same source photo, scene or video are treated as one group and assigned to one subset. Rotations, mirror images, resized copies and crops of the same photo are handled within the same source family; different frames retain their distinct image identities.

Available source identifiers and the basis of each established relationship are recorded with the release. Source-independent results are associated with the corresponding grouped manifests. A shared filename pattern or a visually similar appearance alone does not establish a source group.

## Image-folder convention

```text
FSBench-40K/
├── train/
│   ├── Normal/
│   ├── Fog/
│   ├── Smoke/
│   └── SmokeFog/
├── val/
│   ├── Normal/
│   ├── Fog/
│   ├── Smoke/
│   └── SmokeFog/
└── test/
    ├── Normal/
    ├── Fog/
    ├── Smoke/
    └── SmokeFog/
```

The folder names denote semantic categories. Use the supplied class mapping for numerical label IDs; the order of categories in this page is not a label-index specification.

## Inventory and manifest fields

The following describes the information to accompany an approved release. The repository does not substitute example image IDs for the final inventory.

| Field | Meaning |
| :--- | :--- |
| `release_id` | Fixed data version associated with the inventory |
| `image_id` | Stable identifier for an image in that version |
| `relative_path` | Image path within the supplied package |
| `class_name` | Normal, Fog, Smoke or SmokeFog |
| `split` | train, val or test |
| `sha256` | File checksum for integrity verification |
| `source_group_id` | Established source family or scene/video group, where available |
| `source_reference` | Source attribution or source-record reference, where available |

## Version records

The final split manifests and inventory are fixed together with the image release. Changes to images, labels or split membership are recorded under a new version. See [release documentation](RELEASES.md) and [data access](ACCESS.md).
