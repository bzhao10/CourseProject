# CS410 CourseProject(Text Classification Competition): Twitter Sarcasm Detection 

## Table of Contents

- [Background](#background)
- [Install](#install)
- [Usage](#usage)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Background

This is a course project for CS410 Text Information Systems and is a part of a text classification competition, which involves twitter sarcasm detection.
In this competition, it is required that you classify a twitter response in a conversation into either 'sarcasm' or 'not sarcasm'.

### Data

The [dataset](https://github.com/CS410Fall2020/ClassificationCompetition/tree/main/data) is comprised of two jsonl files, including a train.jsonl for data training and a text.jsonl for text classification.

Each line of the training data set includes the following fileds:
- ***response*** :  the Tweet to be classified
- ***context*** : the conversation context of the ***response***
- ***label*** : `SARCASM` or `NOT_SARCASM` 
- ***id***:  String identifier for sample.

The text classification file (test datset) differs from the training dataset only in that the file lacks the label.

The size of training dataset is 5000 and the size of the test dataset is 1800.

### Output
The output of the project is an anwser.txt document, which includes both id of test sample and a label of either `SARCASM` or `NOT_SARCASM` predicted by the model.

## Install

You can run the whole project on [Google Colab](https://colab.research.google.com/). You don't have to install anything locally.

## Usage

Each of the ipynb file in the [Code](https://github.com/bzhao10/CourseProject/tree/main/Code) folder represents one solution in the competition.

- ***Step 1*** Download two jsonl files, one training data and one test data, from dataset.
- ***Step 2*** Download one of these ipynb files and open it on [Google Colab](https://colab.research.google.com/).
- ***Step 3*** Upload the two jsonl files to [Google Colab](https://colab.research.google.com/) under the dataset folder in the project that you have opened in ***Step 2***.
- ***Step 4*** Run the code line by line using [Google Colab](https://colab.research.google.com/).

By following all the steps mentioned above, you will get an answer.txt file.

Please refer to the presentation video for detailed instructions.

## Results

The following table records the best performance achieved (highest F1 score) by using each model:

| Model| Precision | Recall| F1 |
|-------|-------|-------|-------|
| ALBERT  | 0.65814 |0.77222 | 0.71063 |
| ALBERT V2  | 0.64377 |0.56222 | 0.60024 |
| BERT  | 0.62681 | 0.86778 | 0.72787 |
| BERT(RSUP) | 0.64717 | 0.76222 | 0.7 |
| BERT(R_context) | 0.66042 | 0.70444 | 0.68172 |
| RoBERTa  | 0.65887 | 0.86888 | 0.74053 |
| RoBERTa-large  | 0.54708 | 0.98778 | 0.70416 |
| RoBERTa(R_context)  | 0.67836 | 0.77333 | 0.72274 |
| SqueezeBERT  | 0.61348 | 0.91 | 0.73289 |
| XML-RoBERTa  | 0.61864 | 0.89222 | 0.73066 |

REUP: Remove stopwords and unnecessary puncuations

R_context: Reverse Context

## Contributing

### Conntributors
Team Name: GFZ

Team Member: <br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Bei Zhao - beizhao3 (Captain) <br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Ryan Fraser - rfraser3 <br />
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Yiming Gu - yimingg7 <br />

## License/Ciatation
Tutorial:[Fine-Tuning BERT for Spam Classification](https://colab.research.google.com/github/prateekjoshi565/Fine-Tuning-BERT/blob/master/Fine_Tuning_BERT_for_Spam_Classification.ipynb#scrollTo=k1USGTntS3TS)
