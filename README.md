# Anaglyph Video Processing in THREE.JS

[index.html](index.html) contains all the code for each task in PW1. 

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

## Description

Implementation of various anaglyph and image processing techniques unto a video.

Can be accessed here: [https://septianrazi.github.io/AnaglyphVideoProcessingInThreeJS/](https://septianrazi.github.io/AnaglyphVideoProcessingInThreeJS/)

### Image Processing Techniques
We included the following techniques for our code

- Anaglyphs
- Gaussian Blur
- Laplacian Filter
- Median Denoising Filter
- Seperable Gaussian Blur

Most of the code to accomplish this was done using fragment shader in the index.html file provided.

### How did we process the pixels near the edge?

Our implementation of all the convolutional image processing techniques required us to consider edge cases, not only on the video border but also on the anaglyph border. Our method essentially alters the way we normalise the convolution. On edges where there may be less pixels to consider compared to the middle, we divide the resulting convolution by a fair amount. This results in a more realistic edge.

## Installation

To run the project, simply run the file using a live server implementation. Extensions to do this are available in VSCode. 

## Usage

The videos sources are stereo videos, meaning that the output of our code shows the merging of both the right and left side of the video to create 3D anaglyphs. 

The image processing techniques applied onto the video contain different parameters, and can be stacked on top of each other. 

## Things to Note
- Due to the large file size of the videos, it may need time to load the website initially
- Some of the techniques such as median filters is performance intensive. We recommend keeping kernel sizes on the smaller size to avoid any performance hiccups.

## License

This project is licensed under the [MIT License](LICENSE).

