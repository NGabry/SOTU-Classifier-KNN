# Classifying State of The Union Speeches with scikit-learn KNN implementation

Here we use sklearn to preform K Nearest Neighbor classification of text chunks in order to determine the orator of the speech the text was taken from. 

In this instance, the speeches we are pulling text from are State of the Union Addresses given between 1993 and 2019, meaning that we have 4 potential classifications:
1. George W. Bush
2. Bill Clinton
3. Barack Obabma 
or 
4. Donald Trump

Transcripts of these speeches are avaialble at [govinfo.com](https://www.govinfo.gov/features/state-of-the-union)

I have broken this down into to major parts. In part 1 I run through an initial implementation of the k nearest neighbors leanring model on vectorized text chunks of 100 words. Ultimately, this results in a model that doesn't do much better than what we would expect from a random assigner, even after we find the optimal k-value:

![alt text](https://github.com/NGabry/SOTU-Classifier-KNN/blob/main/figs/k_val_plot.png?raw=true)

In part two, we then begin to explore how altering our data input can result in better classification accuracy by testing three major 
