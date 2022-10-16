# [YOLOv7] Pose Estimation

<p align="center">
  <a href="https://github.com/ITainment-UIT-04"><img width="30%" height="auto" src="https://github.com/Antares3102/Antares3102/blob/main/ITainment.png" height="175px"/></a>
</p>

[![Python 3.9](https://img.shields.io/badge/Python-3.9-3776AB)](https://www.python.org/downloads/release/python-390/)
[![Anaconda](https://img.shields.io/badge/Anaconca-3776A)](https://www.anaconda.com)

## Setup & Installation (For Anaconda environment)

- Download & Extract YOLOv7(pose): [YOLOv7](https://github.com/WongKinYiu/yolov7/tree/pose) *(Branches: pose)*
- Download Anaconda: [Anaconda](https://www.anaconda.com)
- Environment: anaconda *(window, wsl, linux)*
- Get [YOLOv7 inference code](https://github.com/WongKinYiu/yolov7/releases) and download [yolov7-w6-pose.pt](https://github.com/WongKinYiu/yolov7/releases/download/v0.1/yolov7-w6-pose.pt)
- Create new environment:

```sh
conda update conda
conda create --name my_env
conda info --env
conda activate my_env
```

### **Install [CuDNN](https://developer.nvidia.com/rdp/cudnn-archive)**
```sh
conda install -c anaconda cudnn
```

### **Install [Tensorflow](https://www.tensorflow.org/install)**
```sh
conda install -c conda-forge tensorflow
```

### **Install [Pytorch](https://pytorch.org/get-started/previous-versions/)**
```sh
conda install pytorch==1.12.0 torchvision==0.13.0 torchaudio==0.12.0 cudatoolkit=11.3 -c pytorch
```
*After install Pytorch, command:*
```sh
python
```
```sh
import torch
torch.cuda.is_available()
```
*Desired results:*
```sh
True
```
*After that, exit:*
```sh
exit()
```

### **Download file [requirements.txt](https://github.com/WongKinYiu/yolov7/blob/pose/requirements.txt) and command**
```sh
pip install -r requirements.txt
```
### Test Pose estimation with [yolov7-w6-pose.pt](https://github.com/WongKinYiu/yolov7/releases/download/v0.1/yolov7-w6-pose.pt) 
```sh
python detect.py --weight yolov7-w6-pose.pt --kpt-label --hide-labels --hide-conf --source <path> --line-thickness <int> --nosave --view-img
```
**Usage**
```sh
detect.py [-h] [--weights WEIGHTS [WEIGHTS ...]] [--source SOURCE] [--img-size IMG_SIZE [IMG_SIZE ...]]
                 [--conf-thres CONF_THRES] [--iou-thres IOU_THRES] [--device DEVICE] [--view-img] [--save-txt]
                 [--save-txt-tidl] [--save-bin] [--save-conf] [--save-crop] [--nosave]
                 [--classes CLASSES [CLASSES ...]] [--agnostic-nms] [--augment] [--update] [--project PROJECT]
                 [--name NAME] [--exist-ok] [--line-thickness LINE_THICKNESS] [--hide-labels] [--hide-conf]
                 [--kpt-label] [--nobbox]
```
**Real Time Pose Estimation**
```sh
python detect.py --weight yolov7-w6-pose.pt --kpt-label --hide-labels --hide-conf --source 0 --nosave --view-img
```
**Note**: You can get [YOLOv7 inference code](https://github.com/WongKinYiu/yolov7/releases) and download difference **WEIGHTS**
```sh
python detect.py --<WEIGHTS> --kpt-label --hide-labels --hide-conf --source <path> --nobbox
```
## Source: Object Detection (YOLOv7, YOLOv3, YOLOv4 , TensorFlow)
- **Youtube:** [Official YOLO V7 Pose Estimate | Windows and Linux](https://www.youtube.com/watch?v=z1UN7TbcRgM)
- **Dataset:** [Click here to download](#)
