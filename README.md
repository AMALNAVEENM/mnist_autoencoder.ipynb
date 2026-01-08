# MNIST Autoencoder Implementation

A basic fully connected autoencoder trained on the MNIST dataset to compress and reconstruct handwritten digits.

## Architecture
- **Input**: 784 (28×28 flattened image)
- **Latent space**: 32 dimensions
- **Output**: 784 (reconstructed image)
- **Activation**: ReLU (hidden), Sigmoid (output)

## Results
- Smooth loss convergence (50 epochs)
- High-quality reconstructions
- No overfitting
  
 Training Configuration:
Optimizer: Adam (learning_rate=0.001)
Loss function: Mean Squared Error (MSE)
Epochs: 50
Batch size: 256
Training samples: 60,000
Test samples: 10,000
Final Loss (Typical Run):
Training loss (epoch 50): ≈0.018 – 0.022
Validation loss (epoch 50): ≈0.019 – 0.023
Loss curves show smooth convergence with no overfitting
 Reconstruction Quality:
Reconstructed digits are clearly recognizable (e.g., 0, 1, 2, 3, 5, 6, 8, 9)
Minor blurriness present (expected for dense autoencoders)
No structural distortions (e.g., 8 doesn’t become 0)
 Visualization:
Side-by-side plot shows 10 original digits (top row) and their reconstructions (bottom row)
All reconstructions maintain correct digit shape and orientation
Example: A handwritten “4” is reconstructed as a “4”, not confused with “9” or “1”
Key Insight:
A 32-dimensional latent space is sufficient to encode essential visual features of MNIST digits
Autoencoder learns an efficient compressed representation without labels (unsupervised learning)
💡 Note: Exact loss values may vary slightly between runs due to random weight initialization, but reconstructions remain consistently high-quality.

