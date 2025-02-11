# $${\color{#4D918F}\text{Convolutional Neural Network} \space \color{#4D918F}\text{Defect Detection} \space \color{#00D8DB}\text{}}$$

The aim of this project was to automate the process of detecting defects in industrial castings through the use of convolutional neural networks, a type of deep neural networks commonly applied to images.

# $${\color{#E3804B}\text{Results}}$$

Through the use of augmentation techniques and an optimized model design, I was able to consistently achieve 100% classification accuracy on the dataset.

In addition, I was able to achieve this with an efficient self-designed CNN architecture containing only 5 convolutional layers and two dense layers. To compare, a small pretrained model can easily have up to 16-20 layers. Participants could be seen using popular pretrained models such as VGG16, while still recieving unsatisfactory results, as can be seen [here](https://www.kaggle.com/code/siddheshdandagavhal/impeller-casting-defect-detection). Other participants took the opposite route, creating shallow models that were unable to capture small details, while remaining inefficient due to the lack of pooling layers, as can be seen [here](https://www.kaggle.com/code/jominjae/casting-image-classification).

By having an optimized model design, the training time was incredibly short. Not only does the model's efficiency save on time, but it would allow for the use of higher resolution images, which would further ensure the model's performance on small defects.



# $${\color{#4D918F}\text{The Dataset}}$$
This dataset was sourced from kaggle and can be found [here.](https://www.kaggle.com/datasets/ravirajsinh45/real-life-industrial-dataset-of-casting-product/data)

The data consisted of 6633 training images of which 3758 were defective, and 715 test images where 453 were defective.

The class imbalance is small and unlikely to be problematic.



# $${\color{#4D918F}\text{Components} \space \color{#4D918F}\text{Without Defects} \space \color{#00D8DB}\text{}}$$
The components without defects are seen to be entirely free of imperfections:
<div style="display: flex; justify-content: center; gap: 10px;">
  <img width="300" src="https://github.com/ConorWarrilow/Conv-Net-Defect-Detection/assets/152389538/4ad17cc3-ad20-49f3-91e0-2a774b2abb48" alt="Description of image 1">
  <img width="300" src="https://github.com/ConorWarrilow/Conv-Net-Defect-Detection/assets/152389538/d630dbc1-9cf0-4231-a356-0705d884c6a3" alt="Description of image 2">
  <img width="300" src="https://github.com/ConorWarrilow/Conv-Net-Defect-Detection/assets/152389538/d630dbc1-9cf0-4231-a356-0705d884c6a3" alt="Description of image 3">
</div>
<br/>




# $${\color{#4D918F}\text{Components} \space \color{#4D918F}\text{With Defects} \space \color{#00D8DB}\text{}}$$
Some defective components are incredibly easy to spot, and its no question as to whether they're defective.

<div style="display: flex; justify-content: center; gap: 10px; flex-wrap: wrap;">
  <img width="300" src="https://github.com/ConorWarrilow/Conv-Net-Defect-Detection/assets/152389538/6965dc54-89be-479c-a2ee-2415221573e8" alt="Description of image 4">
  <img width="300" src="https://github.com/ConorWarrilow/Conv-Net-Defect-Detection/assets/152389538/0fbd7afe-84b9-4a7e-9b68-d1908e541875" alt="Description of image 5">
</div>
<br/>

Some of the defects are a little less obvious:
<div style="display: flex; justify-content: center; gap: 10px; flex-wrap: wrap;">
  <img width="300" src="https://github.com/ConorWarrilow/Conv-Net-Defect-Detection/assets/152389538/912381e4-bbf4-4b0a-b374-a2085fba24ad" alt="Description of image 4">
  <img width="300" src="https://github.com/ConorWarrilow/Conv-Net-Defect-Detection/assets/152389538/ab4a3162-ae18-4cab-a2fd-943c3febb7a6" alt="Description of image 5">
  <img width="300" src="https://github.com/ConorWarrilow/Conv-Net-Defect-Detection/assets/152389538/fe922346-3602-4221-8933-7626e25d0e8a" alt="Description of image 6">
</div>
<br/>


Lastly, some of the defects are quite difficult to spot with the naked eye and would require close inspection to catch.
<div style="display: flex; justify-content: center; gap: 10px; flex-wrap: wrap;">
  <img width="300" src="https://github.com/ConorWarrilow/Conv-Net-Defect-Detection/assets/152389538/cc0cf600-a1af-43df-b21e-25092e1c68f2" alt="Description of image 4">
  <img width="300" src="https://github.com/ConorWarrilow/Conv-Net-Defect-Detection/assets/152389538/95d68943-6d73-4839-92fe-5e58adb2eae5" alt="Description of image 5">
</div>
<br/>

# $${\color{#4D918F}\text{CNN Architecture} \space \color{#4D918F}\text{} \space \color{#00D8DB}\text{}}$$
<details>
  <summary>$${\color{#72B3A2}\text{What's a CNN?}}$$</summary>

A Convolutional Neural Network (CNN) is a type of artificial neural network primarily used for analyzing visual data, such as images and videos. It’s particularly effective for tasks like image recognition, object detection, and image classification. CNNs use what are called 'convolutional layers', where we can imagine them as taking dozens of cropped screenshots of the image to extract specific patterns and recognize what these patterns mean. Once our model is trained on every image, our model will classify a new image based on its patterns, and classify it to fall in the most similar group.
</details>

I ended up using a relatively simple CNN architecture, and with the data set being small the training time was extremely quick. The model consists of five 3x3 kernel Convolutional layers (64 -> 64 -> 128 -> 128 -> 64), each with 2x2 maxpool layers, bringing the images down from 224x224 to 7x7. It then finishes with two FC layers (3136 and 1568 nodes). Neither batch normalization or dropout layers were found to be necessary and weren't included in the final model.
<br/>

Augmentation was used on the training data which improved classification accuracy on the test set considerably. As lighting, contrast and exposure affect the quality and consistency of the images, I chose color jitter as my main augmentation. 
Augmentation image examples can be seen below:
<br/>
<div align="center">
	<img width = "400" src="https://github.com/ConorWarrilow/Conv-Net-Defect-Detection/assets/152389538/17f2c9fe-5276-416b-ae36-62b97abd2047">
</div>

<div align="center">
	<img width = "400" src="https://github.com/ConorWarrilow/Conv-Net-Defect-Detection/assets/152389538/b02ad66e-2796-4829-9cbb-2ae3f260f4d7">
</div>

<br/>

By around 30 epochs the model was able to consistently acheive 100% accuracy on the test set.

<br/>

<div align="center">
	<img width = "800" src="https://github.com/ConorWarrilow/Conv-Net-Defect-Detection/assets/152389538/551b5721-026b-4b1c-b66f-f5db626cfe9e">
</div>

<br/>

<div align="center">
	<img width = "800" src="https://github.com/ConorWarrilow/Conv-Net-Defect-Detection/assets/152389538/c3ec4391-6673-4e04-80ee-aa9d775e47ba">
</div>
<br/>
<br/>

# $${\color{#4D918F}\text{Conclusion} \space \color{#4D918F}\text{} \space \color{#00D8DB}\text{}}$$
In the business context, such a model would make the process of defect detection incredibly efficient, saving time and money. The model is able to detect even the smallest of defects with perfect accuracy. The size of the training dataset could also be increased over time, further ensuring the model's robustness.
















