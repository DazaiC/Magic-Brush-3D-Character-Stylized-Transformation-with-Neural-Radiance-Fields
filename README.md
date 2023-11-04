# Magic-Brush-3D-Character-Stylized-Transformation-with-Neural-Radiance-Fields
Colab code: https://colab.research.google.com/drive/1wH_EXDCostTjD5UGj7OGYXgzVP6OLs2c
# Introduction
A good external image can be used to express personality and achieve better social goals, but often we are not clear about what is right for us. With the advancement of technology, there are many ways for us to find the style that best suits us. We can use deep learning models to simulate various styles, reducing the cost of trial and error.
In the foreseeable future, socialization will evolve from 2D to 3D. In that world, we would similarly want our avatars to be presentable. Hence, we intend to build a system that can simulate personal 3D images based on individual style preferences. 
We have attempted to use the NeRF architecture to generate 3D images. Additionally, we use the Instruct NeRF2NeRF model, which combines GPT, the diffusion model, and NeRF, to produce images with a specified individual style.

# Dataset
A 27s, 797 frames mp4 video of Roger's full-body portrait, captured by Pixel 4a’s camera; a 20s, 603 frams mp4 video of TaTsan’s full-body portrait and 31s, 897 frams mp4 video of Steven’ s upper half-body portrait
The camera poses were extracted using COLMAP.

# Methodology
First, we use the COLMAP algorithm to convert photos from different angles into data with spatial dimensions, where each data point is represented as xT = [x, y,z, 0,$].
After feeding the data into an MLP (Multi-layer Perceptron), NeRF uses volume rendering techniques to obtain the color of each point from different angles.
First, we use the COLMAP algorithm to convert photos from different angles into data with spatial dimensions, where each data point is represented as xT = [x, y,z, 0,$].
After feeding the data into an MLP (Multi-layer Perceptron), NeRF uses volume rendering techniques to obtain the color of each point from different angles.

To obtain good results, photos need to be collected from different angles.

# Results
Video Demo https://youtu.be/WG_YBp7Z3s8

# Discussion and Conclusion
Input dataset video needs to reduce overlapping routes and increase multi-view input to minimize rendering blur 3D result.
When targeting a specific object for 3D imaging, the object can be well-reproduced, but the surrounding environment becomes blurry in direct proportion to the distance from the object.

# Future Work
We hope to apply this technology in the future to generate various home decoration styles, allowing families to choose suitable interior designs more quickly and accurately.

# References
[1] Mildenhall, Ben, et al. "Nerf: Representing scenes as neural radiance fields for view synthesis." Communications of the ACM65.1 (2021): 99-106.
[2] Haque, Ayaan, et al. "Instruct-nerf2nerf: Editing 3d scenes with instructions." arXiv preprint arXiv:2303.12789 (2023).
