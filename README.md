# My Research and Implementation of QViTs based on Research Papers written

This project is focused on exploring how quantum computing concepts can be combined with transformer-based image models.
Right now, the goal is not to build a perfect production-ready model, but to experiment with different hybrid quantum-classical architectures and understand how they compare with traditional deep learning approaches.

The project currently includes three different model setups:
- A standard CNN baseline model
- A QSANN hybrid model with a classical feature extractor and a quantum layer
- A Quantum Vision Transformer (QViT) inspired model using patch embeddings and a quantum classification layer

Here,
- The CNN model acts as the baseline for accuracy, speed, and training stability.
- The QSANN model combines convolutional feature extraction with a small quantum circuit layer. The idea here is to reduce high-dimensional image features into a smaller quantum representation before classification.
- The QViT model is inspired by Vision Transformers. Instead of processing the entire image at once, the image is divided into patches, embedded into tokens, reduced into quantum inputs, and passed through a variational quantum layer before classification.
All three models are trained and evaluated using the same dataset, training setup, and evaluation metrics so that comparisons stay fair.

The project tracks:
Accuracy, Precision, Recall, F1-score, Inference time, GPU memory usage, Confusion matrices, Training and validation curves
One of the major challenges in this project was handling batch processing inside the quantum layer. Quantum layers do not naturally behave the same way as regular PyTorch layers, especially when working with larger batch sizes and GPU tensors. This project includes fixes for handling batch-wise quantum inference and CPU/GPU compatibility. This is still an active research project and is currently being improved further.

Future work includes:
- Testing on larger datasets beyond MNIST
- Improving the QViT architecture
- Experimenting with deeper quantum layers
- Comparing more hybrid transformer variants
- Exploring better patch embedding methods
- Reducing inference latency
- Writing a research paper based on the results

I am currently working on it and i pushed it to github as basic implementation for Quantum Machine Learning
