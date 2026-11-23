# Brain MRI Image Classification with VGG-16

A computer-vision project exploring **transfer learning with VGG-16** to classify brain MRI images into two dataset labels: **tumor** and **no tumor**.

The implementation is provided in the Jupyter notebook `Brain Tumor.ipynb`.

> **Educational prototype only.** This project is not a medical device, has not been clinically validated, and must not be used to diagnose a brain tumor or make healthcare decisions.

## Project overview

The notebook uses a pretrained VGG-16 network as the basis for an image-classification workflow. The task is a binary classification problem using the folder labels supplied by the dataset.

### Workflow

```text
Brain MRI images
       |
       v
Image preprocessing
       |
       v
VGG-16 transfer-learning model
       |
       v
Binary classification
       |
       v
Tumor / No tumor label
```

## Dataset

- **Source:** [Brain MRI Images for Brain Tumor Detection](https://www.kaggle.com/datasets/navoneel/brain-mri-images-for-brain-tumor-detection)
- **Input:** MRI image files
- **Labels:** `YES` and `NO`, as provided by the dataset

The dataset is intended for experimentation and does not represent the full range of MRI scanners, acquisition protocols, patient populations, or brain conditions encountered in clinical practice.

## Technologies

- Python
- TensorFlow / Keras
- VGG-16 transfer learning
- OpenCV
- NumPy
- Matplotlib and Seaborn
- Jupyter Notebook

## Run the notebook

1. Clone this repository.
2. Download the dataset from the source linked above and review its terms of use.
3. Arrange the dataset folders as expected by the notebook.
4. Open `Brain Tumor.ipynb` in Jupyter or Google Colab.
5. Install the dependencies used in the notebook and execute the cells in order.

A GPU-enabled runtime may speed up training and inference. Exact package versions and runtime requirements depend on the notebook environment.

## Evaluation

The notebook contains the model implementation and evaluation steps. Reported accuracy can vary with the train/validation/test split, preprocessing, random seed, and dataset composition. For a meaningful evaluation, keep patient-level separation between splits where patient identifiers are available, and report precision, recall, F1-score, and a confusion matrix alongside accuracy.

## Limitations

- The dataset is relatively small and may not represent real-world clinical variation.
- A binary label does not capture tumor type, location, grade, or other clinically relevant information.
- High test accuracy on this dataset does not establish clinical reliability or generalization.
- Model outputs must not be used as a substitute for assessment by qualified medical professionals.

## Repository contents

- `Brain Tumor.ipynb` — notebook containing the model workflow.

---

Built by [Nuaima Saeed](https://github.com/Nuaima).
