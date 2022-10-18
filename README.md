# Football_Image_Classification
## Classification Football's match frame to one of the 7th match views: aerial view, side view, non match, close up, front view, wide view, side gate view 
This is a project which labels a particular football match with a point of view.
Project involves:
* Data Operations
> Spliting samples into proper directories based on thier labeling

> Creating samples based on data augmentations using Augmentator library, it was used to balance the dataset

> Spliting finall dataset into train and validation sets

* Defining a function which creates Dataset object and Dataloader in order to inject model with samples
* Defining a callback class which is responsible for stopping training after not getting better validation score
* Defining a class which conist of:
> Initialization configuration data

> Loading a model: already trained ResNet50 using a transfer learnining with a last layers modification

> Performing data loading, achieving prediction result and its validation. Since the dataset is now balanced (each class has same num. of samples)
validation was performed based on accuraccy metrics.

> Creating a training and validation pipeline

* Testing achieved results by:
> Creating test dataset class and test dataset loader

> Loading model state

> Making prediction on a Test Dataset

> Saving predictions to a .csv file
