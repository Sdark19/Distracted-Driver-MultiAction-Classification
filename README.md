# Distracted Driver Classification
This project classifies driver actions into 10 distinct classes using a deep learning model based on MobileNetV2.

### Classes
- **c0**: Safe driving  
- **c1**: Texting - right  
- **c2**: Talking on the phone - right  
- **c3**: Texting - left  
- **c4**: Talking on the phone - left  
- **c5**: Operating the radio  
- **c6**: Drinking  
- **c7**: Reaching behind  
- **c8**: Hair and makeup  
- **c9**: Talking to passenger

### Dataset
* Train Folder: Images divided into subfolders based on class (train/c0, train/c1, ...).
* Test Folder: Images in a single folder (test/).
* Metadata: A CSV file (driver_imgs_list.csv) linking subjects, classes, and image names.

### Download Links
The dataset can be downloaded from the following shared drive link:
https://drive.google.com/file/d/1eSwewRiT5wjOZruI0JflutlSEA7GLwN1/view?usp=sharing

### Instructions:

* Download the train, test, and metadata files from the provided links.
* Extract the train and test folders into the Input/ directory.

### Requirements
Install dependencies using:
```bash
pip install -r requirements.txt  
```
### Required Libraries
numpy
pandas
matplotlib
tensorflow
opencv-python
scikit-learn

### How to Run
# Step 1: Clone the Repository
``` bash
git clone https://github.com/yourusername/Distracted-Driver-Classification.git  
cd Distracted-Driver-Classification  
```
# Step 2: Prepare the Dataset
Place the dataset folders and metadata file in the Input/ directory:
```bash
Distracted-Driver-Classification/
└── Input/
    ├── train/               # Training images (10 subfolders for each class)
    ├── test/                # Test images
    └── driver_imgs_list.csv # Metadata file
```
# Step 3: Install Dependencies
```bash
pip install -r requirements.txt  
```
# Step 4: Run the Notebook
Open and execute the distracted_driver.ipynb file using Jupyter Notebook or vs code:

# Step 5: Outputs
After running the notebook, predictions will be saved in the Output/ directory:
``` bash
Distracted-Driver-Classification/
└── Output/
    └── output.csv           # Output file containing predictions
```
### Model Architecture
* Base Model: MobileNetV2 (pre-trained on ImageNet).
* Custom Layers: Added dense and dropout layers for classification.

### Fine-tuning
The model fine-tunes the last 100 layers of MobileNetV2 for better performance.
### Performance
* Initial Training Accuracy: ~58%
* Fine-tuned Accuracy: ~97%

### File Structure
```bash
Distracted-Driver-Classification/
├── Input/
│   ├── train/               # Training images (10 subfolders for each class)
│   ├── test/                # Test images
│   └── driver_imgs_list.csv # Metadata file
├── Output/
│   └── output.csv           # Output file
├── distracted_driver.ipynb  # Code for the project
├── requirements.txt         # Dependencies
└── README.md                # Project documentation
```
### Notes
* Ensure the Input/ directory structure is correctly maintained as shown above.
* Modify paths in the notebook if your folder structure differs or paths need adjustment.
* For better performance, ensure you have a GPU-enabled environment with TensorFlow.

