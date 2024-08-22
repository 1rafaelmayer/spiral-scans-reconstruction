# Reconstructing Sparsely Sampled Scanning Probe Microscopy Images with Gaussian Process

This tutorial will guide you through the process of reconstructing images from sparsely sampled near-field microscopy data using Gaussian Process.

The code used here is based on the work by Fu, Matthew, et al., titled "Accelerated Nano-Optical Imaging through Sparse Sampling," published in *Nano Letters* (2024). You can find the original paper [here](https://pubs.acs.org/doi/10.1021/acs.nanolett.3c03733).

If you plan to use this code, please remember to cite our work.

**Why does this matter?**

Near-field microscopy (s-SNOM) lets us capture extremely detailed images of a sample, down to just a few nanometers. It's particularly useful for identifying materials based on their chemical makeup. However, scanning the entire image pixel by pixel can be very time-consuming. Ideally, we want to measure only as many pixels as needed to get the information we want.

Instead of scanning an image line by line (raster scanning), the idea here is to scan only a few pixels and then use an algorithm to reconstruct the full image. There are several ways to do this, such as compressed sensing, but in this tutorial, we’ll focus on using Gaussian Process. We’ll scan the image using a spiral pattern, which covers most of the image content with a continuous motion.

In this tutorial, I’ll show you how to:

- Load the data
- Simulate a spiral scan from a real s-SNOM image
- Test the Gaussian Process for image reconstruction
- Choose appropriate Kernel for Gaussian Process
