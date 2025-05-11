<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
   
</head>
<body>
    <div class="container">
        <h1>VEGAN: A Vision-language and Edge-enhanced GAN-based Microscopic Medical Image Segmentation Model</h1>
        <p>
            This is the official GitHub repository corresponding to the research paper entitled <strong>VEGAN: A Vision-language and Edge-enhanced
            GAN-based Microscopic Medical Image Segmentation Model</strong>. The research work has been accepted at the <b> <em>2025 Mediterranean Conference on Embedded Computing (MECO)</em></b>.
        </p>
        <div class="attachment">
            <strong>Attachment:</strong> The attachment below shows the detailed architecture of the proposed methodology.
        </div>
    </div>
</body>
</html>


![Image](https://github.com/user-attachments/assets/1d696da8-79d8-47ad-a05c-7ed51b36bbdf)
# Model Architecture

### 1. Base Model: Attention U-Net

Standard Attention U-Net without any additional inputs.

Only the raw image is used as input.

### 2. Base Model + Edge Map

Attention U-Net with an additional edge map as an input.

The edge map could be a combination of Sobel, Canny, and Laplacian filters, as you've previously considered.

### 3. Base Model + Edge Map + VLM Extracted Feature Maps

Attention U-Net with both edge maps and vision-language model (VLM) extracted features as inputs.

The VLM features can be extracted using a model like BLIP, providing context-aware features to enhance segmentation.

### 4. Proposed Model (Base Model + Edge Map + CBAM + VLM Extracted Feature Maps)

The complete pipeline with the Attention U-Net, edge map, CBAM (Convolutional Block Attention Module), and VLM extracted features.

CBAM will add channel and spatial attention, potentially improving the model's ability to focus on relevant regions.

# Results
| **Model** | **MoNuSeg Dice** | **MoNuSeg IoU** | **CNS Dice** | **CNS IoU** |
|-----------|------------------|-----------------|--------------|-------------|
| **1**     | 72.92            | 57.65           | 99.46        | 98.92       |
| **2**     | 73.56            | 58.30           | 99.46        | 98.93       |
| **3**     | 77.51            | 63.32           | 99.52        | 99.04       |
| **4**     | **79.24**        | **65.68**       | **99.56**    | **99.12**   |


