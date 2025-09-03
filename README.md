# 🧠 MNIST Autoencoder

This project implements a **Convolutional Autoencoder** trained on the MNIST handwritten digits dataset.  
The goal is to learn a compact representation of 28×28 grayscale digits (0–9) and reconstruct them from a low-dimensional latent space.

---

## 📊 Dataset
- **MNIST**: 70,000 images (60k train / 10k test)  
- Each image: **28×28 grayscale**  
- 10 digit classes (0–9)  
- Normalized to values in [0,1]  

---

## Model Architecture
- **Encoder**
  - Conv2D → MaxPooling  
  - Conv2D → MaxPooling  
  - Dense layer → 16-dimensional latent space  
- **Decoder**
  - Dense → Reshape  
  - Conv2DTranspose → upsampling  
  - Conv2D with sigmoid activation (reconstruction)  
- **Loss**: Binary Cross-Entropy (BCE)  
- **Optimizer**: Adam  


