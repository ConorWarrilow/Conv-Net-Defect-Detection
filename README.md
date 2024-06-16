# Conv Net Defect Detection
<div align="center">
	<img width = "400" src="">
</div>

The aim of this notebook was to detect defects in industrial castings.


The data consisted of 6633 training images of which 3758 were defective, and 715 test images with 453 defective.
<br/>
The components without defects are seen to be entirely free of imperfections:
<div style="display: flex; justify-content: center; gap: 10px;">
  <img width="300" src="https://github.com/ConorWarrilow/Conv-Net-Defect-Detection/assets/152389538/4ad17cc3-ad20-49f3-91e0-2a774b2abb48" alt="Description of image 1">
  <img width="300" src="https://github.com/ConorWarrilow/Conv-Net-Defect-Detection/assets/152389538/d630dbc1-9cf0-4231-a356-0705d884c6a3" alt="Description of image 2">
  <img width="300" src="https://github.com/ConorWarrilow/Conv-Net-Defect-Detection/assets/152389538/d630dbc1-9cf0-4231-a356-0705d884c6a3" alt="Description of image 3">
</div>
<br/>

While some defective components are incredibly easy to spot:
<div style="display: flex; justify-content: center; gap: 10px; flex-wrap: wrap;">
  <img width="300" src="https://github.com/ConorWarrilow/Conv-Net-Defect-Detection/assets/152389538/6965dc54-89be-479c-a2ee-2415221573e8" alt="Description of image 4">
  <img width="300" src="https://github.com/ConorWarrilow/Conv-Net-Defect-Detection/assets/152389538/0fbd7afe-84b9-4a7e-9b68-d1908e541875" alt="Description of image 5">
</div>
<br/>

Some are a little less obvious:
<div style="display: flex; justify-content: center; gap: 10px; flex-wrap: wrap;">
  <img width="300" src="https://github.com/ConorWarrilow/Conv-Net-Defect-Detection/assets/152389538/912381e4-bbf4-4b0a-b374-a2085fba24ad" alt="Description of image 4">
  <img width="300" src="https://github.com/ConorWarrilow/Conv-Net-Defect-Detection/assets/152389538/ab4a3162-ae18-4cab-a2fd-943c3febb7a6" alt="Description of image 5">
  <img width="300" src="https://github.com/ConorWarrilow/Conv-Net-Defect-Detection/assets/152389538/fe922346-3602-4221-8933-7626e25d0e8a" alt="Description of image 6">
</div>
<br/>


With some being quite difficult if not questionable:
<div style="display: flex; justify-content: center; gap: 10px; flex-wrap: wrap;">
  <img width="300" src="https://github.com/ConorWarrilow/Conv-Net-Defect-Detection/assets/152389538/cc0cf600-a1af-43df-b21e-25092e1c68f2" alt="Description of image 4">
  <img width="300" src="https://github.com/ConorWarrilow/Conv-Net-Defect-Detection/assets/152389538/95d68943-6d73-4839-92fe-5e58adb2eae5" alt="Description of image 5">
</div>
<br/>

I ended up using a relatively simple CNN architecture, and with the data set being small the training time was extremely quick.
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


By around 30 epochs the model was able to consistently acheive 100% accuracy on the test set.
<br/>

<div align="center">
	<img width = "800" src="https://github.com/ConorWarrilow/Conv-Net-Defect-Detection/assets/152389538/551b5721-026b-4b1c-b66f-f5db626cfe9e">
</div>

<br/>

<div align="center">
	<img width = "800" src="https://github.com/ConorWarrilow/Conv-Net-Defect-Detection/assets/152389538/c3ec4391-6673-4e04-80ee-aa9d775e47ba">
</div>


















