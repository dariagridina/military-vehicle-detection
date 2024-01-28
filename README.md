# MILITARY VEHICLE DETECTION

## Introduction
This project focuses on training a YOLO NAS-based model for military vehicle detection.
It includes a comprehensive training pipeline, as well as a testing pipeline to evaluate the model's performance.

## Installation
1. **Clone the Repository**
   - Begin by cloning the project repository from GitHub:
     ```shell
       git clone https://github.com/dariagridina/military-vehicle-detection.git
     ```
2. **Install Requirements**
   - Navigate to the cloned directory and install the necessary requirements:
     ```shell
     cd military-vehicle-detection
     pip install -r requirements.txt
     ```

## Dataset Acquisition
- **Option 1: Download directly from Roboflow (Recommended for Roboflow Account Holders)**
  - If you have a Roboflow account, you can directly download the dataset using your API key.
  - Uncomment and run the provided script in the `trining_pipeline.ipynb`. Replace `<your-api-key>` with your actual Roboflow API key:
    ```python
    rf = Roboflow(api_key="<your-api-key>")
    project = rf.workspace("vgtu-n8zmy").project("military-vehicle")
    dataset = project.version(6).download("yolov8")
    ```
- **Option 2: Download from Google Drive (Alternative Option)**
  - If you do not have a Roboflow account, you can download the dataset from Google Drive. To do that run this script:
    ```shell
    gdown 'https://drive.google.com/uc?id=1MYhcTICu2Zz-T7wqBfWsaR57j8TingvY'
    unzip military-vehicle-6.zip
    rm -rf military-vehicle-6.zip
    ```

## Training the Model
1. **Start Jupyter Notebook Server**
   - Before accessing the training pipeline, start the Jupyter Notebook server:
     ```shell
     jupyter notebook
     ```
   - This will open Jupyter Notebook in your default web browser.


2. **Access the Training Pipeline**
   - Navigate to the `training_pipeline.ipynb` Jupyter notebook included in the repository.


3. **Run the Training Pipeline**
   - Execute the cells in the notebook to start the training process.
   - Ensure you have the dataset in the correct directory as specified in the notebook.

## Testing the Model
1. **Download Model Checkpoints**
   - Download the trained model checkpoints from Google Drive. Run this script in `test.ipynb` to download:
    ```shell
    gdown 'https://drive.google.com/uc?id=1MDmKKqYyxjqgnU8b_HMauUyxvKBWa1uu'
    unzip checkpoints.zip
    rm -rf checkpoints.zip
   ```

2. **Run the Testing Pipeline**
   - Open the `test.ipynb` notebook.
   - Follow the instructions in the notebook to load the model checkpoints and run the tests.

## Additional Notes
- Ensure you follow the steps in sequence to avoid any issues.
- If you encounter any problems or have suggestions, feel free to open an issue in the GitHub repository.
