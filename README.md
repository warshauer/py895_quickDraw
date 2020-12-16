# py895_quickDraw

Google quickDraw dataset, using 10 arbitrarily selected categories to compare the architectures designed by each group member as well as several well known architectures such as ResNet and MobileNet.

We started by selecting 10 categories of the 354 categories contained in the full Google quickDraw dataset: ['airplane', 'monalisa', 'dragon', 'giraffe', 'axe', 'banana', 'eiffeltower', 'snail', 'windmill', 'snowman']. We imported all of these sets, created a full set, and split 80% of it (1348669 samples) for the training, validation, and initial test of our neural networks. The remaining 20% of it (337167 samples) we separated and did not touch so that it could be used for a comparison test between the neural networks.
These sets are refered to as 'X_use', 'Y_use', 'X_onlytest', and 'Y_onlytest' (these last two are imported as ot1.npy and ot2.npy respectively.

Our project consists of four main notebooks - ML_QD_trainer.ipynb, ML_QD_full_comparison.ipynb, and ML_QD_unrestricted_comparison.ipynb - and one notebook for fun - ML_QD_PictionaryProgram.ipynb. There are also several other notebooks uploaded that were used by groupmembers in training.

The first of these was the notebook used to design or import an architecture and train it. It begins by importing the 'use' datasets and formatting the data for use in the architectures. Next, we either import an architecture or make one. Following this, we train the model on the 'use' dataset. One can then save the trained model. To save on local space, the 'use' datasets are imported from the public_html of warsh's bu.physics website.

The second of these notebooks is the notebook used to import the trained models and test them. In these notebook, the trained models are tested on the 'onlytest' datasets, which are untouched in the training process for the models. We separated these samples from the 'use' set so that it is a fair comparison. If we pulled the samples for the test from the same dataset used in the training notebook, it is not a legitimate comparison because some of the models may have already seen some samples in the comparison test set, giving on obvious advantage to a model which has already memorized those images. These trainings were done with 4 architectures contributed by the group as well as ResNet50v2 and MobileNetv2. All training setups were the same.

The third notebook is the unrestricted comparison of the best models each group member could come up with. Group members were allowed to train for as long as they wanted and use as much computational time as they were willing to commit.

The fourth notebook is our for fun pictionary notebook. One may either import an image which is then formatted for the models or may use the draw features to draw their own image. These images are then put through the trained models and classified. It uses tkinter to create a GUI, so it can be a bit glitchy, if it doesn't want to function for you, there is a more simple fifth notebook called ML_QD_load_and_draw.ipynb, which allows a more simple usage. The pictionary parts only allow for the group models, as the trained resnet and mobilenet models were too large to put on the github (25mb limit); if one would like these trained models, they're available on http://physics.bu.edu/~warsh/ML_QD/ labeled model_RN50V2.h5 and model_MNV2.h5. The exact X_use.npy, Y_use.npy, ot1.npy, and ot2.npy data sets are also available on this site.

The PDF file is our project writeup which contains discissions of many of the ideas we explored in this project.

If you have any questions on any of these notebooks, feel free to reach out to the group members (warsh is particularly available since any terrible code that breaks was likely written by him).
