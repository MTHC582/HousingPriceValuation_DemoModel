# Satellite Housing Valuation: The "ENGINE + BRAIN" Approach

### _A Multimodal Deep Learning Pipeline for Real Estate_

> **"Combining the raw calculation power of numbers (ENGINE) with the visual intuition of satellite imagery (BRAIN)."**

This project implements a **Multimodal Neural Network** that fuses traditional tabular data (bedrooms, sqft, location) with high-resolution **Satellite Imagery** to predict property values. By "looking" at the neighborhood context (greenery, density, road proximity) via a CNN, the model captures value drivers that spreadsheets alone miss.

---

## Project Overview

**The Challenge:** Traditional valuation models relying solely on spreadsheets (Tabular Data) fail to capture "Curb Appeal" or "Neighborhood Vibes."
**The Solution:**

- **The ENGINE (Tabular Branch):** A Feed-Forward Network (FFN) processes exact housing specs (bed, bath, sqft) using `pandas` and `openpyxl`.
- **The BRAIN (Visual Branch):** A ResNet-based CNN processes satellite images to extract environmental features.
- **The Data:** A custom dataset of **22,000 properties**, with imagery programmatically fetched via the **Mapbox Static API**. (Took about 2.3 GB of DATA,as per the mentioned tools)

---

## NOTE:

I used python 3.11 since it supports the CUDA. To avoid discrepancies, would suggest the same.

---

## 📂 Repository Structure

```text
Satellite_Housing_Valuation_DemoModel/
│
├── README.md               # Project Documentation
├── requirements.txt        # Dependencies (Locked for Python 3.11 + CUDA)
├── src/
│   ├── dataset.py          # Custom PyTorch Dataset (Handles Images + Excel)
│   ├── models.py           # Hybrid Neural Network (CNN + FFN)
│   ├── train.py            # Training Loop (CUDA-enabled)
│   ├── predict.py          # Inference Script (Actual vs Predicted Table)
│   └── visualize.py        # Generates Regression Scatter Plots
│
├── data/
│   ├── train(1).xlsx       # Base Tabular Data
|   ├── test2.xlsx          # Testing Data
│   └── images/             # 22k Satellite Images (Fetched via Mapbox)
│
└── best_model.pth      # Saved Model Weights

```

---

**_Further details are provided along .py files itself._**
