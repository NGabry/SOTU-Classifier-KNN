# Classifying State of The Union Speeches with scikit-learn KNN implementation

Here we use sklearn to preform K Nearest Neighbor classification of text chunks in order to determine the orator of the speech the text was taken from. 

In this instance, the speeches we are pulling text from are State of the Union Addresses given between 1993 and 2019, meaning that we have 4 potential classifications:
1. George W. Bush
2. Bill Clinton
3. Barack Obabma 
or 
4. Donald Trump

Transcripts of these speeches are avaialble at [govinfo.com](https://www.govinfo.gov/features/state-of-the-union)

In this repo there are three jupyter-notebooks. 
### setup.ipynb
In this notebook we walk through the steps from reading in the raw speech data, chunk the text into blocks of 100 words, and exporting each chunk into a labeled data frame

### sklearn_knn.ipynb
This notebook contains the full process of reading in the newly created data all the way through to training a KNN model and classifying a test set of speech chunks.
This initial model implementation of the k nearest neighbors algorithm uses vectorized text chunks of 100 words, where a word constitutes any thing 5 letters or longer.

Ultimately we aer able to classify our test set of speeches with an average accuracy of 61.42% when our K value is optimized.

![alt text](https://github.com/NGabry/SOTU-Classifier-KNN/blob/main/figs/first_k_val_plot.png?raw=true)

### FULL_MODEL.ipynb    
Here we condense the previous two notebooks into a single notebook to allow for easier exploration into how altering our data input can result in better classification accuracy. By tweaking two major input parameters (word chunks size, and word letter size), we are abel to get our model up to 100% classification accuracy!

![alt text](https://github.com/NGabry/SOTU-Classifier-KNN/blob/main/figs/k_val_plot_5_500.png?raw=true)

This notebook allows for easy exploration how these two paramters change calssification accuracy by allowing you to set the two variables to any value in the second cell.
