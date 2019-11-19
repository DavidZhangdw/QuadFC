# QuadFC
**Joint Representation Learning with Deep Quadruplet Network for Visual Tracking**

This repository includes PyTorch code for reproducing the results on benchmark.

Dawei Zhang, Zhonglong Zheng

## Prerequisites

CPU: Intel(R) Xeon(R) CPU E5-2683 v4 @ 2.10GHz
GPU: NVIDIA GTX1080Ti

- python3.6
- pytorch == 0.4.1
- numpy
- opencv


## Pretrained model for QuadFC

In our tracker, we use an CIRes22W as our backbone, which is end-to-end trained for visual tracking.
The pretrained model can be downloaded from baidu drive: [QuadFC.model](https://pan.baidu.com/s/1dnQVRyAfxu6Ua6FJrcGkrw).
Then, you should copy the pretrained model file `QuadFC.model` to the subfolder './code', so that the tracker can find and load the pretrained_model.


## Detailed steps to install the prerequisites

- install pytorch, numpy, opencv following the instructions in the `run_install.sh`. Please use conda to install.
  If the tracker is ready, you will see the tracking results. (EAO: 0.358)


## Results
All results can be downloaded from [Baidu Drive](https://pan.baidu.com/s/1dnQVRyAfxu6Ua6FJrcGkrw).

| | <sub>VOT2015</br>A / R / EAO</sub> | <sub>VOT2016</br>A / R / EAO</sub> | <sub>VOT2017 & VOT2018</br>A / R / EAO</sub> | <sub>OTB2015</br>OP / DP</sub> | <sub>UAV123</br>AUC / DP</sub> | <sub>UAV20L</br>AUC / DP</sub> |
| :-: | :-: | :-: | :-: | :-: | :-: | :-: |
| <sub> **SiamRPN** </br> CVPR2017 </sub> | <sub>0.58 / 1.13 / 0.349<sub> | <sub>0.56 / 0.26 / 0.344<sub> | <sub>0.49 / 0.46 / 0.244<sub> | <sub>81.9 / 85.0<sub> | <sub>0.527 / 0.748<sub> | <sub>0.454 / 0.617<sub> |
| <sub> **DaSiamRPN** </br> ECCV2018 </sub> | <sub>**0.63** / **0.66** / **0.446**<sub> | <sub>**0.61** / **0.22** / **0.411**<sub> | <sub>0.56 / 0.34 / 0.326<sub> | <sub>**86.5** / **88.0**<sub> | <sub>**0.586** / **0.796**<sub> | <sub>**0.617** / **0.838**<sub> |
| <sub> **DaSiamRPN** </br> VOT2018 </sub> | <sub>-<sub> | <sub>-<sub>  | <sub>**0.59** / **0.28** / **0.383**<sub> | <sub>-<sub> | <sub>-<sub> | <sub>-<sub> |


# Demo and Test on OTB2015
<div align="center">
  <img src="code/data/bag.gif" width="400px" />
</div>

- To reproduce the reuslts on paper, the pretrained model can be downloaded from [Google Drive](https://drive.google.com/open?id=1BtIkp5pB6aqePQGlMb2_Z7bfPy6XEj6H): `SiamRPNOTB.model`. <br />
:zap: :zap: This model is the **fastest** (~200fps) Siamese Tracker with AUC of 0.655 on OTB2015. :zap: :zap: 

- You must download OTB2015 dataset (download [script](code/data/get_otb_data.sh)) at first.

A simple test example.

```
cd code
python demo.py
```

If you want to test the performance on OTB2015, please using the follwing command.

```
cd code
python test_otb.py
python eval_otb.py OTB2015 "Siam*" 0 1
```


# License
Licensed under an MIT license.


## Citing QuadFC

If you find **QuadFC** useful in your research, please consider citing:

```
@inproceedings{Zhu_2018_ECCV,
  title={Distractor-aware Siamese Networks for Visual Object Tracking},
  author={Zhu, Zheng and Wang, Qiang and Bo, Li and Wu, Wei and Yan, Junjie and Hu, Weiming},
  booktitle={European Conference on Computer Vision},
  year={2019}
}
```
