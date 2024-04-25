![image](https://github.com/oridarshan/Deep-Learning-Genre-Classification/assets/89981387/b71efe1e-2c12-4919-bb45-6407835e4f31)![image](https://github.com/oridarshan/Deep-Learning-Genre-Classification/assets/89981387/1d3a33eb-b1b2-4df0-8e5f-826e487c5fd7)# Spotify-Genre-Classification

We worked about Spotify music dataset which can be found [here](https://www.kaggle.com/datasets/maharshipandya/-spotify-tracks-dataset/data)
Our idea is to use RNN technique with LSTM units and Feed-Forward networkd with droput layers.

## 1. Naive attempt

Before training complex models, we trained and tested basic softmax and also MLP networks with 4 layers to get results to compete with (and also to understand the difficulty of the database):
![image](https://github.com/oridarshan/Deep-Learning-Genre-Classification/assets/89981387/676dbcfb-fd5b-4ab9-bb77-39ad43e4ae37)

![image](https://github.com/oridarshan/Deep-Learning-Genre-Classification/assets/89981387/09b6cd85-f78b-4a07-aed0-4bb02a94f91f)

the softmax and the MLP attempts demonstrated 15% and 25% accuracy each.

## 2. Complex models RNN based

we thought with more complex network we will jump to at least 50% accuracy. 
Training the complex models included four different attempts of LSTM combined and not combined with dropout layers, the best of them is the LSTM network with the dropout layers:
![image](https://github.com/oridarshan/Deep-Learning-Genre-Classification/assets/89981387/6c94a466-d672-4426-b880-b059b3245fcc)
the best network model demonstrates 32% accuracy which is not that good as we thought in first place.

## 3. Analyzing the dataset
After the above attempts, we looked on the confusion matrices (one of them represented below):
![image](https://github.com/oridarshan/Deep-Learning-Genre-Classification/assets/89981387/09237d46-d6b0-4998-b29b-84b8eddf681a)
The errors on the matrix seem to be parallel, this leads us to believe that the main reason for the low accuracy are some interchangeable genres.
Looking at the labels of our dataset we notice many overlapping genres like pop, indie-pop, j-pop, k-pop, mandopop etc.

But in another POV of a probability prespective its not exactly settle down and we explain:
$AMIR TBD

Still, we decided to check this assumption and merged some of the generes, which reduced the 114 generes to 66 generes in total.
Running our best result RNN model:
![image](https://github.com/oridarshan/Deep-Learning-Genre-Classification/assets/89981387/7499af03-6c42-4023-ab56-172068b4d08d)
the accuracy got better to 40% which is still low for our first goal and assumption (crossing the 50% accuracy).


## Summerize
Predicting music tracks genre based on their characteristics turned out to be a difficult task.
Complex models like LSTM did bring better results, however too complex models were hard to train.
Methods that help against overfitting didn’t help because we didn’t manage to interpolate the data.
people that reached better results on kaggle $TBD AMIR










