# SkinCancerPredictionModel

•	Model's inputs : jpeg image of the skin lesion of concern and user input for the lesion's age, sex, and location

•	Model output: label of 0 or 1, indicating whether a person has healthy skin or is at the onset of skin cancer. 

•	Model architecture employs :contrast stretching and image augmentation for preprocessing, feature extraction using parallel MobileNetV2 and DenseNet201 CNNs, a classification head with Global Average Pooling, batch normalization, and dense layers concludes the process by offering binary detection of skin cancer and  Grad-CAM visualization for model interpretability
