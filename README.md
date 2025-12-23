
# Malaria Cell Image Classification with R and Keras

![R](https://img.shields.io/badge/Language-R-blue.svg)
![TensorFlow](https://img.shields.io/badge/Backend-TensorFlow-orange.svg)
![Keras](https://img.shields.io/badge/API-Keras-red.svg)

This repository contains an R-based deep learning project that utilizes a Convolutional Neural Network (CNN) to detect malaria parasites in cell images.

## 📌 Project Overview
The goal of this project is to automate the detection of malaria in blood smear images. Using the `keras` and `tensorflow` libraries in R, we build, train, and evaluate a sequential CNN model.

## 📂 Dataset Structure
The model expects a directory structure as follows:
- `Malaria Cells/training_set/`: Contains labeled images for training.
- `Malaria Cells/testing_set/`: Contains labeled images for validation/testing.

## 🛠 Model Architecture
The CNN is built using the following layers:
- **Convolutional Layers**: 3 layers with varying filters (6 and 12) and kernel sizes.
- **Max Pooling**: Reduces spatial dimensions after each convolution.
- **Flatten & Dense**: Converts feature maps to a single vector followed by a Sigmoid activation for binary classification (Parasitized vs. Uninfected).
- **Dropout**: Included to prevent overfitting.

## 🚀 How to Run

### Prerequisites
Ensure you have [R](https://www.r-project.org/) and [RStudio](https://posit.co/download/rstudio-desktop/) installed. You will also need to have a Python environment available (managed automatically by `reticulate` usually).

### Installation
Open R or RStudio and install the necessary packages:
```r
install.packages(c("keras", "tensorflow", "magick", "imager", "purrr", "dplyr"))
library(keras)
install_keras()
Execution
Clone this repository:

Bash

git clone [https://github.com/your-username/your-repo-name.git](https://github.com/your-username/your-repo-name.git)
Place your dataset in the relative path defined in the script (../input/files1/).

Run the notebook notebook-r-my-pred-11.ipynb or execute the R script.

📊 Results
The model tracks accuracy and loss over 5 epochs. You can visualize the training history using:

R

plot(history)
📝 License
This project is open-source and available under the MIT License.


---

### 2. How to Run on GitHub (Technical Details)
Since you are using a `.ipynb` file (Jupyter Notebook) for R, here are the three main ways to run it:

#### Option A: Local Execution (Recommended)
1. **Install R Kernel for Jupyter**: If you want to run the `.ipynb` file locally, install the `IRkernel`:
   ```r
   install.packages('IRkernel')
   IRkernel::installspec(user = FALSE)
Open with Jupyter: Run jupyter notebook in your terminal and open your file.

Option B: Google Colab
Upload your .ipynb file to Google Colab.

Change the Runtime type to R (Runtime > Change runtime type > R).

Note: You will need to upload your dataset to the Colab environment or link your Google Drive.

Option C: GitHub Codespaces
Click the Code button on your GitHub repo and select Create codespace on main.

Install the R extension in VS Code within the codespace.

Install the system dependencies (like libmagick++-dev for the magick package) via the terminal:

Bash

sudo apt-get update
sudo apt-get install libmagick++-dev
3. Summary of Libraries Used
Based on your notebook, ensure these are available in your environment:

keras & tensorflow: Deep learning backend.

magick & imager: Image processing and manipulation.

purrr, dplyr: Functional programming and data manipulation.
