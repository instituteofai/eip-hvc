# eip-hvc

A **multi-output multi-class** classification problem.



## Images

The dataset contains images of human beings that are padded with empty/black pixels on either side to create colored RGB images of dimensions `224 x 224`.



## Labels to predict

There are 8 labels that have to be predicted for each image (multi-output). Each label can has multiple possible values (multi-class).

1. Gender

   1. Male

   2. Female

      

2. Image Quality

   1. Bad

   2. Average

   3. Good

      

3. Age

   1. 15 - 25

   2. 25 - 35

   3. 35 - 45

   4. 45 - 55

   5. 55+

      

4. Weight

   1. Underweight

   2. Normal-healthy

   3. Slightly-overweight

   4. Overweight

      

5. Bag

   1. Daily/Office/Work Bag

   2. Grocery/Home/Plastic Bag

   3. None

      

6. Footwear

   1. Can't See

   2. Fancy

   3. Normal

      

7. Emotion

   1. Angry/Serious

   2. Happy

   3. Neutral

   4. Sad

      

8. Body pose

   1. Back
   2. Front-frontish
   3. Side

   

[Solution](/colab/EIP_HVC_ResNet_50_2.ipynb)



## Approach

1. One-hot encode the labels to be predicted.
2. Use the following neural network architecture:
   [TODO - add image of model]
3. Use the following image augmentation:
   1. Horizontal flip
   2. Rotation
   3. Width/Height shift
   4. Zoom
4. Use a cylical learning rate for faster convergence.



## Things to try

1. Increase the types of image augmentation using the [imgaug](https://github.com/aleju/imgaug) library.
2. Use [hyperopt](https://github.com/hyperopt/hyperopt) for hyperparameter optimization.
