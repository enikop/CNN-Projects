# CNN projects in Tensorflow and Keras
## Problems
 * Classification on a small, 3-class subset of [Food101](https://www.kaggle.com/datasets/dansbecker/food-101) (**96%** test accuracy)
 * Classification on the [butterflies](https://www.kaggle.com/datasets/phucthaiv02/butterfly-image-classification) dataset
     * only the 15 most common classes (**96%** test accuracy)
     * all 75 classes (**87%** test accuracy)

## Main approaches
  * CNNs from scratch
  * Using pre-trained networks for feature extraction, adding only the fully-connected classification layers
      * MobileNetV2
      * EfficientNetB0 (_unfit preprocessing in Food101, has been corrected for butterflies_)
      * ResNet50 (_unfit preprocessing in Food101, has been corrected for butterflies_)