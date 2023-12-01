# Semi-supervision-aerial-images
Step1: The pretrained I2M and M2I subcomponents are trained on the labelled training set. 
Step2:(a)Unlabelled images fed to the trained I2M generates their soft-masks,
      (b) the trained M2I with predicted soft-masks as input reconstructs the original unlabelled images, 
      (c) the reconstructed and original unlabelled images are compared, 
      (d) if the similarity score between them is above a threshold, the corresponding original unlabelled image and its predicted soft-mask is considered most-confident image-mask pair, 
      (e) the set of most-confident image-mask pair and original labelled training set is used to retrain I2M
To execute the code:
  Execute I2M.ipynb to get the predicted masks of the unlabelled images
  Execute M2I.ipynb to get the reconstructed images of unlabelled images from the predicted masks, check the reconstruction score, and get the 'most-confident' image -mask pair and add it to the      original labelled set to get an enhanced training set.
  Execute I2M.ipynb to train the segmentation model with the enhanced set.
