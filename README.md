# Readme
The readme have the guide to replicate the results of our paper.
## Pre-Trainings
To Generate the psudo parallal corpus, we have used the code from [here](https://github.com/agaralabs/transformer-drg-style-transfer). The psudo parallal corpus have some noise because of the limitations of the model used to generate it, which affacts the content retention ability of the model. To reduce this effect, during pre-training we have used each sentences to be converted in both the target style. The training and validation data can be found [here](https://github.com/agaralabs/rl-st/tree/master/dataset)
