# HPRM-Former

[← Dataset overview](../README.md) · [Dataset statistics and splits](../README.md#dataset-statistics-and-splits)

## Associated paper

**A Heterogeneity-Aware Prototype Routing Transformer with Consensus-Disagreement Memory for Smoke Detection under Foggy Conditions**

Yao Wei, Haicheng Qu, Tong Gao, Hao Chen, and Cuiping Shi

HPRM-Former is an image-classification framework for smoke detection under foggy conditions. It models regional variation, prototype-routing ambiguity and complementary information across feature stages.

## Model components

| Component | Full name | Function |
| :--- | :--- | :--- |
| **RHASR** | Region Heterogeneity-Aware Scale Routing | Uses regional statistics and image-level priors to select spatially varying scale weights. |
| **ACPRM** | Ambiguity-Calibrated Prototype Routing Mixer | Constructs input-dependent prototypes and uses retrieval entropy and confidence to regulate local–prototype fusion. |
| **CDMF** | Consensus-Disagreement Memory Fusion | Combines cross-stage consensus, disagreement and compact memory constructed from the current image. |

The memory is rebuilt for each input image; it is not a persistent video memory.

## Relationship to FSBench-40K

FSBench-40K provides the four-category classification benchmark used in the associated research. The dataset can also support the evaluation of other classification methods under the same release and evaluation protocol.

For citation, see the [repository citation](../README.md#citation). For the dataset and application materials, return to the [dataset overview](../README.md).
