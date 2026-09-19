# Unveiling Hidden Defects: Camouflaged Object Detection for Industrial Defect Localization
Industrial anomaly detection faces a fundamental challenge: surface defects often share nearly identical spectral, textural, and geometric properties with their surrounding material, creating a form of visual camouflage that confounds conventional inspection systems. We reframe industrial defect localization as a camouflaged object detection (COD) problem and conduct a comprehensive evaluation on CDS2K, the largest benchmark for camouflaged defect segmentation, comparing eight anomaly detection (AD) approaches against twelve COD-based architectures. The best COD model (ARNet-v2) outperforms the best AD model (RADIO) by over 24\% in pixel-level F1 and AP metrics overall, while remaining competitive at image-level classification and using architectures orders of magnitude smaller than VFM-based detectors. These findings indicate that, under the zero-shot/supervised comparison regime evaluated here, COD-based architectures are a more effective and efficient paradigm than the VFM-based AD detectors considered for pixel-level, low-contrast industrial defect segmentation on CDS2K; we discuss the supervision asymmetry between the two families of methods and its implications for the fairness of this comparison. 


## Dataset used for supervised techniques
https://www.kaggle.com/datasets/hvelesaca/cds2k-dataset-supervised

##  Dataset used for unsupervised techniques
https://www.kaggle.com/datasets/hvelesaca/cds2k-dataset-unsupervised
