# Depth Mapping from Video using Depth-Anything V2 Small Model

This repository contains a project to perform depth estimation on each frame of a video using the `depth-anything/Depth-Anything-V2-Small-hf` model from Hugging Face's Transformers library. It demonstrates how to extract frames from a video, apply depth estimation, visualize an example depth map, and save the resulting depth maps as a video.

***

## Project Description

The goal of this project is to create depth maps from a given video file, showcasing the depth information present in the scene over time. It uses computer vision libraries and a pre-trained depth estimation model to process video frames and generate corresponding depth visualizations.

***

## Features

- Extract RGB frames from input video.
- Perform depth estimation on each frame using the transformer-based `depth-anything/Depth-Anything-V2-Small-hf` model.
- Normalize and visualize depth maps.
- Save the depth maps as a new grayscale video file.
- Visualize an example frame depth map using a plasma colormap.

***

## Requirements

This project requires the following Python libraries:

- torch
- torchvision
- opencv-python
- matplotlib
- tqdm
- transformers
- Pillow (PIL)
- numpy

Install dependencies using:

pip install torch torchvision opencv-python matplotlib tqdm transformers


***

## How to Use

1. **Set your video path:**

   Edit the `video_path` variable in the script to point to your video file (e.g., `Pencil_Depth_Mapping.mov`).

2. **Run the script to:**

   - Load and extract frames from the video.
   - Apply depth estimation to every frame.
   - Visualize an example depth map (frame index 150).
   - Save all depth maps as a grayscale video (`depth_video.mp4`).

3. **Output:**

   - The depth maps are displayed for one frame with a color map.
   - A video file named `depth_video.mp4` is created showing the depth maps.

***

## File Structure Suggestion

- `/notebooks` - Your Jupyter notebook file if available.
- `/data` - Original video files.
- `/outputs` - The generated depth video and sample depth map images.
- `README.md` - This file for project details.

***

## Visualization

The depth maps are shown with a plasma colormap for better perception of distances in the frame.

*(Replace this with actual images if you add screenshots to your repo)*

***

## Notes

- The depth estimation model used is `"depth-anything/Depth-Anything-V2-Small-hf"` accessed via Hugging Face `pipeline`.
- The output depth video is grayscale and uses 20 FPS.
- Ensure your environment supports the required PyTorch and Transformers libraries.

***
