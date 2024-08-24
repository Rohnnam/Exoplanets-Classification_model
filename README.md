# Exoplanet Models

**Exoplanet Detection via light curve data:** <br>

This project implements an advanced machine learning model designed to detect exoplanets—celestial bodies that orbit stars outside our solar system—utilizing a rich dataset of astronomical observations. The model is built on Long Short-Term Memory (LSTM) networks, which excel in processing sequential data, making them particularly suitable for analyzing light curves generated by exoplanets transiting their host stars. <br>

The model is trained on a dataset comprising a total of 56,461 light curve samples, including 27,994 positive samples (indicative of confirmed exoplanets) and 28,467 negative samples (representing various astrophysical phenomena such as stellar variability and noise). By leveraging sophisticated feature extraction techniques and deep learning methodologies, the model aims to discern subtle variations in light intensity that signal the presence of an exoplanet. <br>

**Exoplanet habitability:** <br>

Building upon our exoplanet detection capabilities, this project extends our research into the realm of exoplanet habitability classification. Utilizing data from the NASA Exoplanet Archive,and implenting data augmentation techniques like weighted combination of features with added noise, we've developed a sophisticated machine learning model to assess the potential habitability of detected exoplanets.
Our habitability classification model employs a hybrid Convolutional Neural Network (CNN) and Long Short-Term Memory (LSTM) architecture, designed to capture both spatial and temporal features of exoplanetary systems. The model analyzes a multitude of parameters including, but not limited to:

- Planetary equilibrium temperature (pl_eqt)
- Planetary radius (pl_rade)
- Orbital period (pl_orbper)
- Semi-major axis (pl_orbsmax)
- Stellar effective temperature (st_teff)
- Stellar mass (st_mass)
- Stellar metallicity (st_met)


### Model Performance

**Exoplanet_detection model**
- **Training Accuracy**: 99.24%
- **Validation Accuracy**: 99.65%
- **Test Accuracy**: 99.68%
- **Precision**: 99.98%
- **Recall**: 99.37%
- **Total Samples Trained**: 56,461

**Exoplanet_habitability_model**
- **Training Accuracy**: 81.0%
- **Validation Accuracy**: 80.0%
- **Test Accuracy**: 81.50%
- **Total Samples Trained**: 5000

## License
This project is licensed under the [MIT License](LICENSE.md).


### Learning Curves

![Model Accuracy and Loss](Exoplanet_latest.png)

### Light Curve Visualization

![Light Curve Around Exoplanet](Exoplanet_graph_balanced.png)


These results underscore the model's capability to effectively differentiate between exoplanets and other astrophysical objects, even amidst the complexities of stellar environments and the inherent noise present in astronomical data. The training process incorporates techniques such as Principal Component Analysis (PCA) for dimensionality reduction, ensuring that the model can efficiently handle the high-dimensional feature space typical of light curve data.<br>

Utilizing data from notable space missions like Kepler and TESS, this model not only enhances the accuracy of exoplanet detection but also contributes to the broader field of astrophysics by providing insights into planetary formation and the potential for habitable worlds. By employing advanced regularization techniques and class balancing strategies, the model is designed to mitigate overfitting and improve generalization to unseen data, thereby advancing our understanding of diverse planetary systems and their characteristics.

## Dependencies

To run this project, you need the following Python packages:

- `pandas`
- `numpy`
- `scikit-learn`
- `tensorflow`
- `keras`
- `matplotlib`
- `concurrent.futures`
- [Exoplanet Archive Table View](https://exoplanetarchive.ipac.caltech.edu/cgi-bin/TblView/nph-tblView?app=ExoTbls&config=PS)


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
git clone https://github.com/Rohnnam/Exoplanet-models.git
cd Exoplanet-models
pip install -r requirements.txt
python main.py

