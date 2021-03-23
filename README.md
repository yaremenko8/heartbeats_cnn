# A deep CNN to classify heartbeats by Team 26
#### Contributors: Emmanuel Akeweje, Grigory Yaremenko, Suparat Srifa, Yatipa Chaleenutthawut

## Goals:
* Reproduce the results of [this paper](https://www.sciencedirect.com/science/article/pii/S0010482517302810?via%3Dihu) that describes a successful attempt at classifying types of cardiovascular abnormalities by corresponding ECG readings via a 1-dimensional CNN.
* Produce a decent non-DL benchmark, so that results achieved by manual feature engineering and model selection could be compared against results produced by a CNN.
* Try to further improve the performance of the aforementioned CNN by creating a CNN-LSTM hybrid based on the original (purely CNN) model.

## How to reproduce our results:
1. Open `heartbeats cnn.ipynb`.
2. Run cells in their intended order.

## Results summary:
* Non-DL approach yielded 76% balanced accuracy with a featureset that comprises a downsampled version of the ECG readings and a segment of its power spectrum.
* CNN improved this result all the way to 89%, thus reducing average misclassification frequency by over 50%.
* The novel CNN-LSTM hybrid model yielded a mean recall (balanced accuracy) of 92%, thereby reducing average misclassification frequency by further 23%.
