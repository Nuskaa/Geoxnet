# GeoXNet: A Hybrid XGBoost-CNN Framework for GIS-Based Land Classification

## Overview

GeoXNet is a hybrid machine learning and deep learning framework designed for GIS-based land-use and land-cover classification using satellite imagery and geospatial data.

The project explores the combination of traditional machine learning models, particularly XGBoost, with deep learning architectures such as ResNet-18 and EfficientNet-B0 to classify different land-cover categories.

## Objectives

- Process Sentinel-2 satellite imagery for land-cover analysis.
- Generate geospatial datasets using Google Earth Engine.
- Extract image patches for model training and evaluation.
- Implement and compare machine learning and deep learning models.
- Explore hybrid model architectures for improved classification performance.

## Datasets

The project uses the following publicly available data sources:

1. **IndiaSAT – Sentinel-2 Dataset**  
   https://github.com/hariomahlawat/IndiaSat

2. **Maharashtra Cadastral Parcels – Tier A**  
   https://huggingface.co/datasets/Ashutosh99/maharashtra-cadastral-tier-a

3. **Dynamic World – Land Cover Dataset**  
   https://developers.google.com/earth-engine/datasets/catalog/GOOGLE_DYNAMICWORLD_V1

### Data Preprocessing

Google Earth Engine was used to process satellite imagery and derive land-cover labels using Dynamic World data.

The processed data was exported as GeoTIFF files containing satellite image bands and corresponding labels. Image patches of size 32 × 32 pixels were subsequently extracted for the patch-based experiments.

## Methodology

The framework explores the following models:

### Machine Learning
- XGBoost
- Random Forest
- LightGBM
- CatBoost

### Deep Learning
- ResNet-18
- EfficientNet-B0

### Hybrid Models
- XGBoost + ResNet
- XGBoost + EfficientNet
- Other evaluated model combinations

## Land-Cover Classes

The patch-based image experiments use three available classes:

- Water
- Greenery
- Built-up

The separate tabular experiments include four classes:

- Water
- Greenery
- Barren
- Built-up

## Repository Structure

```text
GeoXNet/
│
├── GeoXNet_Implementation.ipynb  # Complete project implementation
├── README.md                     # Project documentation
└── requirements.txt              # Required Python libraries
```

## Implementation

The complete project implementation is available in the Jupyter Notebook:

**GeoXNet_Implementation.ipynb**

It includes data preprocessing, model implementation, training, evaluation, and result visualization.
## Technologies Used

- Python
- Google Colab
- Google Earth Engine
- XGBoost
- PyTorch
- Scikit-learn
- NumPy
- Pandas
- Rasterio
- Matplotlib

## Experimental Evaluation

The models are evaluated using the following metrics:

- Accuracy
- Precision
- Recall
- F1-score
- Cohen's Kappa
- Training and inference time

## Reproducibility

The implementation notebooks contain the preprocessing, model training, evaluation, and visualization workflows.

The generated GeoTIFF files and extracted image patches are experimental outputs and may be shared separately due to their file sizes.

## Limitations

- The experiments use a limited geographical study region.
- Dynamic World-derived labels are used as pseudo-labels.
- Spatial generalization requires validation across additional regions.
- The cadastral dataset does not provide land ownership information.
- Further evaluation with independent ground-truth labels is required.

## Future Work

- Extend experiments to multiple geographical regions.
- Incorporate multi-temporal satellite imagery.
- Evaluate models using independently validated land-cover labels.
- Explore integration with GIS-based land monitoring and governance applications.

## Authors

GeoXNet Research Team

## Acknowledgment

We acknowledge the providers of the publicly available satellite imagery, cadastral parcel data, and land-cover datasets used in this research.
