# Solar Panel Dust Detection using VGG16

This project uses transfer learning with the VGG16 model to classify solar panel images as either **Clean** or **Dusty**. The dataset is preprocessed with image augmentation, split into training, validation, and test sets, and trained with class balancing to improve performance.

## 📂 Dataset
Two datasets from Kaggle were combined:
(https://www.kaggle.com/datasets/hemanthsai7/solar-panel-dust-detection/data)

## 🧠 Model
- Base Model: **VGG16** (pretrained on ImageNet, frozen)
- Custom Head: Flatten → Dense(256, ReLU) → Dropout(0.5) → Dense(2, Softmax)
- Optimizer: Adam | Loss: Categorical Crossentropy

## ⚙️ Key Features
- Data Augmentation (rotation, zoom, shift, brightness)
- Class Weighting for imbalance handling
- Visualization of predictions and performance
- Final model saved as `my_trained_vgg16_model.keras`

## 📊 Results
- Achieved high accuracy on validation and test sets
- Visual inspection confirms effective predictions

## 🏁 How to Run
This notebook is designed to run in a Kaggle environment with the provided datasets. Simply execute all cells to preprocess data, train the model, and evaluate performance.

## 📁 Output
- Trained model saved as: `my_trained_vgg16_model.keras`
- Accuracy/Loss plots and prediction visualizations

---

**Author**: Swapnil Paranjape  
**Environment**: Python, TensorFlow, Keras, Matplotlib, Seaborn

