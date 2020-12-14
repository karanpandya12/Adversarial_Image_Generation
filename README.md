# Adversarial_Image_Generation
Experiments on generation of Adversarial images (Implemented using PyTorch)

## What are adversarial images?
Adversarial images are images that look almost identical the original image and are designed to fool
different neural networks. They expose a security issue of CNNs that malicious users can take advantage of.
Lot of research work is being done in this area to make neural networks more robust to adversarial images.

## Dataset
The very poular MNIST dataset was used to perform these experiments. The MNIST database of handwritten digits. It has a training set of 60,000 examples and a test set of 10,000 examples.<br>
<p align = "center">
  <img src = "/Images/dataset_1.png" height = 300>
</p>

## Results
#### Creating adversarial images such that the network misclassifies the image as any label other than the ground truth
<p align = "center">
  <img src = "/Images/result_1.png" height = 250><br>
  <img src = "/Images/result_2.png" height = 250>
</p>

#### Creating adversarial images such that the network misclassifies the image as a chosen target label
<p align = "center">
  <img src = "/Images/result_3.png" height = 250><br>
  <img src = "/Images/result_4.png" height = 250>
</p>

#### Retraining the network and checking the predictions on adversarial images generated using the old network
Note that the network was not trained using the adversarial samples. The network was re-trained on the same MNIST dataset as earlier.
The purpose of this experiment was to see whether adversarial images which fool one neural network can fool another neural network with different weights and parameters.

It was observed that in many cases the new network was able to predict the correct label. But it was still prone to errors and occassionaly predicted the adversarial label. In very rare cases, it predicts a random wrong label which is different from both the adversarial label and the ground truth label. <br>
<p align = "center">
  <img src = "/Images/result_5.png" height = 500>
</p>
