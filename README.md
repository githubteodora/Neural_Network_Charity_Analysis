# Neural_Network_Charity_Analysis

## Overview of the analysis<br>
The purpose of this project is to create a binary classifier that is capable of predicting whether charity applicants will be successful if funded by Alphabet Soup (an imaginary non-profit organization). 
Link to the dataset used for the analysis: [click here](https://github.com/githubteodora/Neural_Network_Charity_Analysis/blob/main/charity_data.csv)

## Tools
 - Python 3
 - Sklearn
 - Tensorflow
 - Jupyter Notebook

## Results: 

### Data Preprocessing
Variable that is the target(s) for the model: IS_SUCCESSFUL
Variables considered to be the features for the model: all other variables, except for the dropped ones
Variables that are neither targets nor features: EIN, NAME 

### Compiling, Training, and Evaluating the Model
4 attempts were made to come up with a model that produces satisfactory results, but none could exceed 72.8% accuracy. Each attempt used different number of neurons. The following guidelines were used when decided on the number of neurons and layers:

 - Stackoverflow (https://stats.stackexchange.com/questions/181/how-to-choose-the-number-of-hidden-layers-and-nodes-in-a-feedforward-neural-netw): 
"The number of neurons comprising that layer is equal to the number of features (columns) in your data. Some NN configurations add one additional node for a bias term. The situations in which performance improves with a second (or third, etc.) hidden layer are very few. One hidden layer is sufficient for the large majority of problems. <br>
 - Other resources: http://www.faqs.org/faqs/ai-faq/neural-nets/part1/preamble.html
"For most problems, one could probably get decent performance (even without a second optimization step) by setting the hidden layer configuration using just two rules: (i) number of hidden layers equals one; and (ii) the number of neurons in that layer is the mean of the neurons in the input and output layers.<br>
In order to secure the ability of the network to generalize the number of nodes has to be kept as low as possible. If you have a large excess of nodes, you network becomes a memory bank that can recall the training set to perfection, but does not perform well on samples that was not part of the training set."

### Summary
The model's performance is not good enough to proceed to operationalizing it. The following steps can be undertaken to try and imrpove the model:
 - data inspection - there might ne null values in the source;
 - normalization of columns - dirty data might be causing the model to underperform;
