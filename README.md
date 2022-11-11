# Free Viewpoint RGB-D Video Dataset

![](https://github.com/sjtu-medialab/Free-Viewpoint-RGB-D-Video-Dataset/blob/main/examples.png)

## Introduction

Our free viewpoint RGB-D video dataset is a dynamic, synchronous and close to practical RGB-D HD free viewpoint synthesis dataset. Our dataset consists of 14 groups of video sequences, including 13 groups of human motion video sequences such as dancing, playing basketball and playing football, and 1 group of empty scene video sequences, as shown below. 

![](https://github.com/sjtu-medialab/Free-Viewpoint-RGB-D-Video-Dataset/blob/main/detail.png)

## Dataset Collecting and Post Processing

We designed the collecting environment and system as shown below. 

![](https://github.com/sjtu-medialab/Free-Viewpoint-RGB-D-Video-Dataset/blob/main/framework.png)

The collecting environment is a uniformly lighted clean indoor stage which is 8.2 meters in length and 5.5 meters in width. The collecting system includes 12 Panasonic DC-BGH1 cameras, 3 raw data collecting computer, a system control computer, the switcher group, and the synchronization signal processor. The 12 cameras are placed regularly on an arc in front of the scene, about 46 cm and 5.5° apart. 

An alumina calibration chess board is used to get more exact intrinsic and extrinsic parameters of the 12 cameras. Then we get depth images for all frames of video sequences with COLMAP. For each camera view, we calculate a common background depth map which is the average of nonempty part of depth images that corresponds to RGB frames taken by this camera. After that, we improved quality of depth images by background replacement and foreground filtering. 

## Video Sequences Download

At this time, you can access our [BaiduNetdisk](https://pan.baidu.com/s/1R-tQ54zPowTkadevr-GbBQ)(百度网盘) with verify code of 'sjtu', or [MEGA](https://mega.nz/folder/pQlGkJCD#jjwphJzKOvpYKWVEc-tKbA) to download video sequences of the dataset. More access to our dataset will be released soon. 

You can also refer to this [link](https://medialab.sjtu.edu.cn/post/free-viewpoint-rgb-d-video-dataset/) in [Medialab](https://medialab.sjtu.edu.cn/).

## Camera Parameters

**Camera parameters are provided in [this repository](https://github.com/sjtu-medialab/Free-Viewpoint-RGB-D-Video-Dataset.git).**

In this repository, `Camera Parameters/paras.txt` has 60 lines.
Each 5 lines contain camera parameters of a camera: 
- Line of `resolution` describes resolution of this camera, all camera have a resolution of 1920x1080;
- Line of `K_matrix` has 4 numbers, which are `fx`, `fy`, `cx`, `cy` of the intrinsic matrix;
- Line of `R_matrix` has 9 numbers, which are the 9 numbers of the rotation matrix `R`, oriented top to bottom and left to right;
- Line of `world_position` has 3 numbers, which describes world position `t` of this camera.

For each point `Xw` in the world system, its position in the position system of this camera `Xc` is got by `Xc = R(Xw-t)`

## Video Demo
A video demo based on this dataset (after quality improvement of depth image) and DIBR benchmark is available in:
[![FVV Demo](https://res.cloudinary.com/marcomontalbano/image/upload/v1663898662/video_to_markdown/images/youtube--pLSruH-0byo-c05b58ac6eb4c4700831b2b3070cd403.jpg)](https://www.bilibili.com/video/BV1Fe4y1b7mt/?vd_source=1ba4467af510cf2b0070aaa2dbb0a4c9 "FVV Demo")

## Paper
If our dataset is helpful to your research, please cite this paper:

```bibtex
@inproceedings{guo2022new,
  title={A new free viewpoint video dataset and DIBR benchmark},
  author={Guo, Shuai and Zhou, Kai and Hu, Jingchuan and Wang, Jionghao and Xu, Jun and Song, Li},
  booktitle={Proceedings of the 13th ACM Multimedia Systems Conference},
  pages={265--271},
  year={2022}
}
```
