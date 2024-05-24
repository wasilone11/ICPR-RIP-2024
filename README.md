# ICPR-RIP-2024
Baselines: We provide two Colab runnable notebooks (Baseline_Single_View and Baseline_MV_early_fusion) as baselines for the Rider Intention Prediction Competition. 
Baseline_Single_View provides a step by step description of the steps involved starting from feature extraction using a VGG16 backbone, to an RNN based classification model. We provide the extracted features using ResNet50 and R(2+1)D as well.
Baseline_MV_early_fusion does concatenation (early fusion) of features from Front, Right, and Left Views and then follows the same steps as Baseline_Single_View. Other fusion methods like channel-wise fusion (commented out in the notebook) can be used as well.
