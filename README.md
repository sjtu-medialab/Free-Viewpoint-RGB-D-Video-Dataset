# Free Viewpoint RGB-D Video Dataset

![](https://github.com/sjtu-medialab/Free-Viewpoint-RGB-D-Video-Dataset/blob/main/frames.png)

## Introduction

Our free viewpoint RGB-D video dataset is a dynamic, synchronous and close to practical RGB-D HD free viewpoint synthesis dataset. Our dataset consists of 14 groups of video sequences, including 13 groups of human motion video sequences such as dancing, playing basketball and playing football, and 1 group of empty scene video sequences, as shown below. 

![](https://github.com/sjtu-medialab/Free-Viewpoint-RGB-D-Video-Dataset/blob/main/detail.png)

## Dataset Collecting and Post Processing

We designed the collecting environment and system as shown below. 

![](https://github.com/sjtu-medialab/Free-Viewpoint-RGB-D-Video-Dataset/blob/main/framework.png)

The collecting environment is a uniformly lighted clean indoor stage which is 8.2 meters in length and 5.5 meters in width. The collecting system includes 12 Panasonic DC-BGH1 cameras, 3 raw data collecting computer, a system control computer, the switcher group, and the synchronization signal processor. The 12 cameras are placed regularly on an arc in front of the scene, about 46 cm and 5.5° apart. 

An alumina calibration chess board is used to get more exact intrinsic and extrinsic parameters of the 12 cameras. Then we get depth images for all frames of video sequences with COLMAP. For each camera view, we calculate a common background depth map which is the average of nonempty part of depth images that corresponds to RGB frames taken by this camera. After that, we improved quality of depth images by background replacement and foreground filtering. 

## Download

At this time, you can access our [Baidu Netdisk](https://pan.baidu.com/s/1onBiiTBXcvb_X_xxht8Fug?pwd=igfd) or [MEGA](https://mega.nz/folder/pQlGkJCD#jjwphJzKOvpYKWVEc-tKbA) to download video sequences of the dataset. More access to our dataset will be released soon. 
You can also refer to this [link](https://medialab.sjtu.edu.cn/post/free-viewpoint-rgb-d-video-dataset/) in [Medialab](https://medialab.sjtu.edu.cn/).
Camera parameters are provided in this repository. 

## Video Demo
A video demo based on this dataset (after quality improvement of depth image) and DIBR benchmark is available in:
<iframe src="//player.bilibili.com/player.html?aid=560846220&bvid=BV1Fe4y1b7mt&cid=840790286&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>

## Paper
If our dataset is helpful to your research, please cite this paper:
> @inproceedings{guo2022new,

  title={A new free viewpoint video dataset and DIBR benchmark},
  
  author={Guo, Shuai and Zhou, Kai and Hu, Jingchuan and Wang, Jionghao and Xu, Jun and Song, Li},
  
  booktitle={Proceedings of the 13th ACM Multimedia Systems Conference},
  
  pages={265--271},
  
  year={2022}
  
}
