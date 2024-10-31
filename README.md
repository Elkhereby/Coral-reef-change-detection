# Coral-reef-change-detection
Change in coral reef(represented as PVC pipes) health like illness or dying parts by comparing different photos of the coral


# Image Alignment and Mask Detection Project

This project aligns two images using SIFT and FLANN-based matching, then applies HSV masking to detect specific regions of interest. The aligned image comparison helps track growth, death, cure, and infection through dynamic color masks. 

## Features

1. **Image Alignment**: Aligns two images for comparison using SIFT key points and FLANN matching.
2. **HSV Masking**: Adjustable HSV color range to isolate regions based on color in both base and aligned images.
3. **Dynamic Mask Creation**: Generates masks for growth, death, cure, and infection changes between images.
4. **Bounding Boxes**: Draws bounding boxes around significant regions of growth, death, cure, and infection.

## Project Setup

- Install the required packages:
  ```shell
  pip install opencv-python numpy
  ```

- Place your two images (e.g., `OneYearImage.jpg` and `coral1.jpg`) in the same directory as the script.

## How to Run

1. Run the script:
   ```shell
   python image_alignment.py
   ```
2. Adjust the HSV color ranges in the trackbars to set the desired color detection ranges for pink and white colors.
3. Press `q` to exit the program.

## Key Functions

- **align_images(img1, img2)**: Aligns `img1` to `img2` using SIFT and FLANN-based matching.
- **create_mask(image, lower_bound, upper_bound)**: Creates HSV masks with dilation and erosion to reduce noise.
- **draw_contours(mask, image, color, min_area)**: Draws bounding boxes on the specified regions.

## Controls

- Use the HSV trackbars to adjust color ranges.
- Press `q` to quit the application.
