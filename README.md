# Scratch GPT: Decoder-only Transformer

This project demonstrates the implementation of a GPT-like language model from scratch, based on the tutorial series "Let's build GPT: from scratch, in code, spelled out" by Andrej Karpathy. The repository contains a few key files that illustrate different stages of model development, focusing on the decoder-only transformer architecture.

## Project Goal
The main goal of this project is to create a language model (LLM) that generates text in the style of William Shakespeare. The code evolves from a basic bigram model to a GPT-like architecture, utilizing transformer mechanisms.

## Repository Structure
The repository contains the following files:

### 1. `bigram.py`
- **Purpose**: Introduces the basic idea of a bigram model, used as a foundation for implementing language models.
- **Key Features**: Demonstrates how language model algorithms can be implemented at a basic level using bigrams.
- **Usage**: This script can be run on any device, and it provides an understanding of how to build simple language models.

### 2. `v2.py`
- **Purpose**: Adds attention mechanisms to the bigram model and introduces inter-token communication, enhancing the model's ability to understand context.
- **Key Features**:
  - Decoder-only transformer (no encoder).
  - Simple 1-1 tokenization is used for encoding the input.
  - Tracks validation loss during training.
- **Training Details**: 
  - Trained for 5000 iterations on a MacBook Pro M1.
  - Validation loss converged from 4.4 to 1.8, making it a good example of how the validation loss behaves during training.
  - Can be run on most devices.
- **Usage**: Run this script to observe the loss convergence and see the improved language model over the basic bigram model.

### 3. `gpt2.py`
- **Purpose**: Full implementation of GPT-2 with larger model size, training parameters, and more complex hyperparameter tuning.
- **Key Features**:
  - Higher number of parameters.
  - Requires a high-end GPU for training due to the size of the model.
- **Usage**: This script implements a more advanced version of the model, designed for those who have access to more powerful hardware and want to train on larger datasets.

### 4. `input.txt`
- **Purpose**: A 1MB text file containing works by William Shakespeare, used as training data for the models.
- **Usage**: This file serves as the training corpus for all models in the repository. The goal is to generate text that mimics Shakespeare's writing style.

## How to Run

1. **Basic Bigram Model (`bigram.py`)**:
   - Run this script on any device to explore how a basic bigram model works for language modeling.

2. **Transformer with Attention (`v2.py`)**:
   - This script introduces the transformer architecture. You can run this on a MacBook Pro M1 or any comparable device to see how attention improves the model's ability to handle longer contexts.
   - Training will take about 5000 iterations, and you can track how the validation loss converges.

3. **Full GPT-2 Implementation (`gpt2.py`)**:
   - Requires a high-end GPU to train. This model is a full-fledged GPT-2 and is designed for large-scale language modeling tasks.

## Results
- `v2.py` demonstrates a significant improvement in validation loss after training for 5000 iterations. The loss drops from 4.4 to 1.8, making it a suitable example of how transformers improve over simple bigram models.
<img width="724" alt="Screenshot 2024-09-06 at 5 58 56 PM" src="https://github.com/user-attachments/assets/4aae7f46-806e-49a8-bb56-c6bd65ab1100">

  
- The `gpt2.py` model is designed for more extensive experimentation with GPT-like architectures and will require considerable hardware resources to train effectively.

## Conclusion
This project provides a hands-on approach to building language models from scratch, starting from simple bigram models to a more sophisticated GPT-2 implementation. By working through these files, you'll understand the core concepts behind large language models and transformers.

### Acknowledgment
This project was inspired by Andrej Karpathy's "Let's build GPT: from scratch, in code, spelled out" video.
