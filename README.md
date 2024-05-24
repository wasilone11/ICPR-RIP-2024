# ICPR-RIP-2024
## Baselines 
We provide two Colab runnable notebooks (Baseline_Single_View and Baseline_MV_early_fusion) as baselines for the Rider Intention Prediction Competition (https://mobility.iiit.ac.in/icpr_2024_rip/index.html). 
### Baseline_Single_View
It provides a step by step description of the steps involved starting from feature extraction using a VGG16 backbone, to an RNN based classification model. We provide the extracted features using ResNet50 and R(2+1)D as well.
### Baseline_MV_early_fusion
Does concatenation (early fusion) of features from Front, Right, and Left Views and then follows the same steps as Baseline_Single_View. Other fusion methods like channel-wise fusion (commented out in the notebook) can be used as well.
- Note: The video features provided here are from the 500 videos that are part of the train data. The 400:100 train:test split is only for baseline purpose.

## Dataset Structure 
The Dataset can be downloaded from here: https://mobility.iiit.ac.in/icpr_2024_rip/dataset.html 
- The Training Set will have features extracted from three backbones: VGG16, ResNet50, and R(2+1)D (Model reference links in the next section). Each of these folders will have folders named as the Frontal view, Left side mirror view, and the Right side mirror view. Within these folders will be the subfolders repressnting six maneuver classes having the maneuver features respectively. They are named as follows: Left Lane Change, Left Turn, Right Lane Change, Right Turn, Slow-Stop, and Straight.
- Note: For Single View RIP, participants should consider using data from the Frontal view only.

## References

### VGG16
- Paper: https://arxiv.org/abs/1409.1556
- Summary and Code: https://paperswithcode.com/method/vgg-16

### ResNet50
- Paper: https://arxiv.org/abs/1512.03385
- Summary and Code: https://paperswithcode.com/method/resnet

### R(2+1)D
- Paper: https://arxiv.org/abs/1711.11248
- Summary and Code: https://paperswithcode.com/method/r-2-1-d
