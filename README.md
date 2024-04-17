# Signature Similarity Detection using ResNet101

This Python script utilizes the ResNet101 architecture for signature similarity detection. Given two binary images of signatures, it computes their feature vectors using the ResNet101 model and measures the cosine similarity between them to determine whether they match or not based on a given threshold.

## Dependencies

- Python 3.10.12
- numpy
- cv2 (OpenCV)
- tensorflow
- scipy

## Installation

1. Install Python 3.10.12 from the official [Python website](https://www.python.org/downloads/).
2. Install dependencies using pip:

```bash
pip install numpy==1.25.2 opencv-python==4.8.0 tensorflow==2.15.0 scipy==1.11.4
```

## Usage
- Ensure that you have two images of signatures (example m1.jpg and m2.jpg) in the specified paths.
- Set the desired threshold for similarity comparison (threshold variable).
- Run the script:

```bash
python signature_similarity.py
```

## Functionality
- The script first imports necessary libraries including numpy, cv2 (OpenCV), tensorflow, and scipy.
- It configures TensorFlow to utilize GPU memory growth if available.
- The ResNet101 model pretrained on ImageNet is loaded using tensorflow.keras.applications.ResNet101.
- A custom model is created to extract features from the average pooling layer ('avg_pool') of the ResNet101 model.
- Two utility functions preprocess_image and cosine_similarity are defined for image preprocessing and cosine similarity calculation, respectively.
- The findSignatureSimilarity function takes two binary image paths and a threshold as input, preprocesses the images, computes their feature vectors, calculates the cosine similarity, and determines if the signatures match based on the threshold.
- Finally, the script compares two signature images (m1.jpg and m2.jpg) and prints whether they match or not based on the set threshold.

## Contributing
Contributions are welcome! If you have any suggestions or improvements, feel free to open an issue or create a pull request.
