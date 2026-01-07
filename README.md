# Multimodal House Price Prediction 

This project uses a fusion of **tabular data** and **satellite imagery** (ResNet-18) to predict property values.

##  How to Run
1. **Setup**: Install dependencies: `pip install -r requirements.txt`
2. **Data Fetching**: Add your Mapbox API key to `data_fetcher.py` and run it to download imagery.
3. **Preprocessing**: Run `preprocessing.ipynb` to generate the engineered features.
4. **Training & Inference**: Run `model_training.ipynb` to train the fusion model and generate `final_submission.csv`.

##  Key Engineering Features
- **Geospatial Anchors**: Luxury hubs and waterfront distances derived from training distributions to prevent data leakage.
- **Image Fusion**: 512-D ResNet-18 embeddings reduced to 15-D via PCA.
- **Robust Inference**: Mean-imputation used for missing test imagery to ensure 100% submission coverage.
