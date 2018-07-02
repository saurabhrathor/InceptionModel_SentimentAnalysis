# InceptionModel_SentimentAnalysis
Performing sentiment analysis on Data using Inception Model. Fasttext is used for Word vectorization.

The code is a part of Test I participated in during an Interview Process. It is built around a recent paper on the topic of NLP. 
The paper:
BB twtr at SemEval-2017 Task 4: https://arxiv.org/pdf/1704.06125.pdf

Here in - 
1. First part is -- Pre-processing of Data to remove unnecessary charactres and repetative words (Temed as Stemming & Lemmatization)
2. Next, Trimming and padding of each sentence to MAX_SEQUENCE_LENGTH
3. Splitting of Dataset in Training, Validation and Testing part
4. Converted Words to Vectors using Fastext Embeddings.
    --> Fasttext is better as it divides the word in smaller parts (called n-grams), and then generate the model as per those n-grams.
        This help in cases of those words which are rarely used, OR are not present in training set. As the probabilty of n-grams 
        repeating in vocab increases as compared to that rare word.

====== Building the Model ============

1. Using CNN -
  CNN is applied using different filter sizes 2x2, 3x3 and 4x4 as per Paper.
  Passing thorugh Dropout layers of 50%
  Contatenating results of above and passing through a Fully Connected Layer

2. Using LSTM - 
  Birectional LSTM is applied with dropout 50% and passed through Dense Layer.
