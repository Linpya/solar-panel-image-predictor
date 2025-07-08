# Solar Panel Dust Detection using VGG16

This project uses transfer learning with the VGG16 model to classify solar panel images as either **Clean** or **Dusty**. It applies data augmentation and class balancing, and trains a deep learning model to detect dust accumulation on solar panels.

---

## 📊 Dataset Summary

- **Train Set**: 2,390 images  
  - Clean: 1,411  
  - Dusty: 979

- **Test Set**: 738 images  
  - Clean: 425  
  - Dusty: 313

- **Validation Set**: 369 images  
  - Clean: 212  
  - Dusty: 157

---

## 🧠 Model Architecture

| Layer         | Output Shape     | Parameters |
|---------------|------------------|------------|
| VGG16 (frozen)| (None, 9, 9, 512)| 14,714,688 |
| Flatten       | (None, 41472)    | 0          |
| Dense (ReLU)  | (None, 256)      | 10,617,088 |
| Dropout (0.5) | (None, 256)      | 0          |
| Dense (Softmax)| (None, 2)       | 514        |
| **Total**     |                  | **25,332,290** |

---

## ✅ Evaluation Results

- **Test Accuracy**: 81.98%  
- **Test Loss**: 0.4457

---

## 🔧 Key Features

- VGG16 transfer learning with custom classifier head
- Real-time data augmentation for improved generalization
- Class weighting to handle data imbalance
- Visualization of predictions with true and predicted labels

---

## 💾 Output

- Trained model saved as: `my_trained_vgg16_model.keras`
- Accuracy/loss plots and labeled test image visualizations

---

## 📁 Dataset Sources
(https://www.kaggle.com/datasets/hemanthsai7/solar-panel-dust-detection/data)


**Author**: Swapnil Paranjape  
**Tools**: TensorFlow, Keras, PIL, Matplotlib, Seaborn  
**Environment**: Python

