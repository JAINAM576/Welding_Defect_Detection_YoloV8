# Welding Defect Detection using YOLOv8

This project focuses on detecting defects in welding surfaces using a YOLOv8 model. The dataset used for training contains three classes: `bad weld`, `good weld`, and `defect`. The dataset is formatted for object detection tasks using the YOLO annotation format.

## Dataset

The dataset used in this project is sourced from the [Welding Defect Object Detection Dataset](https://www.kaggle.com/datasets/sukmaadhiwijaya/welding-defect-object-detection/data) on Kaggle. The dataset includes images labeled for object detection, with annotations provided in YOLO format.

- **Classes**: `bad weld`, `good weld`, `defect`
- **Label Map**: Defined in the `data.yaml` file.

## Model Training

The YOLOv8 model was trained on this dataset for 50 epochs. The final results of the training process are as follows:

| Epoch | GPU Memory | Box Loss | Classification Loss | DFL Loss | Instances | Image Size |
|-------|------------|----------|---------------------|----------|-----------|------------|
| 50/50 | 8.34G      | 1.267    | 1.155               | 1.312    | 18        | 640        |

## Usage

### Installation

To run the code in this repository, follow these steps:

1. **Clone the repository**:

    ```bash
    git clone https://github.com/JAINAM576/Welding_Defect_Detection_YoloV8
    ```

2. **Install the required libraries**:

    ```bash
    pip install -r requirements.txt
    ```

### Inference

To perform inference using the trained model, follow these steps:

1. **Import YOLO from ultralytics**:

    ```python
    from ultralytics import YOLO
    ```

2. **Load the model**:

    ```python
    model = YOLO('path/to/your/model.pt')
    ```

3. **Run inference**:

    ```python
    results = model('path/to/images')
    results.show()
    ```

# Results
After training for 50 epochs, the model can detect defects in welding surfaces with good accuracy. The following metrics were achieved:

Box Loss: 1.267
Classification Loss: 1.155
DFL Loss: 1.312

- F1 CURVE
![F1_curve](https://github.com/user-attachments/assets/90dff7a0-a1ac-46ab-bc57-27cf9c813316)
- PRECISON - RECALL CURVE
 ![PR_curve](https://github.com/user-attachments/assets/c2f90e3d-8842-41dd-8e18-1b1aa3588dbb)



# Contributing
If you'd like to contribute to this project, please fork the repository and use a feature branch. Pull requests are warmly welcome.


# Acknowledgements
The dataset was sourced from the Welding Defect Object Detection Dataset on Kaggle.
Thanks to the authors of the YOLOv8 model and the open-source community for their continuous support.
