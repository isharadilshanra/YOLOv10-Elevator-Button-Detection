# Elevator Button Detection

This project aims to detect and classify various elevator buttons (floor numbers, door open, door close, alarm, etc.) using a video feed from a robot camera. The model is built using the YOLOv10-S model and trained on a custom dataset.

## Project Overview

- **Objective**: Identify elevator buttons from video images captured while the robot navigates in an elevator.
- **Dataset**: A custom dataset of around 1500 images for training, 200 for testing and 400 for validation, sourced from Roboflow.
- **Model**: YOLOv10-S was used to train the object detection model on processed elevator button images.
  
## Features

- **Elevator Buttons Detected**:  
  - Floor number buttons  
  - Door open/close buttons  
  - Alarm button  
  - Additional common buttons found in conventional elevators
- **Image Preprocessing**:
  - Color condition adjustments
  - Rotation and flipping
  - Noise injection for robustness

## Dataset

| Images | Count |
|--------|-------|
| Training Set | 14012  |
| Validation Set  | 405   |
| Testing Set  | 202   |


**Sample Original Images:**

!(![1784_jpg rf dcc678ca671040539852f2ed44948588 (1)](https://github.com/user-attachments/assets/37e28de9-d047-423d-bfcf-315029b6d81b))  
!(![1803_jpg rf bea5f604599000276aa75f44fbcd06ca (1)](https://github.com/user-attachments/assets/e42db114-b1c1-48fd-a80e-6e864c5d9cd4))
!(![2071_jpg rf d7f517c3e86d068c4777bb39e86c0963 (1)](https://github.com/user-attachments/assets/c5432f4a-8b3d-477f-a867-bb62facd2a05))

---

## Model Training

- **Model**: YOLOv10-S
- **Training Epochs**: 120
- **Batch Size**: 16
- **Image Size**: 640x640
- **Optimizer**: Adam
- **Loss Function**: Cross-Entropy Loss with YOLOv10 adjustments

### Image Augmentation
We applied the following augmentations to improve the robustness of the model:

1. Color adjustment
2. Image rotation
3. Flipping
4. Noise injection

---

## Test Results

Below are some results from testing the model:

**Test Image 1:**

| Original Image | Detection Result |
|----------------|------------------|
| !(![1784_jpg rf dcc678ca671040539852f2ed44948588 (1)](https://github.com/user-attachments/assets/4f840731-8c12-4542-8726-c48b7ae395af)) | ![Detection Result 1](![1784_jpg rf dcc678ca671040539852f2ed44948588](https://github.com/user-attachments/assets/68f0656f-390c-4b04-bd3f-1ebe595709af)) |

**Test Image 2:**

| Original Image | Detection Result |
|----------------|------------------|
| !(![1803_jpg rf bea5f604599000276aa75f44fbcd06ca (1)](https://github.com/user-attachments/assets/500f50ed-cdce-4f50-a434-981fc8012e25)) | ![Detection Result 2](![1803_jpg rf bea5f604599000276aa75f44fbcd06ca](https://github.com/user-attachments/assets/14056a3c-bea5-44a4-9613-1226570a6c28)) |

**Test Image 3:**

| Original Image | Detection Result |
|----------------|------------------|
| !(![2071_jpg rf d7f517c3e86d068c4777bb39e86c0963 (1)](https://github.com/user-attachments/assets/028d515b-9a10-41a9-9da0-81ac8871ebb3)) | ![Detection Result 2](![2071_jpg rf d7f517c3e86d068c4777bb39e86c0963](https://github.com/user-attachments/assets/b330f9db-1f71-4a4c-824f-b23d4f47b2c1)) |

---

## Video Demonstration

Watch the video demonstration below, where the robot navigates in the elevator and successfully identifies different elevator buttons in real-time.

[(![thumb-videio](https://github.com/user-attachments/assets/568fd268-b636-4d02-b4aa-ba656bea0b1f)
)](

https://github.com/user-attachments/assets/d4bc3e2d-259e-427f-b73a-90ecb22e1bff

)

---

## How to Use

Clone the repository:
    ```bash
    git clone https://github.com/isharadilshanra/YOLOv10-Elevator-Button-Detection.git
    ```
---

## Future Work

- Improve accuracy on buttons with varying lighting conditions
- Extend to other elevator types
- Enable real-time detections with edge devices

## License

This project is licensed under the MIT License.
