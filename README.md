# ICPR-RIP-2024
(https://mobility.iiit.ac.in/icpr_2024_rip/index.html)
## Baselines 
We provide two Colab baseline runnable notebooks for task 1 i.e., single/frontal-view rider intention prediction (Baseline_Single_View) and task 2 i.e., multi-view rider intention prediction (Baseline_MV_early_fusion). 
### Task 1 (Single-view RIP): Baseline_Single_View
We provide a step-by-step description of the steps involved starting from feature extraction using a VGG16 features, to an RNN based classification model. In the website (https://mobility.iiit.ac.in/icpr_2024_rip/dataset.html) we also provide the extracted features using ResNet50 and R(2+1)D as well that can be used for experiments. 
### Task 2 (Multi-view RIP): Baseline_MV_early_fusion
For multi-view we provide a baseline that does concatenation (early fusion) of features from Frontal-view, Right-side-mirror-view, and Left-side-mirror-view and then follows the same steps as Baseline_Single_View. We also provide other fusion methods like channel-wise fusion (commented out in the notebook) that can be used as well.
**Note**: The video features provided here are from the 500 videos that are part of the training dataset. The 400:100 train:test split is performed only for baseline purpose.

## Dataset Structure 
The Dataset features can be downloaded from here: https://mobility.iiit.ac.in/icpr_2024_rip/dataset.html 
- The Training Set will have features extracted from three backbones: VGG-16, ResNet-50, and R(2+1)D.
- The dataset structure of the training set consists of three subfolders, namely, frontal_view, left_side_mirror_view, right_side_mirror_view. Each of these subfolders have six maneuver classes (i.e., label folders), namely, Left Lane Change, Right Lane Change, Left Turn, Right Turn, Slow-Stop, Straight. The label folders have maneuver video features respectively. For example, there are 29 video features of maneuver left lane change in Left Lane Change folder.
- For Task 1, frontal_view video features needs to be used and for Task 2, all three views i.e., frontal_view, left_side_mirror_view and right_side_mirror_view video features needs to be used in developing the model.

## Evaluation Metrics
The participants are required to output maneuvers classes for each video feature. We evaluate RIP with two ranking metrics for _Task 1_ and _Task 2_: the **classification accuracy**, handling the driving maneuvers as classes, and the **F1** score for detecting the maneuvers (i.e. the harmonic mean of the precision and recall). More details on evaluation metrics: https://mobility.iiit.ac.in/icpr_2024_rip/dataset.html

## References

### VGG-16
- Paper: https://arxiv.org/abs/1409.1556
- Summary and Code: https://paperswithcode.com/method/vgg-16

### ResNet-50
- Paper: https://arxiv.org/abs/1512.03385
- Summary and Code: https://paperswithcode.com/method/resnet

### R(2+1)D
- Paper: https://arxiv.org/abs/1711.11248
- Summary and Code: https://paperswithcode.com/method/r-2-1-d
