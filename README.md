# Face_Recognition
This code implements face recognition using PCA and LDA techniques on the ORL dataset, achieving accurate classification results.

This repository contains the code implementation for the face recognition project (College Group Project). The project aims to recognize subjects based on facial images using the ORL dataset. The code is organized into several steps to achieve the goal of face recognition.

## Dataset and Format
- The ORL dataset is downloaded from the provided link.
- The dataset consists of grayscale images, each with a size of 92x112 pixels.
- There are 10 images per subject, totaling 40 subjects.
## Data Preprocessing
- The code generates a Data Matrix (D) and a Label vector (y) from the dataset.
- Each image is converted into a vector of 10,304 values corresponding to its size.
- The Data Matrix is stacked by combining the vectors from all images.
- The Label vector assigns integer labels from 1 to 40 representing subject IDs.
## Training and Testing Split
- The dataset is split into training and test sets.
- Odd rows of the Data Matrix are used for training, providing 5 instances per person.
- Even rows of the Data Matrix are used for testing, also providing 5 instances per person.
- The Label vector is split accordingly for training and testing.
## Classification using PCA
- PCA (Principal Component Analysis) is performed on the training set.
- The projection matrix (U) is computed using different alpha values.
- The training and test sets are projected onto the same U matrix.
- A simple Nearest Neighbor classifier is used to assign class labels.
- The accuracy is reported for each alpha value.
## Classification using LDA
- LDA (Linear Discriminant Analysis) is applied for multiclass classification.
- Mean vectors and scatter matrices are calculated for each class.
- Between-class scatter matrix (Sb) is obtained.
- Within-class scatter matrices (S1, S2, ..., S40) are summed.
- The projection matrix (U39x10304) is obtained using 39 dominant eigenvectors.
- The training and test sets are projected onto the U matrix.
- Nearest Neighbor classifier is used to assign class labels.
- The accuracy of multiclass LDA is reported.
## Classifier Tuning
- The K-NN (K-Nearest Neighbor) classifier is tuned by varying the number of neighbors (K).
- Performance measures, such as accuracy, are computed for different K values.
- Results are plotted or tabulated for both PCA and LDA.
## Face vs. Non-Face Images
- Non-face images are downloaded and resized to the same dimensions as the face images.
- Classification is performed to distinguish between faces and non-faces.
- Success and failure cases are analyzed and presented.
- The optimal number of dominant eigenvectors for LDA is determined.
- Accuracy is plotted against the number of non-face images while fixing the number of face images.
- Critique of accuracy measure for large numbers of non-face images in the training data is provided.
## Bonus
- Bonus tasks include a different training and test split and exploring variations of PCA and LDA algorithms.
- The performance and accuracy are compared between different training splits.
- Additional PCA and LDA models beyond the original algorithms are implemented and compared in terms of time complexity and accuracy.
For detailed information, please refer to the project report.

## Note
This description provides an overview of the code implementation for the face recognition project. For more detailed information and insights, please refer to the project report.
