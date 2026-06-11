# MOSAIC – Motif-based Surface Alignment & Inference of Cortex

![Pipeline](https://github.com/metrics-lab/MOSAIC/blob/main/%E2%80%8EMOSCAIC_pitch.%E2%80%8Epng.png)


Cortical folding emerges rapidly across the perinatal period, and its pattern varies strikingly between individuals. This variability is a problem for standard surface registration, which assumes a one-to-one correspondence between every subject and a single template and so tends to smooth away precisely the folding differences we want to measure. Motif-based approaches address this by matching each subject to the most similar pattern in a library of folding templates rather than forcing everyone onto one average, preserving individual morphology while still enabling group analysis. MOSAIC brings this idea to fetal and neonatal data, combining motif selection, label propagation, and feature extraction into a single pipeline whose outputs support normative modelling of how folding develops – and where individual brains deviate.

Given a new subject's hemisphere surface, MOSAIC aligns it to HCP space, registers it against a library of folding-motif templates, and selects the closest motif by Deep-Discrete spherical Registration (DDR) and multifacet similarity scores. Using Multimodel surface Matching (MSM), it propagates each template's segmentation and sulcal-fundus labels onto the subject, then extracts surface features (sulcal length, width, cortical thickness, folding extent) in native space. Outputs feed into normative modelling of folding morphometry across perinatal age. The hackathon focuses on label propagation, feature extraction, batch processing of the dHCP cohort, and wiring the feature table into the GP normative-modelling code – packaged as a runnable tool with example data.




# Reference
1. Guo, Yourong, et al. "Motifs of brain cortical folding from birth to adulthood: structural asymmetry and folding-functional links." bioRxiv (2025): 2025-03.
2. Suliman, Mohamed A., et al. "A deep-discrete learning framework for spherical surface registration." International Conference on Medical Image Computing and Computer-Assisted Intervention. Cham: Springer Nature Switzerland, 2022.
