# CIFAR-10 Image Classification with Advanced CNN

A deep learning project implementing an advanced Convolutional Neural Network to classify images from the CIFAR-10 dataset using TensorFlow/Keras.

## Results
- **Test Accuracy: 90.46%** on official CIFAR-10 test set
- **Architecture:** Deep CNN with Batch Normalization, Dropout, and Data Augmentation
- **Parameters:** ~108M trainable parameters

## Model Architecture
- **3 Convolutional Blocks:** 128 → 256 → 512 filters
- **Regularization:** Batch Norm, Dropout (0.2), L2 Weight Decay (1e-6)
- **Data Augmentation:** Random Flip, Translation, Zoom, Contrast, Brightness
- **Classifier:** 8192 → 4096 → 10 (Dense layers with Dropout)

## Training Details
- **Optimizer:** SGD with Momentum (0.9), initial LR 0.01
- **Callbacks:** 
  - ReduceLROnPlateau (patience=10)
  - EarlyStopping (patience=20)
  - ModelCheckpoint (saves best weights)
- **Epochs:** 100 (early stopped around epoch 70+)

## Files
- `code/convnet-cifar-10.ipynb` - Complete training pipeline and inference  
- `submission/submission.csv` - Model predictions (90.46% accuracy results)
- `submission.csv` - Kaggle submission format

## How to Run
1. Open `code/convnet-cifar-10.ipynb` in Jupyter/Colab/Kaggle
2. Run all cells sequentially
3. For Kaggle competitions, the notebook generates `submission.csv`

## Dependencies
See `requirements.txt` for package versions.
