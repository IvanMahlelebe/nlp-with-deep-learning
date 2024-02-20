# NMT Assignment

Note: Heavily inspired by the https://github.com/pcyin/pytorch_basic_nmt repository

## Introduction

--
In this repo, I go through implementation details of Recurrent Neural Networks(RNNs) in machine translation. Before RNNs,
window-based models were widely adopted, but struggled to capture long-range dependencies, resulting in suboptimal translations due to incomplete context understanding. This repo thus presents how a sequence-to-sequence model with attention
mechanism is used for this task. The adopted approach involves training the system using the following procedure:

- [x] Input a source sequence.
- [x] Compute its embeddings.
- [x] Pass them through a convolutional and bidirection LSTM layers for encoding.
- [x] Initialize the decoder with the final hidden state of the encoder
- [x] Compute Attention Scores and Attention Distribution
- [x] Then finally use a softmax layer to generate the Attention Output

The usual cross-entropy loss function is used to train the network, with parameters being optimized with Adams algorithm. The above training procedure follows illustrated with the figure below:

![model-architecture-image](./images/Assignment%204%20Figure.png)

The overall aim is to develop a comprehensive understanding of the components and training procedure of NMT systems.
