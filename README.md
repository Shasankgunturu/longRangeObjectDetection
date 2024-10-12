# bigBangBoomHackathon


## YOLOv5 NAS Object Detection with SuperGradients

This repository contains a Python script, `yoloNAS.ipynb`, that demonstrates a complete object detection training and evaluation pipeline using the YOLOv5 NAS model and the SuperGradients library. The script focuses on the "aerial-person-detection" dataset from Roboflow.

**Project Structure:**

```
├── yoloNAS.ipynb  # Main script for training and evaluation
```

**Functionality:**

1. **Setup and Dependencies:**
    - Checks for GPU availability using `nvidia-smi`.
    - Installs required libraries: `super-gradients`, `roboflow`, and `supervision`.
    - Defines basic variables like the working directory, device, and model architecture.
    - Downloads the "aerial-person-detection" dataset from Roboflow.

2. **Data Loading and Preprocessing:**
    - Extracts dataset information like download location and class labels.
    - Configures data loading parameters including batch size, epochs, checkpoint directory, and experiment name.
    - Loads training, validation, and test datasets using `super_gradients` library.

3. **Model Initialization and Training:**
    - Initializes a YOLOv5 NAS model using `super_gradients` with specified architecture and number of classes.
    - Defines training parameters like optimizer, learning rate scheduler, loss function, metrics, etc.
    - Starts the training process using the `Trainer` object from `super_gradients`.

4. **Evaluation and Visualization:**
    - Loads the best model from checkpoints.
    - Evaluates the model on the test dataset using `test()` method.
    - Visualizes results by displaying test images with overlaid predicted bounding boxes and ground truth annotations.

**Dependencies:**

- `super-gradients`
- `roboflow`
- `supervision`

**Usage:**

1. Install dependencies: `pip install -r requirements.txt`
2. Download the dataset from Roboflow: [Dataset Link](https://universe.roboflow.com/aerial-person-detection)
3. Run `yoloNAS.ipynb` script.

**Output:**

The script will:

- Train the YOLOv5 NAS model on the aerial-person-detection dataset.
- Evaluate the trained model on the test dataset, calculating metrics like mAP@0.50.
- Display test images with overlaid predicted bounding boxes and ground truth annotations.

**Key Features:**

- Utilizes the powerful SuperGradients library for efficient training and evaluation.
- Integrates Roboflow for dataset management and download.
- Leverages Supervision for data loading and visualization.
- Demonstrates a complete object detection workflow from data loading to visualization.

**Note:** This script provides a basic example and can be further customized for specific requirements, including:

- Experimenting with different model architectures and hyperparameters.
- Incorporating data augmentation techniques.
- Implementing advanced visualization methods.
- Integrating with cloud platforms for scalability.

This project serves as a starting point for exploring object detection with YOLOv5 NAS and SuperGradients. Feel free to modify and extend the code for your own applications and research.


---
Generated with ❤️ using [GitDocs](https://github.com/mikhail-ram/gitdocs).
