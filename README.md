# CS168
Spring 2020 UCLA- A Comparative Analysis of Generative Adversarial Networks in synthetic CT generation

## Overview
This repository contains code that we developed and wrote to preprocess images from the RIRE Image Dataset, and then use the images to train and test differen GAN architectures. We assume that before executing this code, all prerequisite libraries are installed and the image dataset has been downloaded and compressed into 1 single tar file. 

**RIREImagePreprocessing.ipynb**: Use this to extract MHD files from the tar file and read/convert them into JPG files (only reads CT images and MR images). This was ran on Google Colab.

**SpineC2M.ipynb**: Use this to convert the images extracted from RIREImagePreprocessing.ipynb into TFRecords, train the model and evaluate the model. Here, we assume that all the images that contained artifacts from the dataset have been removed, beforehand, and the images are compressed into 1 zip file. This was ran on a JupyterLab Notebook deployed on a Google Cloud Platform Deep Learning instance that used tensorflow 1.15.

## Referenced Code
The majority of our code was based on an existing repository for https://www.mdpi.com/2076-3417/9/12/2521 (https://github.com/ChengBinJin/SpineC2M). Special thanks to the authors for helping us modify the code to fit our use case.