In our group project, we are developing a platformer video game that blends reality with the virtual world. The gameplay involves capturing photos of birds in real life, which are then scored based on the rarity of the bird species identified in the images.

My Role :

1) Classification Model Development and Training

- Objective :  Develop a model to accurately identify bird species from images.
- Model Choice : I utilized the InceptionV3 model as the base architecture. This pre-trained model provides a strong foundation for our task due to its advanced feature extraction capabilities.
- Implementation Details : I froze the parameters of the InceptionV3 model to leverage its pre-trained weights and avoid retraining the entire network. I then appended custom layers on top of the InceptionV3 model tailored to our specific dataset. This approach allows the model to adapt to our bird species classification task while maintaining the robustness of the original feature extractor.

2) Preprocessing Image 

- Objective : Define a function that accurately detects birds in images or tells us if there are birds to consider or not.
- Model Choice : I utilized the YOLO model. 
- Implementation Details : YOLO detects objects in images. I take the biggest detected bird as the output. If the precision is inferior to 0.3 I return a message
asking the user to take another picture.
