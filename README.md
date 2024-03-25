# Introduction
This repo is for the course project of EE5179: Deep Learning for Imaging at IIT Madras, under Prof. Kaushik Mitra, EE Dept. In this project, the Neural Radiance Field architecture was implemented for a custom dataset, created and processed from scratch. 

There are two datasets in this repo, one of an idol, and another of one of the students, Sunki. The outputs at all stages (video, COLMAP outputs, and poses) are shown for the idol dataset, while only the poses output is shown for the Sunki dataset. 

# Instructions

This is the procedure used to train any dataset:
1. Pass the `.mp4` file through the `frames_extract.ipynb` notebook to sample out a certain number of frames/photos from the video.
2. Pass the sampled photos to the COLMAP software, the output data of which is stored in the `/colmap/output` folder.
3. This is now passed to the `load_data.ipynb` notebook, from which we store the output arrays in a `.npz` file.
4. The values from the `.npz` file are now extracted in the `model.ipynb` notebook to train the model.

# Limitations

NeRF is a model that needs to be overfit, and due to the lack of computational resources and time, we were unable to replicate the exact images.
