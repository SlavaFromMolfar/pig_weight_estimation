## 1. Please demonstrate data exploration (is the data evenly distributed ? is it important?)
Answer:
The distribution of target variables is close to normal, which may lead to a over-estimation of small swine, and to an under-estimation of heavy pigs. However If we think the data generating process is truly linear, then imbalance doesn’t matter. Of course, this is rarely the case. If your sampling isn’t representative of the population (or the distribution of interest), then the easiest thing to do is just perform weighted least squares. SMUTE-algos (over-sampling) or assign weight for each sample can be used to improve result.
## 2. A method to predict weight from labeled image ( assuming there are <50 pigs weighted in different days, what are the challenges how do you avoid over-fitting)
Answer:
The structural features of the segments of the segmented images are used to describe the images. To predict the weight, it is proposed to construct a multilayer regression neural model. Multi-layer should ensure the extraction of more complex features and the identification of non-linear patterns. To avoid over-fitting can be used : 
* various techniques of regularization; 
* adjustment of hyperparameters based on cross-validation results; 
* early stoping; 
* to increase the feature informativeness using various techniques of representation learning (PCA, ICA, NMS, Sparse coding, Autoencoder and etc) & semi-supervised learning | transfer learning | learning to learn ...
## 3. Suggest and implement a network for weight prediction, What is the network used? why did you choose this structure how would you further improve it if you had more time additional data?
Answer:
The formed datatset is characterized by low dimensionality of data and limited amount of training samples, which makes it difficult to obtain the benefits of the use of modern techniques of deep learning. It is proposed to use the GMDH neural network (Group Method of Data Handling). This method contains mechanisms of fully automatic structural and parametric optimization and avoid overfitting.
