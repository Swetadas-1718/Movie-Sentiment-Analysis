# IMDB-Movie-Review-sentiment-Analysis
Sentiment analysis is the process of using natural language processing, and statistics to analyze the sentiment behind a text. It is a text analysis method that detects polarity (e.g. a positive or negative opinion) within the text, whether a whole document, paragraph, sentence, or clause.

Sentiment analysis is an extremely useful tool that helps us to efficiently monitor social media.

## Dataset
The dataset used here can be downloaded from this Kaggle link. If you download the dataset and extract the compressed file, you will see a CSV file. The file contains 50,000 records and two columns: review and sentiment. The review column contains the text for the review and the sentiment column contains sentiment for the review. The sentiment column can have two values i.e. “positive” and “negative” which makes our problem a binary classification problem.

## Preprocess data
During analyzing our data we found that many of the reviews contained HTML tags, numbers, and special characters which do not hold any significant meaning in the review. So the next step was to remove them.

## Classification Task
1) Sentiment Analysis using RNN "Bi-LSTM"
2) Training using a custom word embedding created using bag of words and tf-idf vectorization 

## Designing the RNN model
I added different layers such a sembedding layer, Bi-LSTM kayer and a dense layer.
Bidirectional Long Short-Term Memory (BiLSTM) is a type of recurrent neural networks. It processes data in two directions since it works with two hidden layers. This is the main point of divergence with LSTM. BiLSTM has proven good results in natural language processing.

![model_design](https://user-images.githubusercontent.com/71088477/189077251-d18056f5-ff47-4295-a4e3-c94c09a5b3b4.png)

## Training the model
I used ‘binary_crossentropy’ as loss function as this is a binary classification. Also, I used Earlystoping method from Keras so that I can stop the training process when we get the minimum validation loss. After training the model for 8 epochs the validation accuracy was about 87% which is not bad.

## Tested own reviews
The next step was to test my model on real reviews and see if it is any good.

## Sentiment Analysis app using streamlit
If you have not heard of streamlit, then you need to quickly check it out. It is an open-source app framework for Machine Learning and Data Science which helps us to make beautiful data apps in hours, not weeks. 
![ss](https://user-images.githubusercontent.com/71088477/189079288-dd1d42e5-6aea-4983-a508-3eb9510015f4.png)
![ss2](https://user-images.githubusercontent.com/71088477/189079789-aead199e-02af-4603-84d0-d9ac304b80c4.png)

As we saw, based on the points given by the critics, the web app was able to classify reviews accurately.
