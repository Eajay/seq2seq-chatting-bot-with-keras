# Seq2seq chatting bot with keras
The program implements models by Python 3.7 with Keras that using Tensorflow-gpu backend. All files are writen in Jupyter format. The purpose of this projects lies in comparing the results of three different models.
  - Concatenate model 
  - naive seq2seq model 
  - seq2seq with attention layer model
 
### Required dataset
##### Training data
All models use cornell movie dialogs corpus as training data, which contains more than 100,000 converstaions. The training data is available on: \
https://www.cs.cornell.edu/~cristian/Cornell_Movie-Dialogs_Corpus.html

##### Embedding file
The program selects Glove with 100 dimension as default embedding matrix. The file is available on:\
https://nlp.stanford.edu/projects/glove/

##### My own question
Since BLEU score is not accurate when it comes to dialog generation, I design 100 sentences to test the models' performances which requires people to judge whether the response sentences are good enough.
The question is available in question.csv.

### Models pictures
Concatenate:\
![alt text](https://github.com/Eajay/seq2seq-chatting-bot-with-keras/blob/master/picutures/concate.png)

Naive Seq2seq:\
![alt text](https://github.com/Eajay/seq2seq-chatting-bot-with-keras/blob/master/picutures/seq2seq.png)

Seq2seq with Attention Layer:\
![alt text](https://github.com/Eajay/seq2seq-chatting-bot-with-keras/blob/master/picutures/attention.png)

### Installation

The system requires several python libraries.
Install the dependencies by requirements.txt:
```sh
$ pip3 install -r requirements.txt 
```

#### Running code
Before training the models, you need to run preprocess.ipynb file to get pickle files that contain preprocessed training data.
Then select one of the model files to run and you should get a saved model file named ending with .h5.
To test the models, run the question_response.ipynb and get responses.

### Result
The three models' results are presented in answer.csv. 
Personally speaking, the result of naive seq2seq is better than the other two models. Without Seq2seq, concatenated model has a poor result. In additional, Seq2seq With attention layer might focus too much on some words which decrease the diversity of responses.

License
----
MIT



