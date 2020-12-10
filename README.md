# py895_quickDraw

Google quickDraw dataset, using 10 CAREFULLY selected categories to compare the architectures designed by each group member as well as several well known architectures such as alexNet, GoogLeNet, and ResNet. 
We started by selecting 10 categories of the 354 categories contained in the full Google quickDraw dataset: ['airplane', 'monalisa', 'dragon', 'giraffe', 'axe', 'banana', 'eiffeltower', 'snail', 'windmill', 'snowman']. We imported all of these sets, created a full set, and split 80% of it (1348669 samples) for the training, validation, and initial test of our neural networks. The remaining 20% of it (337167 samples) we separated and did not touch so that it could be used for a comparison test between the neural networks.
These sets are refered to as 'X_use', 'Y_use', 'X_onlytest', and 'Y_onlytest'.

Our project consists of two main notebooks: ML_QD_trainer.ipynb, ML_QD_comparison_test.ipynb, and ML_QD_pictionary.ipynb.

The first of these was the notebook used to design or import an architecture and train it. It begins by importing the 'use' datasets and formatting the data for use in the architectures. Next, we either import an architecture or make one. Following this, we train the model on the 'use' dataset. One can then save the trained model. To save on local space, the 'use' datasets are imported from the public_html of warsh's bu.physics website.

The second of these notebooks is the notebook used to import the trained models and test them. In these notebook, the trained models are tested on the 'onlytest' datasets, which are untouched in the training process for the models. We separated these samples from the 'use' set so that it is a fair comparison. If we pulled the samples for the test from the same dataset used in the training notebook, it is not a legitimate comparison because some of the models may have already seen some samples in the comparison test set, giving on obvious advantage to a model which has already memorized those images.

The third notebook is our for fun pictionary notebook. One may either import an image which is then formatted for the models or may use the draw features to draw their own image. These images are then put through the trained models and classified. 
