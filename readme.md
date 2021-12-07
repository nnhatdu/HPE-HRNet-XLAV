# Multi-person Human Pose Estimation with HigherHRNet in PyTorch

Supports both Windows and Linux.

This repository currently provides:
- A slightly simpler implementation of ``HigherHRNet`` in PyTorch (>=1.0) - compatible with official weights 
(``pose_higher_hrnet_*``).
- A simple class (``SimpleHigherHRNet``) that loads the HigherHRNet network for the bottom-up human pose 
estimation, loads the pre-trained weights, and make human predictions on a single image or a batch of images.
- Support for multi-GPU inference.
- Multi-person support by design (HigherHRNet is a bottom-up approach).
- A reference code that runs a live demo reading frames from a webcam or a video file.

### Running the live demo

From a connected camera:
```
python scripts/live-demo.py --camera_id 0
```
From a saved video:
```
python scripts/live-demo.py --filename video.mp4
```

### Extracting keypoints:

From a saved video:
```
python scripts/extract-keypoints.py --format csv --filename video.mp4
```

### Installation instructions

- Install the required packages:
 ``pip install -r requirements.txt``

- Download the official pre-trained weights from and extract in to "weights" folder:
https://drive.google.com/file/d/1Ns7sm45AcJH2BfZDlnbbSVcsVAp469Xc/view?usp=sharing

- Your folders should look like:
    ```
    simple-HigherHRNet
    ├── gifs                    (preview in README.md)
    ├── misc                    (misc)
    ├── models                  (pytorch models)
    ├── scripts                 (scripts)
    └── weights                 (HigherHRnet weights)
    ```