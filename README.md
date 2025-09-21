# Signature-Authentication-System

A **multi-class CNN system** that does more than just detect forgery—it can **identify the signer** of a handwritten signature and classify it as **Genuine** or **Forged**. This project achieved **89% accuracy** on the test dataset and demonstrates the power of deep learning in **signature authentication**.

---

## 🌟 Features

- **Dual Classification:** Predicts both the signer and the authenticity of a signature.
- **Lightweight Repository:** Only notebook, metadata, dataset link, and UI screenshot are included.
- **Reproducible:** Easy to run your own experiments using the provided notebook.
- **Visual Reference:** UI screenshot included for a clear understanding of the interface.
- **Scalable:** Can be extended to larger datasets or integrated into authentication systems.

---

## 📂 Repository Structure

import os

# Base project folder
base_dir = "signature-authentication-system"

# Folder structure
folders = [
    "notebooks",
    "data",
    "images"
]

# Files to create (empty placeholders)
files = {
    "notebooks/Signature_Classification.ipynb": "",
    "data/metadata.csv": "",
    "images/ui_screenshot.png": "",
    "README.md": "",
    "requirements.txt": ""
}

# Create folders
for folder in folders:
    os.makedirs(os.path.join(base_dir, folder), exist_ok=True)

# Create files
for file_path, content in files.items():
    full_path = os.path.join(base_dir, file_path)
    with open(full_path, "w") as f:
        f.write(content)

print(f"Project structure created successfully at '{base_dir}'")


---

## 🧠 About the Project

Signatures are widely used for authentication, but **forgeries are common**. This project solves two problems simultaneously:

1. **Identify the signer** – Multi-class classification using CNN to predict the person who made the signature.
2. **Detect forgery** – Binary classification to determine if the signature is genuine or forged.

**Workflow:**

1. Preprocess the signature images (resize, normalize, grayscale).  
2. Train a **Convolutional Neural Network (CNN)** with dual outputs.  
   - Output 1: Person identification (multi-class).  
   - Output 2: Forgery detection (binary).  
3. Evaluate performance using accuracy metrics for both tasks.  
4. Demonstrate predictions using a sample **UI**.

---

## 📥 Dataset

The dataset contains multiple handwritten signatures per person. Only a **link to the dataset** is provided here to keep the repository lightweight:

[Download Dataset][(https://www.kaggle.com/datasets/matteocarnebella/cedar-signatures)] 

After downloading, place the dataset in your preferred folder and update paths in the notebook.  

**metadata.csv** maps numeric person IDs to actual names, so your predictions are human-readable.

---

## 🚀 Installation

Clone the repository and install the required packages:

```bash
git clone <your-repo-url>
cd signature-authentication-system
pip install -r requirements.txt

