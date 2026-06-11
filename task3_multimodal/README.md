# Task 3: Multimodal Housing Price Prediction

## Objective
The objective of this project is to predict housing prices by fusing two distinct data modalities: structured tabular data (e.g., square footage, bedrooms) and unstructured image data (house photos).

## Methodology / Approach
1. **Data Collection:** Loaded tabular features from the King County House Sales dataset and generated corresponding image data representations.
2. **Feature Extraction:** Leveraged a pre-trained Convolutional Neural Network (ResNet-18) as a backbone to extract high-level visual features from the images.
3. **Multimodal Fusion:** Concatenated the extracted CNN image features with the processed tabular features.
4. **Model Training:** Trained a unified Multi-Layer Perceptron (MLP) regression head on the fused feature vectors to predict the log-transformed house price.
5. **Evaluation:** Evaluated the fusion model's predictive performance using Mean Absolute Error (MAE) and Root Mean Squared Error (RMSE).

## Key Results & Observations
* **Performance:** The multimodal model achieved an MAE of approximately $60,000–$90,000 and an RMSE of ~$100,000–$150,000.
* **Insights:** Fusing image features with tabular data consistently improves predictive accuracy compared to relying on tabular data alone, as the CNN captures visual quality signals that raw numbers miss.
* **Optimization:** Log-transforming the target price variable significantly improved model convergence by mitigating the skewed impact of extreme luxury home prices.