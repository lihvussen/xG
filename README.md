This project aims at creating a xG algorithm. xG, also known as expected goals is a football stat which popularity is rising in recent years. It describes the probability of scoring a goal given
particular conditions.

In this case, 3 different model were created. First one, 'xG_shot_parameters.ipynb' only takes into account binary features annotated to some extent subjectively for each of 106 shots,
gathered in 'Chances.xlsm' file. Model architecture is a deep neural network created with keras and tensorflow libraries.

Second one, 'xG_pics_only.ipynb' only focuses on pictures, 10 of which were also uploaded in this repository. These are screenshots of shot moments in Valencia CF home games from 2012-2022 period.
The same stadium in each case should diminish the bias of different backgrounds, which might be significant as the dataset is not huge, since it was all gathered on my own. The model was designed
as convolutional neural network. The results were also promising, overally slightly worse than for the binary model, however the in some cases it did operate better.

Last one 'xG_all.ipynb' is the combination of the 2 mentioned above. The 2 neural networks are concatinated, so both of the datasets are used together. However, this model obtained the worst results.
This could be caused by keeping the same architecture for both parts of the model. With some experiments it could probably get muh better.

The evaluations were made mostly in a subjective way as there is no state of art method in xG field.
