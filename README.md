# Unveiling Hidden Defects: Camouflaged Object Detection for Industrial Defect Localization
Industrial anomaly detection faces a fundamental challenge: surface defects often share nearly identical spectral, textural, and geometric properties with their surrounding material, creating a form of visual camouflage that confounds conventional inspection systems. We reframe industrial defect localization as a camouflaged object detection (COD) problem and conduct a comprehensive evaluation on CDS2K, the largest benchmark for camouflaged defect segmentation, comparing eight anomaly detection (AD) approaches against twelve COD-based architectures. The best COD model (ARNet-v2) outperforms the best AD model (RADIO) by over 24\% in pixel-level F1 and AP metrics overall, while remaining competitive at image-level classification and using architectures orders of magnitude smaller than VFM-based detectors. These findings indicate that, under the zero-shot/supervised comparison regime evaluated here, COD-based architectures are a more effective and efficient paradigm than the VFM-based AD detectors considered for pixel-level, low-contrast industrial defect segmentation on CDS2K; we discuss the supervision asymmetry between the two families of methods and its implications for the fairness of this comparison. 

### Training Parameters

| Category | Technique | Repository | Optimizer | LR | BS | Epochs | Scheduler |
|---|---|---|---|---:|---:|---:|---|
| AD-based | DRAEM | [GitHub](https://github.com/VitjanZ/DRAEM) | — | — | — | — | — |
| AD-based | MMR | [GitHub](https://github.com/zhangzilongc/MMR) | — | — | — | — | — |
| AD-based | MemSeg | [GitHub](https://github.com/TooTouch/MemSeg) | — | — | — | — | — |
| AD-based | CLIP | [GitHub](https://github.com/maticFuc/AnomalyVFM) | — | — | — | — | — |
| AD-based | DINOv2 | [GitHub](https://github.com/maticFuc/AnomalyVFM) | — | — | — | — | — |
| AD-based | DINOv3 | [GitHub](https://github.com/maticFuc/AnomalyVFM) | — | — | — | — | — |
| AD-based | RADIO | [GitHub](https://github.com/maticFuc/AnomalyVFM) | — | — | — | — | — |
| AD-based | SigLIP2 | [GitHub](https://github.com/maticFuc/AnomalyVFM) | — | — | — | — | — |
| COD-based | BASNet | [GitHub](https://github.com/xuebinqin/BASNet) | Adam | 1e-3 | 8 | 1000 | ReduceLROnPlateau |
| COD-based | SINet-v2 | [GitHub](https://github.com/GewelsJI/SINet-V2) | Adam | 1e-4 | 16 | 150 | Custom (Adjust LR) |
| COD-based | BGNet | [GitHub](https://github.com/thograce/BGNet) | Adam | 1e-4 | 12 | 100 | Custom (Poly LR) |
| COD-based | OCENet | [GitHub](https://github.com/Carlisle-Liu/OCENet) | Adam | 1e-5 | 4 | 50 | StepLR |
| COD-based | DGNet | [GitHub](https://github.com/gewelsji/dgnet) | AdamW | 5e-5 | 16 | 150 | CosineAnnealingLR |
| COD-based | HitNet | [GitHub](https://github.com/HUuxiaobin/HitNet) | AdamW | 1e-4 | 8 | 150 | Custom (Adjust LR) |
| COD-based | PCNet | [GitHub](https://github.com/yjybuaa/PlantCamo) | AdamW | 1e-4 | 8 | 150 | Custom (Adjust LR) |
| COD-based | CTF-Net | [GitHub](https://github.com/zcc0616/CTF-Net) | Adam | 1e-4 | 12 | 100 | Custom (Poly LR) |
| COD-based | ARNet | [GitHub](https://github.com/akuan1234/ARNet) | Adam | 5e-5 | 16 | 150 | Adjust LR |
| COD-based | CHNet | [GitHub](https://github.com/akuan1234/CHNet) | Adam | 5e-5 | 24 | 180 | Adjust LR |
| COD-based | ARNet-v2 | [GitHub](https://github.com/akuan1234/ARNet-v2) |Adam | 5e-5 | 8 | 200 | Adjust LR |
| COD-based | AINet | [GitHub](https://github.com/hvelesaca/AINet) | AdamW | 1e-4 | 16 | 150 | CosineAnnealingLR |

## Datasets 

### Used for supervised techniques
It is necessary to separate the datasets because the file hierarchy used by camouflage-based techniques differs from that used by anomaly-based techniques.

https://www.kaggle.com/datasets/hvelesaca/cds2k-dataset-supervised

### Used for unsupervised techniques
https://www.kaggle.com/datasets/hvelesaca/cds2k-dataset-unsupervised

##  Results
The qualitative mask results are available in the folder [results](results).
