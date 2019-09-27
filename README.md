# Readme
The readme have the guide to replicate the results of our paper.
## Pre-Trainings
To Generate the psudo parallal corpus, we have used the code from [here](https://github.com/agaralabs/transformer-drg-style-transfer). The psudo parallal corpus have some noise because of the limitations of the model used to generate it, which affacts the content retention ability of the model. To reduce this effect, during pre-training we have used each sentences to be converted in both the target style. The training and validation data can be found under **dataset** directory.

Execute the below commands to run the pre-training:
```
export DG_TRAIN_DATA=Path to the training file generated in the previous step
export DG_EVAL_DATA=Path to the eval file generated in the previous step
export DG_MODEL_OUT=Path to save the Delete and Generate model weights
```
```
python openai_gpt_delete_and_generate.py \
--model_name openai-gpt \
--do_train \
--do_eval \
--train_dataset $DG_TRAIN_DATA \
--eval_dataset $DG_EVAL_DATA \
--train_batch_size 32 \
--eval_batch_size 32 \
--max_seq_length 85 \
--output_dir $DG_MODEL_OUT
```
## RL Training:
For RL training run all the cells of **Policy_Gradient_Final_version.ipynb** by filling the model and dataset path.

## Note:
We haven't put the GYAFC data as it requires permission from the authors of the dataset. 
