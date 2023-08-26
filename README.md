# Breast Cancer Detection Using Federated Learning 

<img src="https://github.com/Rhidz/Breast-Cancer-Detection-Using-Federated-Learning/blob/main/Header Picture.jpg" align="center"
     width="700" height="400">

# Framework

<img src="https://github.com/Rhidz/Breast-Cancer-Detection-Using-Federated-Learning/blob/main/Fl.png" align="center"
     width="700" height="300">

## Setup
### 1)Envs
- mac/windows
- Python>=3.6

### 2)Prepare the dataset
- Download the breast cancer dataset from [Kaggle](https://www.kaggle.com/datasets/aryashah2k/breast-ultrasound-images-dataset?resource=download).
- Use the [masking.ipynb](https://github.com/Rhidz/Breast-Cancer-Detection-Using-Federated-Learning/blob/main/masking.ipynb) file to perform preprocessing on the dataset

The dataset is divided into three folders benign, malignant, and normal. In each folder the ultrasound image of either a benign/malignant ultrasound with its mask is present. To create the dataset for training using the [Federated Learning Architecture](https://github.com/Rhidz/Breast-Cancer-Detection-Using-Federated-Learning/blob/main/Breast__Cancer__Detection__Using__FL.ipynb) create a folder in the same directory where the dataset is downloaded. The file structure should be as follows.

- File Structure
   ```
  BC_FL
    ├──dataset_masked
         ├── benign
               ├── benign_1.png
               ├── benign_2.png
               └── ...
         ├── malignant
               ├── malignant_1.png
               ├── malignant_2.png
               └── ...
         ├── normal
               ├── normal1.png
               ├── normal2.png
               └── ...
          
  ```

### 3) Validation and Accuracy

As described in the Federated Learning Architecture, data is divided among the clients manually using the [model](https://github.com/Rhidz/Breast-Cancer-Detection-Using-Federated-Learning/blob/main/Breast__Cancer__Detection__Using__FL.ipynb). Each client locally trains their model on the local data and shares the weights via communication. In this [model](https://github.com/Rhidz/Breast-Cancer-Detection-Using-Federated-Learning/blob/main/Breast__Cancer__Detection__Using__FL.ipynb) only one communication round is performed and accuracy after global update is around 94%. 


  
  
