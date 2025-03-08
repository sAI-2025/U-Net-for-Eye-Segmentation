# U-Net for Eye Segmentation

## Project Description
This project presents an improved eye segmentation model using **U-Net**, achieving **89.6% Intersection over Union (IoU)** and **87.4% Dice Coefficient**. The model performance was enhanced by experimenting with customized loss functions, including **Dice Loss, Binary Cross-Entropy (BCE), Hybrid Loss, and K-Loss**.

## Project Structure
```
.
├── Unet_Eye.ipynb            # Jupyter Notebook with model implementation
├── Results                   # Folder containing model results, predictions, and metrics
├── Dataset                   # Dataset structure
│   ├── nil_files/            # Input data (X)
│   └── labels/               # Corresponding masks (Y)
```

## Dataset Information
The dataset consists of labeled eye images where each pixel belongs to specific anatomical structures, such as:
- **Iris**
- **Pupil**
- **Sclera**

The data is in **NIfTI (.nii)** format, commonly used in medical imaging applications. The segmentation masks provide pixel-wise annotations for training the model.

## Implementation Steps
### 1. Install Required Dependencies
Ensure you have Python **3.10** installed. First, check if `pip` is installed:
```bash
pip --version
```
If not installed, upgrade it:
```bash
python3.10 -m pip install --upgrade pip
```
Next, install all required dependencies using:
```bash
pip install -r requirements.txt
```

### 2. Setting Up the Dataset
Organize the dataset as mentioned in the **Project Structure**. If the dataset is unavailable, the script will automatically download it.

### 3. Running the Model
Execute the Jupyter Notebook:
```bash
jupyter notebook
```
Open **Unet_Eye.ipynb** and run all the cells to train and evaluate the model.

---

## U-Net Architecture
The **U-Net** architecture was a groundbreaking discovery in medical image segmentation, focusing on accurately detecting objects and boundaries within an image.

### Key Components of U-Net:
- **Contracting Path:**
  - Uses convolution and pooling layers to extract relevant image features while reducing spatial dimensions.
- **Expanding Path:**
  - Uses convolution and up-convolution (transposed convolution) to upsample feature maps and generate a precise segmentation map.
- **Skip Connections:**
  - Directly link the contracting path to the expanding path, preserving fine-grained spatial information.

### Advantages of U-Net:
- **High Accuracy:**
  - Achieves state-of-the-art segmentation results in biomedical imaging tasks.
- **Fully Convolutional Architecture:**
  - No dense layers, making it efficient in handling images of varying sizes.
- **Effective for Small Datasets:**
  - Data augmentation and skip connections enable training with limited labeled data.

---

## Loss Functions Used
To optimize segmentation performance, various loss functions were explored:

1. **Dice Loss:** Measures the overlap between predicted and ground truth masks.
2. **Binary Cross-Entropy (BCE):** Standard loss for binary segmentation problems.
3. **Hybrid Loss (Dice + BCE):** Combines the benefits of both loss functions.
4. **K-Loss:** A custom loss function designed for improved segmentation accuracy.

These loss functions were evaluated to determine the most effective optimization strategy for eye segmentation.

---

## Conclusion
The U-Net model provides an accurate and efficient approach for medical image segmentation. Its ability to preserve fine details through skip connections makes it ideal for segmenting complex structures such as the eye.

---

### Author
**Sai Krishna Chowdary Chundru**

For further queries, feel free to contact:
- **Email:** cchsaikrishnachowdary@gmail.com
- **LinkedIn:** [linkedin.com/in/sai-krishna-chowdary-chundru](https://linkedin.com/in/sai-krishna-chowdary-chundru)
- **GitHub:** [github.com/sAI-2025](https://github.com/sAI-2025)

