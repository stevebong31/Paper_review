# UnDeepVO: Monocular Visual Odometry through Unsupervised Deep Learning

## Abstract
UnDeepVO is able to estimate the 6-DoF pose of a monocular camera and the depth.
1. unsupervised deep learning scheme, 
2. and the other is the absolute scale recovery.
3. monocular system
   
The loss function defined for training the networks is based on spatial and temporal dense information.

![figure 1](/images/deepvo/1.png)

model-based methods tend to be sensitive to camera parameters and fragile in challenging settings, e.g., featureless places, motion blurs and lighting changes.

data-driven VO or deep learning based VO has drawn significant attention due to its potentials in learning capability and the robustness to camera parameters and challenging environments.

Currently obtaining ground truth datasets in practice is typically difficult and expensive, and the amount of existing labeled datasets for supervised training is still limited. 

proposed a novel unsupervised depth estimation method by using the left-right photometric constraint of stereo image pairs.

UnDeepVO only requires stereo imagery for training without the need of labeled datasets, it is possible to train it with an extremely large number of unlabeled datasets to continuously improve its performance.