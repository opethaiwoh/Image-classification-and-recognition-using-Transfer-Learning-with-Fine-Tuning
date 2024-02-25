# Image-classification-and-recognition-using-Transfer-Learning
Using a CNN pre-trained on the ImageNet dataset and fine-tune it to perform image classification and recognize classes it was never trained on.

## Fine-tuning a convolutional neural network (CNN) involves a strategic, multi-step procedure designed to adapt a pre-trained model for a specific task without compromising the integrity of previously learned features. The process includes:

Node Removal: Eliminating the fully connected layers at the end of the network, which are responsible for generating specific class label predictions.
Node Replacement: Substituting the removed layers with new, uninitialized fully connected layers to tailor the model to a new task.
Layer Freezing: Locking the weights of the initial convolutional layers to preserve the generic features already learned, ensuring that these foundational insights remain unaltered during the initial phase of retraining.
Selective Training: Focusing the training efforts on the newly added fully connected layers to fine-tune the model’s predictions for its new application.
Layer Unfreezing (Optional): Gradually reactivating some or all of the previously frozen convolutional layers for a comprehensive, second phase of training, allowing the model to adjust more deeply to the nuances of the new task.
This methodical approach ensures that the network retains its ability to recognize broad patterns while being refined for enhanced performance on more specialized tasks."
1. Removing the fully connected nodes at the end of the network (i.e., where the actual class label predictions are made).
2. Replacing the fully connected nodes with freshly initialized ones.
3. Freezing earlier CONV layers earlier in the network (ensuring that any previous robust features learned by the CNN are not destroyed).
4. Training the FC layer heads.
5. Optionally unfreezinf some/all of the CONV layers in the network and perform a second pass of training.
