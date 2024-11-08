# Skin Cancer Detection Project

## Project Overview
This project aims to develop a machine learning model that can classify skin lesions as benign (non-cancerous) or malignant (cancerous). The model uses a hybrid approach, incorporating both skin lesion images and tabular patient data, to provide healthcare professionals with a supportive tool for early skin cancer detection and diagnosis.

## Data and Methods
The project utilizes a dataset containing skin lesion images and associated tabular patient data, including risk factors. The data is preprocessed by:
1. Resizing and centering the images, and removing unwanted features like hair.
2. Normalizing the tabular data using the training set's mean and standard deviation.
3. Addressing class imbalance by undersampling the majority (benign) class.

The model architecture follows a hybrid design, using a pre-trained DenseNet121 model for feature extraction from the images, and a fully connected network for the tabular data. The combined features are then fed into the final classification layer.

The model is trained using PyTorch, with Focal Loss to handle the class imbalance, and the AdamW optimizer with learning rate scheduling. Early stopping is implemented to prevent overfitting.

## Results
The model achieves a ROC-AUC score of 0.92 on the validation set and 0.90 on the tes
## Future Improvements
Potential future improvements to the project include:
- Exploring alternative model architectures or ensemble methods to further enhance performance.
- Incorporating additional data sources, such as clinical history or dermoscopic images, to improve the model's predictive capabilities.
- Evaluating the model's performance on larger and more diverse datasets to ensure real-world applicability.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.
