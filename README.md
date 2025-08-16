# ☁️ Cloud Motion Estimation using FlownetS
Optical flow or optic flow is the pattern of apparent motion of objects, surfaces, and edges in a visual scene caused by the relative motion between an observer and a scene.
This project implements **FlowNet**, a convolutional neural network for estimating optical flow, specifically applied to **cloud motion estimation** from satellite or weather images. The model helps analyze and visualize cloud movement over time.

---

## 📁 File Structure

```
├── flo2img.py          # Convert .flo optical flow files to images
├── flownet_test.py     # Test the FlowNet model on sample image pairs
├── flownet_train.py    # Train the FlowNet model using a dataset
└── README.md           # Project documentation
```

## 🔧 Training Details

- **Optimizer**: Adam  
- **Activation Function**: LeakyReLU  
- **Adam Parameters**:  
  - β₁ = 0.9  
  - β₂ = 0.999  
- **Mini-Batch Size**: 8 image pairs  
- **Learning Rate (λ)**: 1e-4  
- **Learning Rate Schedule**:  
  - λ is halved every 100k iterations after the first 300k iterations  
- **Total Epochs**: 300  
- **Epoch Size**: 1000 samples per epoch  


## My youtube explanation video of the project: https://www.youtube.com/watch?v=ObQx9PNnGt8

<img width="1873" height="1038" alt="image" src="https://github.com/user-attachments/assets/db121473-b056-4acf-8631-bc71499b807b" />

## Acknowedgement
The code is built on top of https://github.com/ClementPinard/FlowNetPytorch repo.
