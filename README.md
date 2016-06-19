# MC-DCNN
## Multi Channel-Deep Convolutional Neural Network for time series classification.

MC-DCNN (http://staff.ustc.edu.cn/~cheneh/paper_pdf/2014/Yi-Zheng-WAIM2014.pdf) architecture, implemented with lasagne/theano. 

With the MC-DCNN architecture, features are first learned idependently on each time series channel with a
cascade of 1D convolutions and maxpooling, then the learned features are concatenated and fed into a MLP. 
The MLP is in charge of learning the correlations between channels and classification.

MC-DCNN architecture:

![alt tag](https://github.com/LouisFoucard/MC_DCNN/blob/master/architecture.png)

Here we train the MC-DCNN on a dataset of biometric data (ppg + accelerometer data time series), recorded over one month for 10 users. The MC-DCNN is trained to recoginze user ID based on its biometric data.
We achieve a classification F1 score of 0.96+.

MC-DCNN also remove the need for engineering features such as spectrogram or fft: the convolutional and pooling layers are able to learn time and frequency domain features at different time scales. The input data is only slightly preprocessed, with smoothing and scaling.

Below is the train/test error from CV:

![alt tag](https://github.com/LouisFoucard/MC_DCNN/blob/master/CV.png)
