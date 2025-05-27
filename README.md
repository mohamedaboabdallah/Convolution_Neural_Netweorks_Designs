# 📚 CNN Model Comparison and ResNet50 Transfer Learning Tutorial

## 📊 CNN Architecture Comparison Table

| Feature              | **ResNet50**            | **InceptionV3**        | **VGG19**               | **DenseNet121**         | **MobileNetV2**          |
|----------------------|--------------------------|--------------------------|--------------------------|---------------------------|----------------------------|
| **Year**             | 2015                     | 2015                     | 2014                     | 2017                      | 2018                       |
| **Top-1 Accuracy**   | ~76%                    | ~78%                    | ~71%                    | ~75%                     | ~72%                      |
| **Parameters**       | ~25.6M                  | ~23.8M                  | ~143M                   | ~8M                      | ~3.4M                     |
| **Model Size**       | Medium                  | Medium                  | Very Large              | Small                    | Very Small                |
| **Speed (Inference)**| Moderate                | Slow                    | Slow                    | Moderate                 | Fast                      |
| **Depth**            | 50 layers               | ~48 layers              | 19 layers               | 121 layers               | ~88 layers                |
| **Architecture Type**| Residual                | Inception Modules       | Plain CNN               | Dense Connectivity       | Depthwise Separable CNN   |
| **Best Use Case**    | General purpose         | Image recognition       | Simple classification    | Memory-efficient tasks   | Mobile/embedded devices   |

---

## 🧠 Architecture Overviews

### 🔸 ResNet50
- **Concept**: Introduces residual (skip) connections to allow gradient flow through deep networks.
- **Pros**: Handles deep networks well, good balance of performance and size.
- **Cons**: More complex than VGG, slower training.

---

### 🔸 InceptionV3
- **Concept**: Parallel convolutions of different sizes capture multi-scale features.
- **Pros**: High accuracy, efficient parameter usage.
- **Cons**: Complicated structure, harder to modify.

---

### 🔸 VGG19
- **Concept**: Stacked 3x3 conv layers with max pooling. Simple and deep.
- **Pros**: Easy to understand and implement.
- **Cons**: Extremely large, slow and resource-heavy.

---

### 🔸 DenseNet121
- **Concept**: Each layer takes input from all previous layers.
- **Pros**: Efficient and fewer parameters, good gradient flow.
- **Cons**: Concatenation increases GPU memory usage.

---

### 🔸 MobileNetV2
- **Concept**: Uses depthwise separable convolutions and inverted residual blocks.
- **Pros**: Very lightweight, fast inference, mobile-ready.
- **Cons**: Slightly lower accuracy, not for very complex tasks.

---

## 🔧 Transfer Learning with ResNet50 in TensorFlow

### ✅ Description

This example demonstrates how to:
1. Load a pre-trained ResNet50 model (without top layers).
2. Add a custom classification head.
3. Train the new head while keeping the base frozen.
4. Optionally unfreeze deeper layers for fine-tuning.
5. Evaluate the model on a test set.
