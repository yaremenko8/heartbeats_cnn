# A deep CNN to classify heartbeats by Team 26
#### Contributors: Emmanuel Akeweje, Grigory Yaremenko, Suparat Srifa, Yatipa Chaleenutthawut

## Goals:
* Reproduce the results of [this paper](https://www.sciencedirect.com/science/article/pii/S0010482517302810?via%3Dihu) that describes a successful attempt at classifying types of cardiovascular abnormalities by corresponding ECG readings via a 1-dimensional CNN.
* Produce a decent non-DL benchmark, so that results achieved by manual feature engineering and model selection could be compared against results produced by a CNN.
* Try to further improve the performance of the aforementioned CNN by creating a CNN-LSTM hybrid based on the original (purely CNN) model.

## How to reproduce our results:
1. Makes sure your tensorflow backend runs on CPU.
2. Make sure you're using Python 3.7 or follow instructions below to reproduce our results in Google Colab.
    1. Clone the repository.
    2. Open [this link](https://colab.research.google.com/github/yaremenko8/heartbeats_cnn/blob/main/heartbeats%20cnn.ipynb).
    3. Create `beats` folder in the current directory (in Google Colab).
    4. Upload the contents of `beats` from the repository you just cloned to `beats` that you've just created in Colab.
3. Open `heartbeats cnn.ipynb`.
4. Run cells in their intended order.

## Results summary:
* Non-DL approach yielded 76% balanced accuracy with a featureset that comprises a downsampled version of the ECG readings and a segment of its power spectrum.
* CNN improved this result all the way to 89%, thus reducing average misclassification frequency by over 50%.
* The novel CNN-LSTM hybrid model yielded a mean recall (balanced accuracy) of 92%, thereby reducing average misclassification frequency by further 23%.
