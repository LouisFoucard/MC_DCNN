# MC_DCNN
## Multi channel deep convolutional neural network for time series classification.

MC-DCNN (http://staff.ustc.edu.cn/~cheneh/paper_pdf/2014/Yi-Zheng-WAIM2014.pdf) architecture.  

With the MC-DCNN architecture, features are first learned idependently on each channel with a
cascade of 1D convolutions and maxpooling, then the learned features are concatenated and fed into a MLP. 
The MLP is in charge of learning the correlations between channels and classification.

