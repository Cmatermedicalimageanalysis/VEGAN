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
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Model Comparison</title>
    <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="bg-gray-100 min-h-screen flex items-center justify-center p-6">
    <div class="bg-white rounded-2xl shadow-xl w-full max-w-4xl p-8 space-y-6">
        <h1 class="text-3xl font-bold text-center text-gray-800">Model Comparison</h1>

        <div class="space-y-4">
            <div class="bg-blue-50 p-6 rounded-xl border border-blue-200">
                <h2 class="text-2xl font-semibold text-blue-700">1) Base Model: Attention U-Net</h2>
                <p class="text-gray-700 mt-2">Standard Attention U-Net without any additional inputs. Only the raw image is used as input.</p>
            </div>

            <div class="bg-green-50 p-6 rounded-xl border border-green-200">
                <h2 class="text-2xl font-semibold text-green-700">2) Base Model + Edge Map</h2>
                <p class="text-gray-700 mt-2">Attention U-Net with an additional edge map as input. The edge map could be a combination of Sobel, Canny, and Laplacian filters.</p>
            </div>

            <div class="bg-yellow-50 p-6 rounded-xl border border-yellow-200">
                <h2 class="text-2xl font-semibold text-yellow-700">3) Base Model + Edge Map + VLM Extracted Feature Maps</h2>
                <p class="text-gray-700 mt-2">Attention U-Net with both edge maps and vision-language model (VLM) extracted features as inputs, providing context-aware features for enhanced segmentation.</p>
            </div>

            <div class="bg-red-50 p-6 rounded-xl border border-red-200">
                <h2 class="text-2xl font-semibold text-red-700">4) Proposed Model</h2>
                <p class="text-gray-700 mt-2">Base Model + Edge Map + CBAM Attention + VLM Extracted Feature Maps. Combines spatial, channel, and context-based attention for improved focus on relevant regions.</p>
            </div>
        </div>
    </div>
</body>
</html>

![Image](https://github.com/user-attachments/assets/1d696da8-79d8-47ad-a05c-7ed51b36bbdf)
