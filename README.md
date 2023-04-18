# Image-classification-and-recognition-using-Transfer-Learning-with-Fine-Tuning
Using a CNN pre-trained on the ImageNet dataset and fine-tune it to perform image classification and recognize classes it was never trained on.

## Fine-tuning is a multi-step process that involve the ffg:
1. Removing the fully connected nodes at the end of the network (i.e., where the actual class label predictions are made).
2. Replacing the fully connected nodes with freshly initialized ones.
3. Freezing earlier CONV layers earlier in the network (ensuring that any previous robust features learned by the CNN are not destroyed).
4. Training the FC layer heads.
5. Optionally unfreezinf some/all of the CONV layers in the network and perform a second pass of training.
