# SlotHash core experimental results

Zekai Ye and Linxin Xu

This repository contains numerical results supporting *SlotHash: Foreground-Aware Slot Hashing for Fine-Grained Sketch-Based Image Retrieval*. It covers the primary ShoeV2 comparison (Table 1) and the source data for Figures 2 and 3.

| File | Contents |
| --- | --- |
| [table1_shoev2_seed_metrics.csv](table1_shoev2_seed_metrics.csv) | Seven 64-bit methods evaluated over three matched training seeds (2026–2028). The official test set has 666 sketch queries and 200 gallery identities. |
| [table1_shoev2_paired.csv](table1_shoev2_paired.csv) | Six paired contrasts, computed as SlotHash minus the matched comparator, with 95% identity-cluster bootstrap confidence intervals. |
| [figure2_code_length.csv](figure2_code_length.csv) | Test mAP for ShoeV2 and ChairV2 at 16, 32, 64 and 128 bits. End-to-end methods use one training seed. ShoeV2 ITQ entries report the mean and sample standard deviation across three frozen training-seed encoders, after averaging three quantizer fits per encoder. ChairV2 ITQ entries summarize three quantizer fits on one frozen encoder. |
| [figure3_aggregation.csv](figure3_aggregation.csv) | One-seed test mAP for global pooling and the shared-slot configuration with slot-consistency supervision. |
| [figure3_distillation.csv](figure3_distillation.csv) | Routed distillation minus teacher initialization at 16 bits (one seed) and 64 bits (three matched seeds). |
| [provenance.json](provenance.json) | SHA-256 checksums of the published tables and of the archived statistics and figure-source records used to derive them. |

mAP, recall, differences and confidence limits are expressed as proportions. Multiply a difference by 100 to report percentage points. A stored bootstrap tail area of zero is reported in the paper as p < 0.001. Seed-level metric names with the val_ prefix refer to validation.

The benchmark datasets are provided by their original distributors. See the [QMUL ShoeV2 project](http://www.eecs.qmul.ac.uk/~qian/Project_cvpr16.html) and the [ChairV2 release](https://github.com/AyanKumarBhunia/on-the-fly-FGSBIR/blob/master/ChairV2.zip). The manuscript's supplementary methods document the protocol and splits.
