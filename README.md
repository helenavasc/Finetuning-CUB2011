# Finetuning-CUB2011
For anyone who wants to either separate CUB Birds into its designated train-test split, fine-tune a pre-trained PyTorch Model, or both.
Thank you to PyTorch for code used in `pretraining.py`

Step 1:
Because CUB2011 has a pre-defined train-test split in `train_test_split.txt` but the dataset itself is not already separated in this manner, we first need to run all the code cells in `splitting_test_and_train.ipynb`, which separates the dataset according to the contents of `train_test_split.txt`. You must only need to change the following line: `CUB_200_2011_path = '/vision2/u/helenav/CUB/CUB_200_2011'` Please change this line of code to reflect your dataset path.

Step 2:
After you have ran `splitting_test_and_train.ipynb`, you will need to run `pretraining.py`, but make sure to change certain lines of code in `pretraining.py` first! Specifically, change line 20 `data_dir = "/vision2/u/helenav/CUB/CUB_200_2011/images"` to reflect the dataset path (with the subdirectory 'images'). You must also change line 39 `save_model_path = "/scr/helenav/ToM/pretrained_models/state_dict_model.pt"` to reflect where you will like to save your model. You can also change which model you are finetuning on, the batch size, the number of epochs, in lines 23, 29, and 32, respectively.

Please email me at helena v [at] stanford [dot] edu if you have any questions. 
