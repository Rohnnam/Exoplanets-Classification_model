# Exoplanet Detection Model

This project implements a machine learning model to detect exoplanets using a dataset of astronomical observations. The model is built using LSTM (Long Short-Term Memory) networks, which are particularly effective for sequential data.

## Project Overview

The model is trained on a dataset containing a total of **56,461 samples**, with **27,994 positive samples** (exoplanets) and **28,467 negative samples** (non-exoplanets). The goal is to accurately classify these samples based on their features.

### Model Performance

- **Training Accuracy**: 99.24%
- **Validation Accuracy**: 99.65%
- **Test Accuracy**: 99.68%
- **Precision**: 99.98%
- **Recall**: 99.37%
- **Total Samples**: 56,461
- **Positive Samples**: 27,994
- **Negative Samples**: 28,467

### Learning Curves

![Model Accuracy and Loss](Exoplanet_latest.png)

### Light Curve Visualization

![Light Curve Around Exoplanet](Exoplanet_graph_balanced.png)

## Dependencies

To run this project, you need the following Python packages:

- `pandas`
- `numpy`
- `scikit-learn`
- `tensorflow`
- `keras`
- `matplotlib`
- `concurrent.futures`

***Disclaimer:***
The exoplanet detection model presented in this project is intended for educational and research purposes. While the model demonstrates high accuracy and performance metrics, it is essential to understand that the results may not be applicable to all datasets or real-world scenarios. Users are encouraged to validate the model's performance on their specific datasets before deploying it for practical applications.

***Limitations:***

**Dataset-Specific Results:**<br>
The model's performance is closely tied to the dataset it was trained on, which primarily consists of light curve data from specific space missions such as Kepler or TESS. The accuracy and generalization of the model may vary when applied to data from other sources or with different characteristics.

**Model Sensitivity to Noise:**<br>
The deep learning model may be sensitive to noise in the light curve data, such as instrument errors or cosmic interference. This could lead to false positives or negatives in exoplanet detection, particularly in cases where the light curves are noisy or incomplete.

**Simplification of Complex Phenomena:**<br>
The model assumes that light curves can be accurately interpreted by a deep learning algorithm without accounting for all astrophysical phenomena. This simplification may lead to misclassification in cases where other astrophysical events (e.g., stellar flares, binary stars) mimic or obscure the signals of exoplanets.

**Limited Feature Scope:**<br>
The model focuses on a predefined set of features extracted from light curves. Additional factors, such as stellar activity, orbital mechanics, or multi-planet systems, are not explicitly modeled and could affect the detection and classification outcomes.

**Generalization to New Data:**<br>
While the model may perform well on the dataset it was trained on, its ability to generalize to new, unseen data (especially from different stellar environments or instruments) is not guaranteed. Users should exercise caution when applying the model to data outside the scope of the training set.

**Ethical and Interpretive Considerations:**<br>
The interpretation of results produced by deep learning models should be conducted with caution. The "black-box" nature of these models means that their decision-making process is not always transparent, which can pose challenges for scientific interpretation and ethical use.

**Dependence on Preprocessing Steps:**<br>
The model's effectiveness is dependent on the quality and consistency of the preprocessing steps applied to the light curve data. Any deviation in these steps could impact the model's ability to accurately detect and classify exoplanets.

```bash
git clone https://github.com/yourusername/exoplanet-detection.git
cd exoplanet-detection
pip install -r requirements.txt
python main.py

