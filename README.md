# German Traffic Sign Recognition Benchmark (GTSRB) 🚦

A deep learning project utilizing a Convolutional Neural Network (CNN) to classify 43 unique types of German traffic signs. This model is designed to assist in autonomous driving research and computer vision tasks.

## 📊 Dataset Overview
The project uses the **GTSRB (German Traffic Sign Recognition Benchmark)**, a multi-class, single-image classification challenge.
- **Classes:** 43 distinct traffic sign categories (Speed limits, yield, stop, warnings, etc.).
- **Data Source:** [Kaggle - German Traffic Sign Dataset](https://www.kaggle.com/datasets/meowmeowmeowmeowmeow/gtsrb-german-traffic-sign)



## 🧠 Model Architecture
The core of this project is a Sequential CNN optimized for $32 \times 32$ RGB images:

* **Convolutional Layers:** Multiple stages of feature extraction using 3x3 filters.
* **Regularization:** Integration of `Dropout` layers to prevent overfitting and `BatchNormalization` for stable training.
* **Downsampling:** `MaxPooling2D` layers to reduce spatial dimensions and focus on high-level features.
* **Output Layer:** A 43-unit Dense layer with `Softmax` activation to produce a probability distribution across all sign types.

## ⚙️ Training Specifications
- **Optimizer:** Adam
- **Loss Function:** `SparseCategoricalCrossentropy`
- **Input Shape:** $(32, 32, 3)$
- **Performance:** Achieved ~99.73% validation accuracy (20% subset of the training dataset).



## 🔮 Inference & Usage
A custom prediction script that can handle local paths.
