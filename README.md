# Conv Net Defect Detection

Just a quick notebook from a while ago using a CNN to detect defects in an industrial component.

We had 6633 images in the training dataset of which 3758 were defective, and 715 images in the test dataset of which 453 were defective. 

Example images can be seen below:

<img width="396" alt="image" src="https://github.com/ConorWarrilow/Conv-Net-Defect-Detection/assets/152389538/17f2c9fe-5276-416b-ae36-62b97abd2047">



I ended up using a relatively simple model, importing a pretrained model wasn't necessary.




Augmentation was used on the training data which improved classification accuracy on the test set considerably.


We had 6633 images in the training dataset of which 3758 were defective, and 715 images in the test dataset of which 453 were defective. 

Example images can be seen below:
<img width="396" alt="image" src="https://github.com/ConorWarrilow/Conv-Net-Defect-Detection/assets/152389538/17f2c9fe-5276-416b-ae36-62b97abd2047">




I ended up using a relatively simple model, importing a pretrained model wasn't necessary.

<img width="551" alt="image" src="https://github.com/ConorWarrilow/Conv-Net-Defect-Detection/assets/152389538/551b5721-026b-4b1c-b66f-f5db626cfe9e">

By around 30 epochs the model was able to consistently acheive 100% accuracy.




2875  train pass

2875   3758   262   453 
