# AlexNet

  **Problem**: Image recognition is difficult. Before this paper, it proved to be computationally expensive and prone to overfitting. In order to train many images, the model must possess a large learning capacity and adequate prior knowledge.

  **Solution**: Convolutional neural networks trained on "cheap" GPUs 

  ## Key Ideas

  ### Local Response Normalization

  A method to mimic the lateral inhibition found in real neurons. Basically, it square-normalizes the pixel values in a feature map within a local neighborhood.

  ### ReLU Nonlinearity

  Popular neural network activation functions follow sigmoid or tanh(x) functions. However, these saturating functions train much slower than non-saturating nonlinearities. Rectified Linear Units (ReLUs) train much faster.
  
### Data Augmentation

There were two distinct forms of data augumentation novelly used. First, the images are translated and reflected. This minimizes overfitting.

Second, PCA is performed on RGB pixel values to alter the intensities. 

### Dropout

Dropout refers to setting the output of hidden neurons to zero with a probability of 0.5. This means that during the forward pass, 50% of all activations of the layer were set to zero and also did not participate in backpropagation. During testing, no single neuron is dropped as in the real-time Inference.

## Thoughts
* This paper seems very much involved in "results". Basically, every little increase in accuracy is mentioned.

## Appendix

**saturating nonlinearities** : These functions do not approach infinity as the limit increases

**non-saturating nonlinearities** : These functions do approach infinity as the limit increases

**sigmoid**: $f(x) = (1 + e^{-x})^{-1}$

**tanh**: $f(x) = tanh(x)$

**ReLU**: $f(x) = max(0,x)$

<img src="https://render.githubusercontent.com/render/math?math=e^{i \pi} = -1">