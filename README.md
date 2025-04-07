# CNN projects in Tensorflow and Keras
## Problems
 * Classification on a small, 3-class subset of [Food101](https://www.kaggle.com/datasets/dansbecker/food-101) (**96%** test accuracy)
 * Classification on the [butterflies](https://www.kaggle.com/datasets/phucthaiv02/butterfly-image-classification) dataset
     * only the 15 most common classes (**96%** test accuracy)
     * all 75 classes (**87%** test accuracy)
 * Simple visualization of faulty classification decisions and the top probability classes for butterflies [here](butterfly\analysis_butterflies_classification_efficientnet_75_BEST.ipynb) (last cell)
 * Open set classification solutions for the detection of unknown (untrained for) objects
     * thresholding after softmax
     * thresholding before softmax - [results](butterfly\open_set_butterflies_classification.ipynb)
     * OpenMax layer

## Main approaches
  * CNNs from scratch
  * Using pre-trained networks for feature extraction, adding only the fully-connected classification layers
      * MobileNetV2
      * EfficientNetB0 (_unfit preprocessing in Food101, has been corrected for butterflies_)
      * ResNet50 (_unfit preprocessing in Food101, has been corrected for butterflies_)

## Preliminary results
   * EffiecientNetB0 seems to be the most suitable pre-trained model for the 75-class butterflies dataset
       * more promising results (**>90%** test accuracy) can be reached by training a CNN of 11 million parameters from scratch (based on experiments conducted by other parties in the research group)
   * As expected, thresholding after softmax is insufficient (based on experiments conducted by other parties in the research group)
   * Thresholding on logits provides more accuracy in unknown pattern detection, but with a considerable tradeoff of about 10% loss in accuracy on base test sets (mistakes unseen data from known classes for unknown class)

## To do
   * OpenMax layer
   * other solutions for Open Set Networks