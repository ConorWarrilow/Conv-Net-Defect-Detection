# Conv Net Defect Detection

Just a quick notebook from a while ago using a CNN to detect defects in an industrial component.

We had 6633 images in the training dataset of which 3758 were defective, and 715 images in the test dataset of which 453 were defective. 

Example images can be seen below:
<br/>
<img width="100" alt="image" src="https://github.com/ConorWarrilow/Conv-Net-Defect-Detection/assets/152389538/17f2c9fe-5276-416b-ae36-62b97abd2047">

<br/>
<br/><br/><br/><br/><br/><br/>
I ended up using a relatively simple model, importing a pretrained model wasn't necessary.
<br/><br/><br/>

<br/>

Augmentation was used on the training data which improved classification accuracy on the test set considerably.
<br/>

We had 6633 images in the training dataset of which 3758 were defective, and 715 images in the test dataset of which 453 were defective. 
<br/>
Example images can be seen below:
<br/>
<img width="396" alt="image" src="https://github.com/ConorWarrilow/Conv-Net-Defect-Detection/assets/152389538/17f2c9fe-5276-416b-ae36-62b97abd2047">

<br/>


<div align="center">
	<img width = "400" src="https://github.com/ConorWarrilow/Conv-Net-Defect-Detection/assets/152389538/17f2c9fe-5276-416b-ae36-62b97abd2047">
</div>




I ended up using a relatively simple model, importing a pretrained model wasn't necessary.
<br/>
<img width="551" alt="image" src="https://github.com/ConorWarrilow/Conv-Net-Defect-Detection/assets/152389538/551b5721-026b-4b1c-b66f-f5db626cfe9e">
<br/>
By around 30 epochs the model was able to consistently acheive 100% accuracy.

<br/>
<div align="center">
	<img width = "400" src="https://github.com/ConorWarrilow/Conv-Net-Defect-Detection/assets/152389538/c3ec4391-6673-4e04-80ee-aa9d775e47ba">
</div>
<br/>
2875  train pass

2875   3758   262   453 

<img width="906" alt="Screenshot 2024-06-16 161652" src="https://github.com/ConorWarrilow/Conv-Net-Defect-Detection/assets/152389538/c3ec4391-6673-4e04-80ee-aa9d775e47ba">


The components without defects are free of imperfections:

<img width="300" alt="Screenshot 2024-06-16 161652" src="https://github.com/ConorWarrilow/Conv-Net-Defect-Detection/assets/152389538/4ad17cc3-ad20-49f3-91e0-2a774b2abb48">

<img width="300" alt="Screenshot 2024-06-16 161652" src="https://github.com/ConorWarrilow/Conv-Net-Defect-Detection/assets/152389538/d630dbc1-9cf0-4231-a356-0705d884c6a3">

![pass4](https://github.com/ConorWarrilow/Conv-Net-Defect-Detection/assets/152389538/d630dbc1-9cf0-4231-a356-0705d884c6a3)
![pass1](https://github.com/ConorWarrilow/Conv-Net-Defect-Detection/assets/152389538/0890fe33-aefd-48fb-9ea8-0f7043fe66b1)








While some defective components are easy to spot:

![defect1](https://github.com/ConorWarrilow/Conv-Net-Defect-Detection/assets/152389538/6965dc54-89be-479c-a2ee-2415221573e8)
![defect9](https://github.com/ConorWarrilow/Conv-Net-Defect-Detection/assets/152389538/0fbd7afe-84b9-4a7e-9b68-d1908e541875)

Some are a little less obvious:
![defect3](https://github.com/ConorWarrilow/Conv-Net-Defect-Detection/assets/152389538/912381e4-bbf4-4b0a-b374-a2085fba24ad)
![defect11](https://github.com/ConorWarrilow/Conv-Net-Defect-Detection/assets/152389538/ab4a3162-ae18-4cab-a2fd-943c3febb7a6)
![defect12](https://github.com/ConorWarrilow/Conv-Net-Defect-Detection/assets/152389538/fe922346-3602-4221-8933-7626e25d0e8a)




