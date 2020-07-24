# QuadFC
**Joint Representation Learning with Deep Quadruplet Network for Real-Time Visual Tracking**

## Introduction
Recently, trackers based on Siamese networks have attracted spread attention in the field of visual tracking because of a balance between accuracy and speed. Learning powerful representation via effective offline training strategy is critical for constructing high performance Siamese trackers. However, features extracted in most networks cannot accurately distinguish a tracked target from the background with semantic information in some challenging scenes. 

In this work, we develop a Fully- Convolutional deep Quadruple Network (QuadFC) to learn more expressive representation via a novel multi-task loss function composed of a differential pairwise loss for tracking and a constructed triplet loss for metric learning, which can be trained offline in an end-to-end manner. Extensive experiments on several tracking benchmarks, show that the proposed tracker achieves the state-of-the-art tracking performance while running at 68 FPS.

## Exprimental Results
This repository includes PyTorch code for reproducing the results on benchmark.

#### Main results on VOT and OTB Benchmarks
| Models  | OTB13 | OTB15 | VOT15 | VOT16 | VOT17|
| :------ | :------: | :------: | :------: | :------: | :------: | 
| Alex-FC      | 0.608 | 0.579 | 0.289 | 0.235 | 0.188 |
| Alex-RPN     | -     | 0.637 | 0.349 | 0.344 | 0.244 |
| CIResNet22-FC  | 0.663 | 0.644 | 0.318 | 0.303 | 0.234 |
| CIResIncep22-FC| 0.662 | 0.642 | 0.310 | 0.295 | 0.236 |
| CIResNext23-FC | 0.659 | 0.633 | 0.297 | 0.278 | 0.229 |
| QuadFC         | **0.686** | **0.666** | **0.362** | **0.343** | **0.275** |
| Raw Results | :paperclip: [OTB2013](https://pan.baidu.com/s/1OO3Dejx8SiQjMTq9P0B0-A) | :paperclip: [OTB2015](https://pan.baidu.com/s/1Mnvgp56XYGD3RJCzUF7iQg)  | :paperclip: [VOT15](https://pan.baidu.com/s/1SGLcMWgrBuBT_kaXMdQBug)  | :paperclip: [VOT16](https://drive.google.com/open?id=1dAyYSpAJhMd6mFE2uRPblCkci) |  :paperclip: [VOT17](https://drive.google.com/open?id=1Heg_Pwv021pl47ekHM43KjF4I) |

- The trained models are released to facilitate further reseaches.
- Download pretrained [model](https://pan.baidu.com/s/1zYBmJ5tkEWVm0avv6ZaFbA) (password:bvde).

#### Environment 
The proposed architecture is implemented in Python with PyTorch 0.4.1 and all the experimental results are obtained on a workstation with Intel(R) Xeon(R) CPU E5-2683 v4
@2.10GHz and a NVIDIA GeForce GTX 1080 Ti GPU

### Citation
If you find this code useful, please consider citing:

```
@inproceedings{Zhang_2019_QuadFC,
  title={Joint Representation Learning with Deep Quadruplet Network for Real-Time Visual Tracking},
  author={Dawei Zhang and Zhonglong Zheng},
  booktitle={International Joint Conference on Neural Networks (IJCNN)},
  year={2020}
}
```
