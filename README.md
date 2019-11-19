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


## Citing QuadFC

If you find **QuadFC** useful in your research, please consider citing:

```
@inproceedings{Zhang_2019_QuadFC,
  title={Joint Representation Learning with Deep Quadruplet Network for Visual Tracking},
  author={Dawei Zhang and Zhonglong Zheng},
  booktitle={arXiv preprint arXiv:19xx.xxxxx},
  year={2019}
}
```
