# FSA-AViT for Pediatric Dental Disease Classification

This repository presents the implementation of an intelligent deep learning framework for automated pediatric dental disease classification using panoramic dental radiographs. The proposed framework integrates image preprocessing, CNN-based feature extraction, feature tokenization, an Attention Vision Transformer (AViT), and Fine-Tuned Sandpiper Algorithm (FSA)-based optimization.

## Overview

The framework is designed to identify and classify pediatric dental diseases from panoramic radiographic images. LabelMe JSON annotations are used to identify annotated dental regions and their corresponding disease classes.

The implementation supports six dental disease categories:

- Dental Caries
- Periapical Periodontitis
- Pulpitis
- Deep Pits & Fissures
- Dental Developmental Anomalies
- Others

## Implementation Workflow

The overall workflow consists of:

1. Dataset Loading and LabelMe JSON Annotation Parsing
2. Dental Region of Interest (ROI) Extraction
3. Median Filtering
4. Grayscale Normalization
5. CNN-Based Multi-Scale Feature Extraction
6. Feature Tokenization
7. Positional Embedding
8. Attention Vision Transformer (AViT)
9. Fine-Tuned Sandpiper Algorithm (FSA) Optimization
10. Six-Class Dental Disease Classification

## Proposed FSA-AViT Framework

The proposed architecture combines a CNN-based feature encoder with an Attention Vision Transformer. The CNN component extracts multi-scale spatial representations from dental radiographs, while feature tokenization transforms the extracted feature maps into sequential tokens suitable for transformer processing.

The AViT component uses multi-head self-attention to capture global contextual relationships between dental image regions. The Fine-Tuned Sandpiper Algorithm optimizes selected model hyperparameters, including the learning rate and dropout rate.

## Model Configuration

- Input Image Size: 224 × 224
- Input Channels: 1 (Grayscale)
- Number of Classes: 6
- CNN Feature Embedding Dimension: 256
- Transformer Layers: 6
- Attention Heads: 8
- Classification Function: Softmax
- Optimizer: Adam with FSA-optimized parameters

## Evaluation Metrics

The model is evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score
- AUC
- Five-Fold Cross-Validation
- Statistical Significance Analysis
- Ablation Testing
- Number of Model Parameters
- GFLOPs
- Inference Time (ms/image)

## Ablation Study

Ablation experiments are performed to analyze the contribution of individual components of the proposed framework:

- Baseline SA
- FSA-AViT Without Preprocessing (PP)
- FSA-AViT Without Feature Extraction (FE)
- FSA-AViT Without FSA
- FSA-AViT Without AViT
- Complete FSA-AViT Proposed Model

## Requirements

The implementation requires Python and the following major libraries:

- TensorFlow
- Keras
- OpenCV
- NumPy
- Pandas
- Scikit-learn
- SciPy
- Matplotlib

## Dataset Structure

The expected dataset directory structure is:

    Pediatric dental disease detection dataset/
    ├── Train/
    │   ├── images/
    │   └── label/
    └── Test/
        ├── images/
        └── label/

The `label` directories contain LabelMe JSON annotation files corresponding to the panoramic dental radiographs.

## Cross-Validation

Five-fold cross-validation is used to evaluate the robustness and generalization capability of the proposed framework. Accuracy, Precision, Recall, F1-Score, and AUC are calculated for each fold.

## Statistical Analysis

Statistical significance analysis is conducted using the five-fold cross-validation results. The analysis includes:

- Mean ± Standard Deviation
- 95% Confidence Interval
- t-value
- p-value

## Disclaimer

This repository is intended for research and educational purposes. The framework is not intended to replace professional dental diagnosis or clinical decision-making.

## License

Please refer to the repository license for information regarding the use and distribution of this project.
