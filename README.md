# Detecting-Fake-Tweets-Related-to-The-Russian-Invasion-of-Ukraine-by-Applying-Deep-Learning-Approach

In the technological project, the fake tweets (content) task was approached by applying Deep Learning approach. The project’s objective was to build Deep Learning models that are able to identify whether anything related to the Russian invasion of Ukraine in 2022 on Twitter.The main goal of this project was to build Deep Learning models that would automatically classify tweets related to the Russian invasion of Ukraine in 2022 on Twitter with high accuracy. The developing process was focused on Deep Learning algorithms that are based on the following features: Sentence segmentation, Word tokenization, Tagging parts of speech, Stop words, etc.

# Research Question
This technological project proposes the research question of what accuracy can be reached in detecting fake tweets related to Russian invasion of Ukraine by applying developed the Long Short-Term Memory (LSTM) neural networks and the Gated Recurrent Unit (GRU) neural networks models. Specifically, the aim of this project is to develop and train Long Short-Term Memory (LSTM) neural networks and Gated Recurrent Unit (GRU) neural networks models by using publicly available datasets with related tweets. Additional question of the project is to identify the most accurate model that is effective in predicting fake tweets while also minimising the training time.

# Pre-Process Diagram

The diagram illustrates the process of creating The Long Short-Term Memory (LSTM) network and the Gated Recurrent Unit network models.
<img width="690" alt="Screenshot 2022-08-15 at 11 23 03" src="https://user-images.githubusercontent.com/76842663/184619197-fba8ceac-6318-47a3-b809-b55cedb16226.png">
# Long Short-Term Memory (LSTM) Model Architecture 

<img width="499" alt="Screenshot 2022-08-15 at 11 27 30" src="https://user-images.githubusercontent.com/76842663/184619824-17adcfe6-10f9-49ca-bdba-48aca094185b.png">

# The Gated Recurrent Unit (GRU) Model Architecture 

<img width="449" alt="Screenshot 2022-08-15 at 11 27 55" src="https://user-images.githubusercontent.com/76842663/184619927-ab0949f3-78fd-4e62-9c25-f59dd7013c64.png">

# The Long Short-Term Memory (LSTM) Model Prediction

All the results have been reached after a slight model modification that improved accuracy and reduced loss. A new convolutional layer (Conv1D) has been added to the model architecture, while the amount of included neurons in The Long Short-Term Memory layer and Dence layers were decreased. Nevertheless, the training dataset had enough data to train the model with many neurons, the decision to decrease the number of neurons was made, in order to increase the training speed of the Long Short-Term Memory (LSTM) Model. Based on the graphs, it seems that the model operates faster and predicts fake and real tweets more accurately after the number of neurons and layers were decreased from 300 neurons to 64 neurons and Dence layers from 5 to 1. The additional Convolutional Layer with one Dimension assisted in decomposing the input data into smaller parts, before going through the Long Short-Term Memory (LSTM) layer. In order to ensure that the data has not been randomly tested for more fake tweets than real tweets (vice versa), preconfigured validation data was also applied.

### The graph illustrates the training and validation accuracy of the LSTM model based on every running epoch.
<img width="422" alt="Screenshot 2022-08-15 at 11 31 54" src="https://user-images.githubusercontent.com/76842663/184620661-492e6092-accd-4236-bfef-ad2da1698e58.png">

### The graph illustrates the training and validation loss of the LSTM model based on every running epoch.
<img width="418" alt="Screenshot 2022-08-15 at 11 32 14" src="https://user-images.githubusercontent.com/76842663/184620692-8eeab5eb-03e0-4f75-8e32-1d960969dfe5.png">

### The confusion matrix for prediction performance of the Long Short-Term Memory (LSTM) Model.
<img width="383" alt="Screenshot 2022-08-15 at 11 32 36" src="https://user-images.githubusercontent.com/76842663/184620849-9078aa8b-0391-4a76-956c-213edaf1269a.png">

### The classification report illustrates Accuracy, Precision, Recall and F-1 Score for prediction performance of the Long Short-Term Memory (LSTM) Model.
<img width="459" alt="Screenshot 2022-08-15 at 11 32 56" src="https://user-images.githubusercontent.com/76842663/184620922-daedac19-43b7-4527-832e-1674e9443c6a.png">

According to the classification report, the accuracy of the Long Short-Term Memory (LSTM) Model was 0.97 %, it means that 97 % of tweets were classified correctly. However, it is important to highlight that the high accuracy result was reached on the ideal data with a large number of fake and real tweets. The precision results illustrated 0.95 % for real tweets and 0.98% for fake tweets. The recall results were 0.98 % for real tweets and 0.96 % for fake tweets. Additionally, the f1-score result for each category was 0.97 %. It seems that the prediction performance result of the Long Short-Term Memory (LSTM) Model was extremely close to the ideal result of 1. However, the nearly perfect prediction performance of the Long Short- Term Memory (LSTM) Model has become possible due to important several factors, such as : the large amount of data has been used to train the model and the ideal data distribution (with 30847 fake tweets and 29761 true tweets).

# The Gated Recurrent Unit (GRU) Model Prediction 
The final training run after all data- related training and problems were addressed. The training/ validation accuracy and training/ validation loss have been increased and decreased respectively, as illustrated in both graphs. The right parameters and modifications helped to develop the Gated Recurrent Unit (GRU) Model which was able to operate properly and perform high-accuracy predictions with little loss on both testing and training data.

### The graph illustrates the training and validation accuracy of the GRU model based on every running epoch.
<img width="458" alt="Screenshot 2022-08-15 at 11 43 26" src="https://user-images.githubusercontent.com/76842663/184624185-167d6d0c-76be-49ba-bf8c-d514d9f12986.png">

### The graph illustrates the training and validation loss of the GRU model based on every running epoch.
<img width="422" alt="Screenshot 2022-08-15 at 11 43 47" src="https://user-images.githubusercontent.com/76842663/184624271-ffb2902f-15ae-4bb8-955e-e70815c30afc.png">

### The confusion matrix for prediction performance of the GRU Model.
<img width="387" alt="Screenshot 2022-08-15 at 11 44 12" src="https://user-images.githubusercontent.com/76842663/184625214-e4071b58-351a-459e-8886-9ec85822ec51.png">

### The classification report illustrates Accuracy, Precision, Recall and F-1 Score for prediction performance of the Long Short-Term Memory (LSTM) Model.
<img width="486" alt="Screenshot 2022-08-15 at 11 44 37" src="https://user-images.githubusercontent.com/76842663/184625281-e1ea854d-c66a-4514-9070-2330672b481a.png">

Based on the classification report, the accuracy of The Gated Recurrent Unit (GRU) Model was 1.00%, it means that almost 100% of tweets were classified correctly. It is crucial to note again that the high accuracy result was reached on the ideal data with a large number of fake and real tweets. The Gated Recurrent Unit (GRU) Model performed with ideal/perfect accuracy, and the other metrics (Precision, Recall, and F-1 Score) showed the same result. As it was mentioned for Long Short-Term Memory (LSTM) Model, the perfect prediction accuracy has been made possible by a number of crucial aspects, including the vast quantity of data that was used to train the model and the ideal data distribution.
