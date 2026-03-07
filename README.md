# Computer Vision - Image Classification
This project is my homework for CIS 9660 - Data Mining for Business Analytics.
### Pizza or Not Pizza?
**A computer vision project that converts raw food images into 40,000-feature vectors, benchmarks 7 machine learning algorithms, and serves predictions through a lightweight Flask app.**

On a balanced dataset of 1,966 images, the best model achieved **70.68% accuracy** and **0.705 weighted F1** on a held-out 590-image test set.

| Area | Step |
|---|---|
| Problem Solving | Built an end-to-end binary **image classification workflow** from raw image files to prediction interface |
| Computer Vision | Engineered **color, texture, and edge-based** features from images |
| Machine Learning | Benchmarked 7 algorithms: **Logistic Regression, GaussianNB, Decision Tree, Random Forest, SVC, KNN, and KMeans** |
| Experimental Rigor | Used a 70/30 train-test split plus **5-fold cross-validation** on the training set |
| Evaluation | Compared models with accuracy, precision, recall, and F1-score |
| Deployment | Created a **Flask app** for upload-and-predict inference |
| Tech Stack | Python, NumPy, pandas, scikit-image, scikit-learn, Matplotlib, Seaborn, Flask |

## Project Snapshot

- **Objective:** Classify whether an image contains pizza or not.
- **Dataset:** Kaggle pizza/not-pizza dataset with **983 pizza** images and **983 non-pizza** images.
- **Train/Test Split:** **1,376** training images and **590** test images.
- **Feature Engineering:** Resized images to `100 x 100` and extracted average RGB intensity, Local Binary Pattern (LBP) texture features, and horizontal plus vertical Prewitt edge features.
- **Feature Space:** `40,000` engineered features per image.
- **Modeling Approach:** Compared linear, probabilistic, tree-based, kernel-based, instance-based, and clustering methods.

## Workflow

- Loaded and explored a balanced image dataset from Kaggle.
- Visualized random pizza and non-pizza samples to understand class variability.
- Built a reusable feature extraction pipeline for image color, texture, and edge structure.
- Trained and evaluated 7 machine learning models on the same engineered feature set.
- Ranked models using cross-validation and holdout test performance.
- Developed a Flask web app prototype so a user can upload an image and receive a prediction.

## Results

| Model | Accuracy | Weighted Precision | Weighted Recall | Weighted F1 |
|---|---:|---:|---:|---:|
| GaussianNB | **0.7068** | **0.7151** | **0.7068** | **0.7051** |
| RandomForestClassifier | 0.6966 | 0.6990 | 0.6966 | 0.6964 |
| SVC | 0.6610 | 0.6688 | 0.6610 | 0.6588 |
| DecisionTreeClassifier | 0.5797 | 0.5813 | 0.5797 | 0.5793 |
| LogisticRegression | 0.5441 | 0.5433 | 0.5441 | 0.5425 |
| KNeighborsClassifier | 0.5102 | 0.2629 | 0.5102 | 0.3470 |
| KMeans | 0.4017 | 0.3998 | 0.4017 | 0.3949 |


