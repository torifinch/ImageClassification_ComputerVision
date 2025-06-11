# CIFAR-10 Image Classification with Transfer Learning (ResNet50)

A computer vision project using transfer learning with ResNet50 to classify CIFAR-10 images.  
Includes data augmentation, dropout regularization, AdamW optimizer, and EarlyStopping for improved generalization.

---

## 🚀 Project Overview

This project explores image classification on the CIFAR-10 dataset using a transfer learning approach. I used a pretrained ResNet50 model with ImageNet weights as a feature extractor and added a custom classification head.

To enhance model performance and prevent overfitting, I incorporated:

✅ **Image Resizing** to `64x64` resolution 
✅ Data augmentation (random horizontal flips and rotations)  
✅ Dropout layers in the classification head  
✅ AdamW optimizer with decoupled weight decay  
✅ EarlyStopping to monitor validation loss and stop training at the optimal point  

---

## 🗂️ Project Details

- **Model**: ResNet50 (`imagenet` weights, `include_top=False`)  
- **Training Data**: 10,000 CIFAR-10 images (32x32 px)  
- **Testing Data**: 10,000 CIFAR-10 images  
- **Loss Function**: `categorical_crossentropy` (labels one-hot encoded with `to_categorical()`)  
- **Optimizer**: AdamW  
- **Regularization**: Dropout + EarlyStopping  
- **Epochs**: 10 (frozen base) + 10 (fine-tuning)  

---

## 🏆 Final Results

**✅ 82.76% accuracy**  
**✅ Test loss: 0.5323**

This is a strong result considering the dataset size, small image resolution, and training constraints. These improvements raised accuracy by **+30%** compared to the baseline model.

---

## ⚙️ Tools & Libraries

- TensorFlow / Keras  
- ResNet50 pretrained on ImageNet  
- AdamW optimizer  
- Matplotlib for visualizations  

---

## 📚 Key Learnings

- How to apply transfer learning with ResNet50 to small image datasets  
- The importance of matching preprocessing to the pretrained model (`preprocess_input()`)  
- When to use `to_categorical()` with `categorical_crossentropy`  
- How data augmentation, dropout, and weight decay improve generalization  
- How EarlyStopping helps prevent overfitting  

---

## 🚀 Future Work

- Train on the full CIFAR-10 dataset (50,000 images)  
- Apply more advanced data augmentation (random zoom, brightness, contrast)  
- Experiment with different architectures better suited to small images (ResNet32, MobileNetV2)  
- Implement learning rate scheduling during fine-tuning  
- Further tuning of AdamW hyperparameters  

---

## 🎓 Author

**Victoria Finch**  
[Github Profile](https://github.com/torifinch)

---

