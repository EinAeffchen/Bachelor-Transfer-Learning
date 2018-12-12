# Code and Models for my bachelor thesis "Transfer Learning for Short Text Classification Applications"

The files here can be used to create language models and use these for transfer learning based classifiers. 

## Getting Started

Just clone this git and run the jupyter notebooks.

### Prerequisites

Take care that you follow the instructions for installing the fast.ai library correctly.
First download and install Anaconda. Used for this project is conda 4.5.11. Newer versions might work too, but if you have issues, stick to the version used here.

For an installation guide for Anaconda go [here](http://docs.anaconda.com/anaconda/install/windows/).

An installation guide for fast.ai can be found [here](https://forums.fast.ai/t/how-to-set-up-windows-10-for-fast-ai/9811).

### Usage

#### Creating a language model

To create a language model based on the sentiment140 dataset you first need to download the dataset from [Kaggle](https://www.kaggle.com/kazanova/sentiment140).
Rename the downloaded file into "train.csv" and copy it into "Create Languagemodel/sentiment140"
Now enter the Create Languagemodel folder, open a console and run 
```
jupyter notebook
```
In the new browser window you can open the "Sentiment140-Languagemodel.ipynb" file and just run all the cells. This will take a while.
The finished languagemodels name will be "lm0_fit_50k_bs70_clrB_noQRNN" and can be found in the models folder.
If you just want to use the pre-trained model, just copy it from the models folder into the corresponding classification task.

#### Fine-tuning a classifier and classification

Each Classification task contains 3 .ipynb files and a folder. The three datasets for these tasks can be found on the following websites:

EmoContext: [https://www.humanizing-ai.com/emocontext.html](https://www.humanizing-ai.com/emocontext.html)
HateSpeech: [https://data.world/ml-research/automated-hate-speech-detection-data](https://data.world/ml-research/automated-hate-speech-detection-data)
Sentiment140: see above

These Datasets belong into the subfolder inside the classification tasks, along the tmp and models folder.
Each models folder contains three subfolders, to use the corresponding languagemodel copy it into the correct subfolder along its itos_*.pkl file.
Except for the WikiText103 languagemodel, the other two pre-trained models are already copied into the model folders of the EmoContext Folder. The WikiText103 model can be downloaded [from fast.ai](http://files.fast.ai/models/wt103/).

When all files are downloaded and copied to the correct folders, you just need to run 
```
jupyter notebook
```
in the corresponding folder and run all cells in the notebook for the languagemodel you want to test.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details