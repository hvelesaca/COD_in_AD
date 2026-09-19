# Unveiling Hidden Defects: Camouflaged Object Detection for Industrial Defect Localization
Industrial anomaly detection faces a fundamental challenge: surface defects often share nearly identical spectral, textural, and geometric properties with their surrounding material, creating a form of visual camouflage that confounds conventional inspection systems. We reframe industrial defect localization as a camouflaged object detection (COD) problem and conduct a comprehensive evaluation on CDS2K, the largest benchmark for camouflaged defect segmentation, comparing eight anomaly detection (AD) approaches against twelve COD-based architectures. The best COD model (ARNet-v2) outperforms the best AD model (RADIO) by over 24\% in pixel-level F1 and AP metrics overall, while remaining competitive at image-level classification and using architectures orders of magnitude smaller than VFM-based detectors. These findings indicate that, under the zero-shot/supervised comparison regime evaluated here, COD-based architectures are a more effective and efficient paradigm than the VFM-based AD detectors considered for pixel-level, low-contrast industrial defect segmentation on CDS2K; we discuss the supervision asymmetry between the two families of methods and its implications for the fairness of this comparison. 

# Github repositories
\begin{table*}[!h]
    \centering
    \caption{Details of the training parameters used in evaluated techniques. Learning rate (LR); Batch size (BS).}
    \vspace{0.1cm}
    %\resizebox{1.0\columnwidth}{!}{
    \begin{tabular}{cl|lcccccc}
        \toprule
        & Technique & Repository & Optimizer & LR & BS & Epochs & Scheduler \\
        \midrule
\multirow{8}{*}{\rotatebox{90}{AD-based}} & DRAEM & \url{https://github.com/VitjanZ/DRAEM} \\ 
        & MMR & \url{https://github.com/zhangzilongc/MMR} \\ % 28.5
        & MemSeg & \url{https://github.com/TooTouch/MemSeg} \\ % 12.3
        & CLIP & \url{https://github.com/maticFuc/AnomalyVFM} \\
        & DINOv2 & \url{https://github.com/maticFuc/AnomalyVFM} \\
        & DINOv3 & \url{https://github.com/maticFuc/AnomalyVFM} \\
        & RADIO & \url{https://github.com/maticFuc/AnomalyVFM} \\
        & SigLIP2 & \url{https://github.com/maticFuc/AnomalyVFM} \\ 

\midrule

\multirow{12}{*}{\rotatebox{90}{COD-based}} & BASNet & \url{https://github.com/xuebinqin/BASNet} & Adam & 1e-3 & 8 & 1000 & ReduceLROnPlateau \\
& SINet-v2 & \url{https://github.com/GewelsJI/SINet-V2} & Adam & 1e-4 & 16 & 150 & Custom (Adjust LR) \\
& BGNet & \url{https://github.com/thograce/BGNet} & Adam & 1e-4 & 12 & 100 & Custom (Poly LR) \\
%& C$^{2}$F-Net & \url{https://github.com/thograce/C2FNet} & AdaXW & 1e-4 & 32 & 50 & Custom (Poly LR) \\
& OCENet & \url{https://github.com/Carlisle-Liu/OCENet} & Adam & 1e-5 & 4 & 50 & StepLR \\
%& EAMNet & \url{https://github.com/sdy1999/EAMNet} & AdamW & 5e-5 & 16 & 150 & Custom (Adjust LR) \\
& DGNet & \url{https://github.com/gewelsji/dgnet} & AdamW & 5e-5 & 16 & 150 & CosineAnnealingLR \\
& HitNet & \url{https://github.com/HUuxiaobin/HitNet} & AdamW & 1e-4 & 8 & 150 & Custom (Adjust LR) \\
& PCNet & \url{https://github.com/yjybuaa/PlantCamo} & AdamW & 1e-4 & 8 & 150 & Custom (Adjust LR) \\
& CTF-Net & \url{https://github.com/zcc0616/CTF-Net} & Adam & 1e-4 & 12 & 100 & Custom (Poly LR) \\
& ARNet & \url{https://github.com/akuan1234/ARNet} \\
& CHNet & \url{https://github.com/akuan1234/CHNet} \\
& ARNet-v2 & \url{https://github.com/akuan1234/ARNet-v2} \\
& AINet & \url{https://github.com/hvelesaca/AINet} & AdamW & 1e-4 & 16 & 150 & CosineAnnealingLR \\
        \bottomrule
    \end{tabular}
    %}
    \label{tab:cod_repositories}
\end{table*}

## Dataset used for supervised techniques
https://www.kaggle.com/datasets/hvelesaca/cds2k-dataset-supervised

##  Dataset used for unsupervised techniques
https://www.kaggle.com/datasets/hvelesaca/cds2k-dataset-unsupervised
