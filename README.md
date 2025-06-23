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

#### 1. Prerequisites
Python 3.8 or newer.
pip and venv for package management.
An NVIDIA GPU with CUDA support is highly recommended for reasonable generation times. The code will fall back to the CPU, but it will be extremely slow.
#### 2. Create a requirements.txt file
For easy installation of dependencies, create a file named requirements.txt in your project's root directory and add the following lines to it:

```
torch
diffusers
transformers
accelerate
gradio
```
#### 3. Installation Steps

Clone the repository and set up the virtual environment.

```
# 1. Clone your GitHub repository
git clone https://github.com/YOUR_USERNAME/YOUR_REPOSITORY_NAME.git

# 2. Navigate to the project directory
cd YOUR_REPOSITORY_NAME

# 3. Create a Python virtual environment
python -m venv venv

# 4. Activate the virtual environment
# On Windows:
.\venv\Scripts\activate
# On macOS/Linux:
source venv/bin/activate

# 5. Install the required libraries from the requirements.txt file
pip install -r requirements.txt
```

### 🚀 How to Run

Since this project is a Jupyter Notebook, you will need to launch it using Jupyter.

1. Start Jupyter Notebook or JupyterLab from your activated virtual environment
   ```
   jupyter notebook
   ```
   or
   ```
   jupyter lab
   ```
2. Open the Notebook: A new tab should open in your browser. Navigate to and open the .ipynb file for this project.

3. Run the Cells: Execute the notebook cells in order from top to bottom.

- Run the imports cell.
- Run the model loading cell.
- Run the UI definition and launch cell.

Important Note: The first time you run the model loading cell, it will download the Stable Diffusion models (several gigabytes each) from the Hugging Face Hub. This may take a significant amount of time depending on your internet connection. On subsequent runs, the models will be loaded from your local cache, which is much faster.

4. Access the Interface: Once you run the final cell containing demo.launch(share=True), the Gradio interface will start. You will see a local URL (e.g., http://127.0.0.1:7860) and a public URL (if share=True is used) printed in the notebook output. Open one of these links in your browser to start using the application.

# usage

Model: ```Select either stable-diffusion-v1-5``` or the higher-quality ```stable-diffusion-xl-base-1.0``` from the dropdown menu.

Prompt: Write a descriptive text of the image you want to create. Be as specific as possible for better results.

CFG Scale: Adjust the slider to control prompt adherence. Lower values (e.g., 3-6) give the model more creative freedom, while 
higher values (e.g., 7-12) make it stick more closely to your prompt.

Image Width/Height: Set the desired dimensions for the output image. Note that SDXL works best with resolutions of 1024x1024.

Generate: Click the "Generate Image" button and wait for the result to appear on the right.

# 🙏 Acknowledgments

- Thanks to Stability AI and RunwayML for releasing the Stable Diffusion models.
- This interface is built using the fantastic Gradio library.
- Model hosting and pipelines are powered by Hugging Face.
