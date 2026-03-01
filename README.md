# AI-for-sustainbility

# Land Cover Classification (Delhi NCR)

A simple Deep Learning project that classifies Earth Observation satellite images into 5 land cover categories using PyTorch and a pre-trained ResNet18 model.

## Dataset
* **Images:** 128x128 RGB satellite image patches from the Delhi NCR region.
* **Labels:** ESA WorldCover 2021 data. The original 11 classes are simplified into 5 main categories: Built-up, Vegetation, Water, Cropland, and Others.

## Tech Stack
* **Deep Learning:** PyTorch, Torchvision (ResNet18)
* **Data Processing:** Rasterio,Pandas, NumPy
* **Evaluation & Splitting:** Scikit-Learn
* **Visualization:** Matplotlib, Seaborn

## Project Workflow
1. **Data Extraction:** Reads a raw `.tif` map and extracts 128x128 pixel patches matching specific coordinate locations.
2. **Data Prep:** Maps raw ESA codes to the 5 simplified categories and splits the data 60/40 (Train/Test).
3. **Training:** Loads the images into a custom PyTorch `Dataset` and trains a modified ResNet18 CNN.
4. **Evaluation:** Tests the model on unseen data and outputs the final Accuracy, F1-Score, and a Confusion Matrix heatmap.

##Dataset 
Download the dataset here: `https://www.kaggle.com/datasets/rishabhsnip/earth-observation-delhi-airshed/code`
