# Artistic Style Transfer: From Photo to Monet using CycleGAN

This project uses a Cycle-Consistent Generative Adversarial Network (CycleGAN) to translate photographs into the artistic style of the French Impressionist painter, Claude Monet. The model is trained on two unpaired image collections: landscape photographs and Monet's paintings.

This repository contains the Jupyter Notebook with the complete implementation, from data preprocessing to model training and evaluation.

**Project Link:** https://github.com/jjzd83/IDL-wk5

## 📖 Overview

The goal is to perform image-to-image translation. We take a standard photograph and apply the artistic style of Monet. Since we don't have paired images (i.e., a photo and its corresponding Monet painting), a CycleGAN is the ideal architecture. It learns the mapping between the two image domains using a cycle-consistency loss, which ensures that an image translated from domain A to B and back to A remains true to the original.

## 🚀 Getting Started

Follow these instructions to get a copy of the project up and running on your local machine.

### Prerequisites

* Python 3.7+
* Jupyter Notebook or JupyterLab

You will also need to install the Python packages listed in the `requirements.txt` file.

### Installation

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/jjzd83/IDL-wk5.git](https://github.com/jjzd83/IDL-wk5.git)
    cd IDL-wk5
    ```

2.  **Create and activate a virtual environment (recommended):**
    ```bash
    python -m venv venv
    # On macOS/Linux:
    source venv/bin/activate
    # On Windows:
    .\venv\Scripts\activate
    ```

3.  **Install the required packages:**
    A `requirements.txt` file is not provided in the repo, but you can create one with the following content:
    ```
    tensorflow
    matplotlib
    numpy
    ```
    Then, run the installation command:
    ```bash
    pip install -r requirements.txt
    ```

## 💻 Usage

1.  **Download the dataset** from the ["I'm something of a painter myself"](https://www.kaggle.com/c/gan-getting-started) Kaggle competition. You will need the `monet_tfrec` and `photo_tfrec` directories containing the TFRecord files.

2.  **Place the dataset** into the project directory. Ensure the notebook paths align with where you've stored the data.

3.  **Launch Jupyter:**
    ```bash
    jupyter notebook
    ```

4.  Open `style-transfer-monet.ipynb` and run the cells sequentially to preprocess the data, build the model, and start the training process.
