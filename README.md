
# Data-Driven-Fluid-Mechanics-Project
This repository hosts a Python project that utilizes image processing and Proper Orthogonal Decomposition (POD) to analyze fluid dynamics from video data. The project includes steps for noise addition, noise reduction, and flow analysis through computational methods in image processing and machine learning.

## Project Overview

The aim of this project is to extract meaningful insights from video frames capturing fluid dynamics experiments. The specific goals include:
- Extracting frames from video data.
- Applying Gaussian and Speckle noise to simulate varying experimental conditions.
- Implementing noise reduction techniques such as Gaussian blur and Non-Local Means (NLM) denoising.
- Analyzing the fluid flow using Proper Orthogonal Decomposition (POD) to identify dominant flow modes.
## POD Analysis Overview
Proper Orthogonal Decomposition (POD) is a strong mathematical technique used in fluid dynamics to derive dominating modes of flow from large datasets. This method minimizes data dimensionality by dividing the flow field into orthogonal modes depending on energy levels. POD is critical for recognizing major flow patterns, making it easier to analyze turbulent or complex fluid processes. In this project, we use POD to investigate the effects of noise and denoising techniques on fluid dynamics, allowing for a better understanding of underlying flow structures and assisting in the construction of efficient simulation models.
## Types of noise used
- Gaussian Noise
- Speckle Noise

## Summery Of This Project
This research entails utilising Proper Orthogonal Decomposition (POD) through Singular Value Decomposition (SVD) to examine fluid dynamics data, with a specific emphasis on the analysis of fluid flow across time as depicted in a sequence of photographs. The objective is to decrease the dimensionality of the data while retaining the most important characteristics of the flow, which are crucial for comprehending the fundamental dynamics of the system.

The procedure commences by gathering flow field photographs, each of which captures a moment in time. Subsequently, these images are transformed into a matrix structure, wherein each image is compressed into a vector and combined into a matrix representing a snapshot. This matrix efficiently combines all the geographical and temporal information into a unified mathematical framework.

The SVD method decomposes the snapshot matrix into three matrices: U, Σ, and Vᵀ. In this context, U denotes the spatial modes, Σ corresponds to the strength or energy of each mode, and Vᵀ represents the temporal coefficients. This decomposition enables us to prioritise the modes based on their energy content, which is crucial for determining the most impactful modes in the flow.

The results obtained from the Proper Orthogonal Decomposition (POD) using Singular Value Decomposition (SVD) offer valuable insights into the primary patterns and structures present in the flow field. These results effectively highlight important features such as vortices or waves that have a substantial impact on the behaviour of the fluid. This study not only enhances the comprehension of fluid dynamics but also enhances computing efficiency and provides valuable insights for future research and development in fluid mechanics.
## Results

This section presents the outcomes of the implemented noise addition, noise reduction techniques, and POD analysis on the fluid dynamics images. Below are summaries and visualizations demonstrating the effectiveness of different methods in handling and analyzing noisy images.

### Noise Addition Effects

We added Gaussian and Speckle noise to clean images from fluid dynamics experiments to simulate varying conditions. Below are examples showing the effects of different noise levels:

- **Gaussian Noise**: Images with 20%, 40%, 60%, and 80% Gaussian noise show progressively more obscured details and increased visual distortion.
- **Speckle Noise**: Similarly, Speckle noise at these levels introduced a grainy appearance, making finer details harder to discern.

![Noise Addition Comparison]

### Noise Reduction Techniques

We applied Gaussian Blur and Non-Local Means (NLM) denoising techniques to noisy images. The results show significant improvements:

- **Gaussian Blur**: Effective at reducing high-frequency noise but tends to blur edges, losing some important image details.
- **Non-Local Means Denoising**: Superior in preserving edges and fine details while effectively reducing noise.

Here are side-by-side comparisons illustrating the before and after effects of the denoising techniques on an image with 60% Gaussian noise:

![Denoising Comparison]

### POD Analysis

Proper Orthogonal Decomposition (POD) was performed to identify dominant flow modes in the original, noisy, and denoised images. The analysis revealed:

- **Impact of Noise**: Noise significantly affects the accuracy of flow mode identification, introducing errors and inconsistencies in the lower energy modes.
- **Recovery with Denoising**: Post-denoising, the flow modes closely resembled those obtained from clean images, demonstrating the efficacy of our noise reduction approaches.

![POD Analysis Results](/path/to/pod_analysis_results_image.jpg)

## Conclusion

The experiments and analyses confirm that while noise addition can significantly degrade image quality and analysis accuracy, the application of sophisticated denoising techniques and robust analysis methods like POD can effectively mitigate these effects. Future work may explore more advanced denoising algorithms and their impact on automated image analysis tasks in fluid dynamics and other fields.


## Installation and Setup

### Prerequisites
- Python 3.x
- Libraries: OpenCV, NumPy, Matplotlib, and Scikit-learn



## Installation

Clone this repository to your local machine using:

```bash
git clone https://github.com/sonalrajsr/Data-Driven-Fluid-Mechanics-Project.git
```
Find dataset for this Project
```bash
https://drive.google.com/file/d/1WiSbCQmxu9ugEideLkcdAof1GA0uYXXT/view?usp=sharing
```
## Directory Structure
- frames/: Contains extracted frames from the original video.
- noise_x/: Directories such as noise_20, noise_40, etc., containing frames with added noise.
- denoised_images_x/: Contains frames after applying denoising techniques.
