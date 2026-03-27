
# PCA and K-Means Clustering: Evaluating the Impact of Dimensionality Reduction

## Author: Irshad Patan
## Student ID: 24147104
## Module: Advanced Machine Learning
## Repository: https://github.com/patanirshad3818-lgtm/PCA_Before_K-means.git 

### Project Overview

This project investigates the effect of Principal Component Analysis (PCA) on K-Means clustering performance.

Clustering algorithms such as K-Means rely heavily on Euclidean distance. In high-dimensional datasets, distance metrics may become less informative due to the curse of dimensionality. PCA reduces dimensionality by projecting data onto orthogonal components that maximise variance.

This tutorial explores:

K-Means clustering on standardised data
PCA as a preprocessing step
K-Means clustering after PCA
Comparison using inertia and silhouette score
Analytical discussion of when PCA improves clustering

The objective is not only to implement these techniques but to critically evaluate their interaction.

 ### Dataset

The project uses the Wine dataset from sklearn.datasets.

Dataset characteristics:

178 samples
13 numerical features
3 underlying wine classes (not used during clustering)

All features are standardised before applying PCA or K-Means.

 ### Methods Implemented
**1. Data Preprocessing**
Standardisation using StandardScaler
Ensures equal contribution of features
**2. Baseline Clustering**
K-Means with K = 3
Evaluation using:
Inertia (within-cluster sum of squares)
Silhouette score
**3. Dimensionality Reduction**
PCA applied to scaled data
Explained variance analysis
Reduction to 2 principal components for visualisation
**4. Clustering After PCA**
K-Means applied to PCA-transformed data
Performance comparison with baseline
### Evaluation Metrics
Inertia: Measures within-cluster compactness.
Silhouette Score: Measures separation between clusters.

Higher silhouette scores indicate better-defined clusters.

### Repository Structure
PCA_KMeans_Clustering/
│
├── PCA_KMeans_Tutorial.ipynb      # Main notebook
├── PCA_KMeans_Report.pdf          # Final report (if submitted as PDF)
├── README.md                      # Project overview
├── LICENSE                        # License file
⚙️ Requirements

This project uses Python 3 and the following libraries:

numpy
pandas
matplotlib
scikit-learn

Install dependencies using:

pip install numpy pandas matplotlib scikit-learn
### How to Run the Notebook
Clone the repository:
git clone https://github.com/your-username/PCA_KMeans_Clustering.git
Navigate to the project directory:
cd PCA_KMeans_Clustering
Launch Jupyter Notebook:
jupyter notebook
Open PCA_KMeans_Tutorial.ipynb and run all cells.

The notebook is designed to run from top to bottom without modification.

### Key Findings
PCA significantly improves cluster visual interpretability.
Moderate dimensionality reduction can improve clustering quality.
Over-reduction may cause information loss.
K-Means performance is sensitive to feature geometry.

The interaction between PCA and K-Means is nuanced and context-dependent.

### Ethical Considerations

Clustering results may influence decisions in domains such as healthcare and finance. Dimensionality reduction may remove meaningful attributes or obscure bias.

This project highlights the importance of:

Transparent preprocessing
Careful metric interpretation
Awareness of information loss

Unsupervised models should be treated as exploratory tools rather than objective truth.

### References

Bishop, C.M. (2006) Pattern Recognition and Machine Learning. Springer.

Hastie, T., Tibshirani, R. and Friedman, J. (2009) The Elements of Statistical Learning. Springer.

Jolliffe, I.T. (2002) Principal Component Analysis. Springer.

MacQueen, J. (1967) ‘Some methods for classification and analysis of multivariate observations’, Proceedings of the Fifth Berkeley Symposium.

### License

This project is released under the MIT License. See the LICENSE file for details.
