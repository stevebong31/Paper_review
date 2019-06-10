# Unsupervised Learning of Depth and Ego-Motion from Video

## Abstract

unsupervised learning framework for the task of monocular depth and camera motion estimation from unstructured video sequences

Our method uses single-view depth and multi-view pose networks, with a loss based on warping views to the target using the computed depth and pose (applied independently)

## Introduction 

Humans are remarkably capable of inferring ego-motion and the 3D structure of a scene even over short timescales. 
So why do humans excel at this task? (past visual experience)

From millions of such observations, we have learned about the regularities of the world—roads are flat, buildings are straight, cars are supported by roads etc., and we can apply this knowledge when perceiving a new scene, even from a single monocular image. 

![figure 1](/images/usl_depth_ego/1.png)

End-to-end approach in allowing the model to map directly from input pixels to an estimate of ego-motion (parameterized as 6-DoF transformation matrices) and the underlying scene structure (parameterized as per-pixel depth maps under a reference view). 

## Approach 

 the scene appearance change across different frames is dominated by the camera motion. 

 ### View synthesis as supervision 

 ### Differentiable depth image-based rendering 