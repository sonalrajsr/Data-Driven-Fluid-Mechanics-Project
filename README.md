# Data-Driven Fluid Mechanics Project

This repository hosts a Python project that utilizes image processing and Proper Orthogonal Decomposition (POD) to analyze fluid dynamics from video data. This project covers steps for extracting frames, adding noise, applying noise reduction techniques, and analyzing fluid flow using POD.

## Project Overview

The aim of this project is to extract meaningful insights from video frames capturing fluid dynamics experiments. Our objectives are:
- **Extracting frames** from video data.
- **Simulating varying experimental conditions** by applying Gaussian and Speckle noise.
- **Implementing noise reduction** techniques including Gaussian blur and Non-Local Means (NLM) denoising.
- **Analyzing fluid flow** using Proper Orthogonal Decomposition (POD) to identify dominant flow modes.

## Installation and Setup

### Prerequisites
Ensure you have Python 3.x installed along with the following Python libraries:
- OpenCV
- NumPy
- Matplotlib
- Scikit-learn

### Installation Instructions
Clone the repository to your local machine:
```bash
git clone https://github.com/yourgithubusername/Data-Driven-Fluid-Mechanics-Project.git
```
## Dataset
Access the dataset used in this project via the following link:
```bash
https://drive.google.com/file/d/1WiSbCQmxu9ugEideLkcdAof1GA0uYXXT/view
```

## Directory Structure
- frames/: Contains extracted frames from the original video.
- noise_x/: Directories such as noise_20, noise_40, etc., containing frames with added noise.
- denoised_images_x/: Contains frames after applying denoising techniques.
## Results

This section presents the outcomes of the implemented noise addition, noise reduction techniques, and POD analysis on the fluid dynamics images. Below are summaries and visualizations demonstrating the effectiveness of different methods in handling and analyzing noisy images.

### Noise Addition Effects

We added Gaussian and Speckle noise to clean images from fluid dynamics experiments to simulate varying conditions. Below are examples showing the effects of different noise levels:

- **Gaussian Noise**: Images with 20%, 40%, 60%, and 80% Gaussian noise show progressively more obscured details and increased visual distortion.
- **Speckle Noise**: Similarly, Speckle noise at these levels introduced a grainy appearance, making finer details harder to discern.

### Noise Reduction Techniques

We applied Gaussian Blur and Non-Local Means (NLM) denoising techniques to noisy images. The results show significant improvements:

- **Gaussian Blur**: Effective at reducing high-frequency noise but tends to blur edges, losing some important image details.
- **Non-Local Means Denoising**: Superior in preserving edges and fine details while effectively reducing noise.

### POD Analysis

Proper Orthogonal Decomposition (POD) was performed to identify dominant flow modes in the original, noisy, and denoised images. The analysis revealed:

- **Impact of Noise**: Noise significantly affects the accuracy of flow mode identification, introducing errors and inconsistencies in the lower energy modes.
- **Recovery with Denoising**: Post-denoising, the flow modes closely resembled those obtained from clean images, demonstrating the efficacy of our noise reduction approaches.
