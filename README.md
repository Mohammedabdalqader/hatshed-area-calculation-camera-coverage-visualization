# Hatched Area Calculation and Camera Coverage Visualization

## Project Overview

This project focuses on calculating of hatched areas and visualizing camera coverage on a given floor plan using image processing techniques. The project is divided into two main parts:

1. **Hatched Area Calculation**: Identifies and calculates the area of hatched regions within an architectural layout using traditional image processing techniques like masking, thresholding, and morphological operations.
   
2. **Camera Coverage Visualization**: Determines and visualizes the coverage areas of security cameras based on their specifications and positions. It uses edge detection to account for obstacles and renders the effective coverage areas of each camera.

**Note**: There are numerous deep learning approaches that can achieve more accurate results compared
to the traditional image processing methods demonstrated in this report for both hatched
area detection and camera coverage visualization. Notable models include YOLOv8, Mask RCNN.
There are also Models known as vision large language models such as Phi-3.5-Vision and
MiniCPM-Llama3-V-2_5. These models can be Fine-tuned using new techniques like Low Rank
Adapter (LoRA) or more advanced methods like QLoRA to optimize their performance for these specific task.


## Prerequisites

To run the code, you need the following libraries:

- Python 3.8 or later
- Jupyter Notebook
- Required Python libraries:
  - `numpy`
  - `opencv-python`
  - `matplotlib`

## Installation

1. **Clone the Repository**:
    ```bash
    git clone https://github.com/Mohammedabdalqader/hatched-area-calculation-camera-coverage-visualization.git
    cd hatched-area-calculation-camera-coverage-visualization
    ```

2. **Install Python Dependencies**:
    ```bash
    pip install -r requirements.txt
    ```

Repository Structure

    hatched_area_calculation.ipynb: The main Jupyter notebook containing code for hatched area calculation and camera coverage visualization.
    camera_coverage_images/: Directory containing sample images used for processing and visualization.
    area_calculation_image_processing/: Directory containing sample images of image pre-processing during hatched area calculation.
    assignment_report: A full ducometation of the solution of the tasks ( A PDF version of the Notebook)


<h3>Image processing duraing Hatched Area Calculation</h3>

<h5> Segment the image into two regions: foreground (hatch areas) and background.</h5>

<p align="center">
  <img src="area_calculation_image_processing/thresholded_image.jpg" alt="Step 1" width="600"/>
</p>

<h5> Applying Gaussian Blur to Reduce Noise and using canny edge detector to detect the edges of the hatched regions. </h5>

<p align="center">
  <img src="area_calculation_image_processing/dilated_edges.jpg" alt="Step 1" width="600"/>
</p>

<h5> Filling Hatched Regions Using Morphological Closing + Identifying and Filtering Connected Components. </h5>

<p align="center">
  <img src="area_calculation_image_processing/closed.jpg" alt="Step 1" width="600"/>
</p>

<h5> Removing Small White Regions (Noise) Using Morphological Opening. </h5>

<p align="center">
  <img src="area_calculation_image_processing/cleaned_image.jpg" alt="Step 1" width="600"/>
</p>

<h5> Estimated Hatched Area (in m2 - Real World) :  ~ 481.5 m2 </h5>


<h3>Overlay (All Cameras)</h3>
<p align="center">
  <img src="overlay.jpg" alt="overlay" width="600"/>
</p>

<h3>Camera Coverage Area (All Cameras)</h3>
<p align="center">
  <img src="all-cameras.jpg" alt="" width="600"/>
</p>

<p align="center">
  <img src="camera_coverage_images/camera1.jpg" alt="Camera 1" width="200"/>
  <img src="camera_coverage_images/camera2.jpg" alt="Camera 2" width="200"/>
  <img src="camera_coverage_images/camera3.jpg" alt="Camera 3" width="200"/>
</p>

<p align="center">
  <img src="camera_coverage_images/camera4.jpg" alt="Camera 4" width="200"/>
  <img src="camera_coverage_images/camera5.jpg" alt="Camera 5" width="200"/>
  <img src="camera_coverage_images/camera6.jpg" alt="Camera 6" width="200"/>
</p>

<p align="center">
  <img src="camera_coverage_images/camera7.jpg" alt="Camera 7" width="200"/>
  <img src="camera_coverage_images/camera8.jpg" alt="Camera 8" width="200"/>
  <img src="camera_coverage_images/camera9.jpg" alt="Camera 9" width="200"/>
</p>

<p align="center">
  <img src="camera_coverage_images/camera10.jpg" alt="Camera 10" width="200"/>
  <img src="camera_coverage_images/camera11.jpg" alt="Camera 11" width="200"/>
  <img src="camera_coverage_images/camera12.jpg" alt="Camera 12" width="200"/>
</p>

<p align="center">
  <img src="camera_coverage_images/camera13.jpg" alt="Camera 13" width="200"/>
  <img src="camera_coverage_images/camera14.jpg" alt="Camera 14" width="200"/>
  <img src="camera_coverage_images/camera15.jpg" alt="Camera 15" width="200"/>
</p>

<p align="center">
  <img src="camera_coverage_images/camera16.jpg" alt="Camera 16" width="200"/>
  <img src="camera_coverage_images/camera17.jpg" alt="Camera 17" width="200"/>
  <img src="camera_coverage_images/camera18.jpg" alt="Camera 18" width="200"/>
</p>

