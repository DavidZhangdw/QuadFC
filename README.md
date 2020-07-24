# QuadFC
**Joint Representation Learning with Deep Quadruplet Network for Real-Time Visual Tracking**

## Introduction
Recently, trackers based on Siamese networks have attracted spread attention in the field of visual tracking because of a balance between accuracy and speed. However, features extracted in most networks cannot accurately distinguish a tracked target from the background with semantic information in some challenging scenes. 

Therefore, learning powerful representation via effective offline training strategy is critical for constructing high performance Siamese trackers. In this work, the main
contributions of this work are suammrized as:
1) we developed a Fully- Convolutional deep Quadruple Network (QuadFC) to learn more expressive representation by mining inherent connections among samples. 
2) We proposed a multi-task loss function composed of a differential pairwise loss as well as the constructed triplet loss for joint representation learning.
3) Comprehensive experiments, on several representative tracking benchmarks, show that QuadFC achieves state-of-the-art performance while tracking with a far beyond real-time speed.

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
| Raw Results | :paperclip: [OTB2013](https://pan.baidu.com/s/1IyTuzeMioo1njzjHiNHDcQ) | :paperclip: [OTB2015](https://pan.baidu.com/s/1TDoa0R3WEdzGnKPPuIqYCg)  | :paperclip: [VOT15](https://pan.baidu.com/s/1SGLcMWgrBuBT_kaXMdQBug)  | :paperclip: [VOT16](https://pan.baidu.com/s/11-5_PVhRzu-3CAinSA1PTQ) |  :paperclip: [VOT17](https://pan.baidu.com/s/1PIgI5c8vmEL39frywsiMFA) |

- The trained models are released to facilitate further reseaches.
- Download pretrained [model](https://pan.baidu.com/s/1zYBmJ5tkEWVm0avv6ZaFbA) (password: bvde).

#### Environment 
The proposed architecture is implemented in Python with PyTorch 0.4.1 and all the experimental results are obtained on a workstation with Intel(R) Xeon(R) CPU E5-2683 v4
@2.10GHz and a NVIDIA GeForce GTX 1080 Ti GPU.

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
