## Visualisation of Convolutional Neural Network Decision Marking via Gradient-weighted Class Activation Mapping (Grad CAM)

Original paper:https://arxiv.org/abs/1610.02391  
Site: http://gradcam.cloudcv.org/  
Guide: https://github.com/fchollet/deep-learning-with-python-notebooks/blob/master/5.4-visualizing-what-convnets-learn.ipynb  

This project was inspired by seeking to build trust in using neural networks/AI by being able to understand how neural networks come to their decision. The aim was to be able to visualise what the CNN was 'looking at' when it came to it's decision.   

The model was trained on images from Kaggle (https://www.kaggle.com/iarunava/cell-images-for-detecting-malaria) and Grad CAM was applied to highlight the areas that led to the model's decision of the cell being infected. This would help build trust as one would be able to have an idea of how the model came to its decision. In addition, it could potentially speed up second opinions by enabling a professional to quickly zoom in on what the model picked up, rather than having to scan the entire image wondering why triggered the model.
