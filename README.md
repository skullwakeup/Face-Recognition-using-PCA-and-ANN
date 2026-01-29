# Face-Recognition-using-PCA-and-ANN
An end-to-end face recognition system using PCA-based Eigenfaces for dimensionality reduction and ANN for classification, with performance analysis on different PCA dimensions and imposter detection.
# Face Recognition using PCA and ANN

## 📌 Project Overview
This project implements a **Face Recognition System** using **Principal Component Analysis (PCA)** for feature extraction (Eigenfaces) and an **Artificial Neural Network (ANN)** for classification.

The main objective is to reduce the high-dimensional facial image space into a lower-dimensional feature space using PCA and then recognize faces using a trained neural network.

---

## 🧠 Methodology

### Training Phase
1. Face images are read using OpenCV and converted into column vectors.
2. A **mean face** is computed from the training dataset.
3. Mean normalization is performed by subtracting the mean face from each image.
4. A **surrogate covariance matrix** is calculated to reduce computational complexity.
5. Eigenvalues and eigenvectors are obtained using PCA.
6. Top **k eigenvectors** (Eigenfaces) are selected based on descending eigenvalues.
7. Each face is projected into Eigenface space to generate **face signatures**.
8. An **Artificial Neural Network (ANN)** is trained using these signatures.

---

### Testing Phase
1. Test image is converted into a column vector.
2. Mean normalization is applied.
3. Image is projected onto the Eigenface space.
4. The trained ANN predicts the identity of the face.
5. Imposter faces (unknown persons) are detected as **not enrolled**.

---

## 📊 Experiments & Evaluation
- Dataset split: **60% training, 40% testing**
- Accuracy evaluated by varying the number of Eigenfaces (**k**)
- A graph is plotted between **classification accuracy vs k**
- Imposter detection is tested using unseen faces

---

## 📈 Results
The system shows that recognition accuracy improves with increasing `k` up to an optimal point, after which overfitting may occur.

---

## 📂 Dataset
Dataset used for this project:
(https://drive.google.com/file/d/1KU-usOIMtV2somSrVu9RJclHiHQgvpCD/view?usp=drive_link)


---

## 🛠️ Technologies Used
- Python
- NumPy
- SciPy
- OpenCV
- Scikit-learn
- Matplotlib

---

## 🚀 How to Run
1. Clone the repository
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
