# Wildlife_Species_Identification
This project uses a Convolutional Neural Network (CNN) to identify wildlife species from images. The model is trained on a dataset of 10 species, including lions, deer, eagles, and more. It can classify an input image into one of the predefined species with high accuracy.

The project is implemented using PyTorch, a popular deep learning framework, and includes scripts for training the model, making predictions, and visualizing results.
# Features
**Image Classification**: Classifies images into 10 wildlife species.

**Pre-Trained Model**: Uses a pre-trained ResNet18 model for transfer learning.

**Training Script**: Allows you to train the model on your own dataset.

**Prediction Script**: Predicts the species of a given image.

**Visualization**: Displays the input image along with the predicted species.

**CSV Export**: Saves predictions along with image paths and base64-encoded images (optional).
# Installation
**Clone the repository**:
  git clone https://github.com/SHASHANK-SM/Wildlife_Species_Identification.git
**Navigate to the project directory**:
  cd wildlife-species-identification
**Install the required dependencies**:
  pip install -r requirements.txt
# Training the Model
Place your dataset in the data/ folder with the following structure:
```wildlife-species-identification/
├── data/                  # Folder for dataset (optional, if not too large)
├── models/                # Folder for saved models
│   └── wildlife_best_model.pth
├── scripts/               # Folder for scripts
│   ├── train.py           # Training script
│   ├── predict.py         # Prediction script
│   ├── predict_batch.py   # Batch prediction script
│   └── utils.py           # Utility functions
├── requirements.txt       # List of dependencies
├── README.md              # Project documentation
├── .gitignore             # Files/folders to ignore in Git
└── LICENSE                # License file
```
# Run the training script
python scripts/train.py
# Dataset
Get the Datasets from Kaggle or Hugging face.
# Model Architecture
The project uses a ResNet18 model pre-trained on ImageNet. The final layer is modified to output 10 classes (one for each species). The model is fine-tuned on the wildlife species dataset.

**Training Details**
Loss Function: Cross-Entropy Loss

Optimizer: Adam

Learning Rate: 0.001

Epochs: 10

Batch Size: 32
