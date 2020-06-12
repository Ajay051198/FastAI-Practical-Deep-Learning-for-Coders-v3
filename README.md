# FastAI LOG

Date: Jun 10, 2020
bout': Observations

## I am logging my learning progression with the FASTAI module which is built on top of PyTorch

---

Jun 10, 2020 

- DOG/CAT breed → 97% accuracy  with minimal training
- An systematic approach to create custom Image classification datasets from Google Images
- CIFAR10 → 95% accuracy with minimal training
- CIFAR100 →  ~ 90% accuracy
- CAMVID Image Segmentation → 95% accuracy

---

Jun 11, 2020 

- (NLP) IMDB Sentiment Analysis → 94.4% accuracy [Training language model on custom sentences corpus followed by training a classifier instantiated with the language model's encoder]
- Tabular data → 87% accuracy
- Collaborative filtering ideology: 
It works with embeddings. for example for a movie recommnedation system. Consider a 1D vector of 5 numbers representing a user and a 1D vector of 5 number representing a movie. 
- when you Matrix multiply the two vectors you get a number, this should be the rating given to the movie by the user. Simarly you can compare all the rating given by multiple users to different movies. and the loss would be the sum of all the differences between the true ratings and the ratings calculated by multipliing the two vectors. By minimizing the loss. The model learns genres and types of people by itself.
- Notes on Overfitting and Underfitting
    - If training loss > validation loss → you are under fitting
    - if validation loss > training loss → does not mean you are overfitting (because of training stratergy)
    - You are overfitting only when you see a sustained degradation of evaluation metric on the validation set
- Weight decay → Prevents the weights from growing too big and makes the model more linear thus preventing overfitting. (Tip: lambda (wd factor, wd in FASTAI = 0.1 or "default 0.01"  almost works every time)
- [Platform.ai](http://platform.ai) → Useful for Labelling images
- A function to show data augmented images in FastAI

    ```python
    def _plot(i,j,ax):
    	x,y = data.train_ds[3]
    	x.show(ax, y=y)

    plot_multi(_plot, 3, 3, figsize=(8,8))
    ```

---

Jun 12, 2020 

- Rewatch lecture 7, superres Gan , Superres

[https://youtu.be/9spwoDYwW_I](https://youtu.be/9spwoDYwW_I)