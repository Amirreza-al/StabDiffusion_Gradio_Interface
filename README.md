# StabDiffusion Gradio Interface

### 🖼️ Stable Diffusion Gradio Interface

A simple yet powerful Gradio web interface for generating images with Stable Diffusion models. This project allows users to easily interact with both SD 1.5 and the high-resolution SDXL models, providing real-time control over key generation parameters.

### ✨ Features

Dual Model Support: Seamlessly switch between Stable Diffusion 1.5 and the more advanced Stable Diffusion XL.
Parameter Control: Interactively adjust settings to fine-tune your creations:
CFG Scale (Guidance Scale): Control how strictly the model follows your prompt.
Image Dimensions: Set custom image width and height.
Intuitive UI: A clean and user-friendly interface built with Gradio.
Notebook Format: Organized into logical cells for imports, model loading, and the UI, making the code easy to understand and modify.

### 📸 Demo

![image](https://github.com/user-attachments/assets/618aa22f-1716-440a-b506-d8d29e61c86e)


## ⚙️ Setup and Installation

Follow these steps to set up the project environment and run the interface.

1. Prerequisites
Python 3.8 or newer.
pip and venv for package management.
An NVIDIA GPU with CUDA support is highly recommended for reasonable generation times. The code will fall back to the CPU, but it will be extremely slow.
2. Create a requirements.txt file
For easy installation of dependencies, create a file named requirements.txt in your project's root directory and add the following lines to it:

```
torch
diffusers
transformers
accelerate
gradio
```
