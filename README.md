# Pytorch-CIFAR10-Image-Classification

### 1. Data preprocessing & augmentation
- RandomResizedCrop: and RandomHorizontalFlip are useful.
- RandomRotation, RandomVerticalFlip and Normalizea are unuseful.

### 2.Define the model
- ResNet
  - Classic CNN network.
  - Very easy to achieve 90%+ score on this dataset.
- ViT
  - Use transformer framework on vision tasks.
  - Training more slowly than ResNet.

### 3. Pipelines
- Design unified pipelines to train model and test on test dataset.

### 4. Train model
- ResNet
  - larger framework is not useful.
  - Adam and StepLR is better.
  - larger learning rate is batter (1e-3 > 1e-4).
- ViT
  - Because of slow convergence speed, MultiStepLr can set a large learning rate in the beginning to accelarate training.
  
### 5. Evaluation
  - Compare ResNet and ViT with following metrics:
    - Precision
    - Recall
    - F1 score
    - Overall Accuracy
    - ROC curve
    - AUC
    - Confusion matrix
- Accuracy and AUC of Resnet are higher than ViT.
- Both of models are more likely to confuse airplane and dog.

### Ensemble Learning
- Using Ensemble Learning method, use Resnet and ViT vote for the pridiction result.
- Weights of them is Resnet:ViT = 3:1.
