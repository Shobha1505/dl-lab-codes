This document summarizes the key differences between the ORIGINAL codes and their UPDATED versions across 5 Deep Learning and Reinforcement Learning implementations.


 
1. AlexNet (CNN – Image Classification)
Original Code:
- Used incorrect constructor (_init_ instead of __init__)
- No Batch Normalization
- No regularization
- Very large fully connected layers (4096, 4096)
- Designed strictly for ImageNet (1000 classes)

Updated Code:
- Fixed constructor (__init__)
- Added Batch Normalization layers
- Added L2 regularization
- Reduced fully connected layer sizes (2048, 1024)
- Flexible number of output classes
- Faster training and reduced overfitting

Impact:
- Improved training stability
- Reduced model size
- Better generalization
- Different model summary and output behavior

 
2. Q-Learning on Graph (Shortest Path / Environment Aware)
Original Code:
- No learning rate (α)
- No ε-greedy exploration
- Action sampling bug (used global variable)
- Limited environment influence (police/drugs weakly used)
- Static behavior with repeated paths

Updated Code:
- Added learning rate (α)
- Added ε-greedy strategy
- Fixed action sampling bug
- Increased discount factor (γ)
- Strong environment-aware path filtering
- Cleaner reward matrix design

Impact:
- Different learned paths
- More realistic agent behavior
- Improved convergence
- Different reward curves and outputs


3. Character-Level RNN Text Generation
Original Code:
- Used SimpleRNN
- Used one-hot encoding
- Used argmax for prediction
- Limited creativity
- Output was repetitive and deterministic

Updated Code:
- Replaced SimpleRNN with LSTM
- Added Embedding layer
- Used sparse categorical loss
- Introduced temperature-based sampling
- Increased training epochs

Impact:
- More fluent text generation
- Higher variation in output
- Different text generated every run
- Better sequence learning

 
4. Tic-Tac-Toe Reinforcement Learning
Original Code:
- Bug in playerSymbol initialization
- Weak reward structure
- Slower learning rate
- High exploration randomness
- Less strategic gameplay

Updated Code:
- Fixed initialization bug
- Improved reward policy (win/loss/draw)
- Increased learning rate and discount factor
- Reduced exploration
- Cleaner winner logic
- Stronger and faster-learning AI

Impact:
- AI plays more optimally
- Fewer draws
- Different gameplay outcomes
- Faster convergence during training

 
5. LSTM Time-Series Forecasting (Airline Passengers)
Original Code:
- Single LSTM layer
- Time step = 10
- Batch size = 1
- Limited seasonal modeling
- Higher RMSE

Updated Code:
- Two LSTM layers with Dropout
- Time step increased to 12 (seasonality)
- Increased epochs and batch size
- Cleaner dataset creation function
- Improved input reshaping

Impact:
- Smoother prediction curves
- Lower RMSE
- Better seasonal trend capture
- Improved generalization

Colab notebook:
https://colab.research.google.com/drive/1N_FNFJENcAS2abniKsXPS8E7eZaCLhoz?usp=sharing
