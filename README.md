# Resources for Low Light Imaging & Low Light Image Enhancement
**This is a list of resources for low light imaging and low light image enhancement, including datasets, algorithms and so on.**

**Maintained by:** [Zhihong Zhang](mailto:z_zhi_hong.com)

## Introduction

Low light imaging and low light image enhancement have wild applications in our daily life and different scientific research fields, like night surveillance, automated driving, fluorescence microscopy, high speed imaging and so on. However, there is still a long way to go in dealing with these tasks, considering the great challenges in low photon counts, low SNR, complicated noise models, etc. Here, we collect a list of resources which are related to low light imaging and low light image enhancement, including datasets, algorithms and so on. We hope this can help to provide some help to the development of new methods and solutions to the low light imaging tasks.



## Table of Contents

* [Datasets](#datasets)
* [Algortihms](#algortihms)
  + [Non-learning-based methods](#Non-learning-based methods)
  + [Learning-based methods](#Learning-based methods)
  + [Related methods](#Related methods)

- [Reference](#reference)


## Datasets
|          dataset           |                      brief introduction                      |                             link                             |
| :------------------------: | :----------------------------------------------------------: | :----------------------------------------------------------: |
|        VIP-LowLight        |  Eight Natural Images Captured in Very Low-Light Conditions  | https://uwaterloo.ca/vision-image-processing-lab/research-demos/vip-lowlight-dataset |
|           ReNOIR           | RENOIR - A Dataset for Real Low-Light Image Noise Reduction  | [http://ani.stat.fsu.edu/~abarbu/Renoir.html](http://adrianbarburesearch.blogspot.com/p/renoir-dataset.html) |
| Raw Image Low-Light Object |                              -                               |        https://wiki.qut.edu.au/display/cyphy/Datasets        |
|            SID             | Learning to see in the dark; <br />light level (outdoor scene 0.2 lux - 5 lux; indoor scene: 0.03 lux - 0.3 lux) | http://vladlen.info/publications/learning-see-dark （including codes） |
|           ExDARK           | Getting to Know Low-light Images with The Exclusively Dark Dataset | https://github.com/cs-chan/Exclusively-Dark-Image-Dataset （including codes） |
|      MIT-Adobe FiveK       | Learning Photographic Global Tonal Adjustment with a Database of Input / Output Image Pairs<br />(with ~4% low light images) |          https://data.csail.mit.edu/graphics/fivek           |
|       LRAICE-Dataset       |   A Learning-to-Rank Approach for Image Color Enhancement    |                              -                               |
|     The 500px Dataset      |    Exposure: A White-Box Photo Post-Processing Framework     |                              -                               |
|            DPED            | DSLR-quality photos on mobile devices with deep convolutional networks |              http://people.ee.ethz.ch/~ihnatova              |
|            LOL             |     Deep Retinex Decomposition for Low-Light Enhancement     |          https://daooshee.github.io/BMVC2018website          |
|             VV             |                              -                               |       https://sites.google.com/site/vonikakis/datasets       |


## Algorithms
### Non-Learning-based methods

- **LIME** 
- **A New Low-Light Image Enhancement Algorithm Using Camera Response Model** [[Pdf]](http://ieeexplore.ieee.org/document/8265567/) 
  * Z. Ying, G. Li, Y. Ren, R. Wang and W. Wang, "A New Low-Light Image Enhancement Algorithm Using Camera Response Model," *2017 IEEE International Conference on Computer Vision Workshops (ICCVW)*, Venice, 2017

### Learning-based methods

* **MSR-net** [[Pdf]](https://arxiv.org/pdf/1711.02488v1.pdf)
  * L. Shen, Z. Yue, F. Feng, Q. Chen, S. Liu, and J. Ma, “MSR-net:Low-light Image Enhancement Using Deep Convolutional Network,” *arXiv:1711.02488 [cs]*, Nov. 2017
* **Deep Burst Denoising** [[Pdf]](http://arxiv.org/abs/1712.05790)
  * C. Godard, K. Matzen, and M. Uyttendaele, “Deep Burst Denoising,” *arXiv:1712.05790 [cs, stat]*, Dec. 2017 
* **LLCNN** [[Pdf]](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=8305143)
  * L. Tao, C. Zhu, G. Xiang, Y. Li, H. Jia and X. Xie, "LLCNN: A convolutional neural network for low-light image enhancement," *2017 IEEE Visual Communications and Image Processing (VCIP)*, St. Petersburg, FL, 2017
* **Deep bilateral learning for real-time image enhancement** [[Web]](https://groups.csail.mit.edu/graphics/hdrnet/) [[Code]](https://github.com/google/hdrnet) [[Pdf]](https://arxiv.org/abs/1707.02880)
  * M. Gharbi, J. Chen, J. T. Barron, S. W. Hasinoff, and F. Durand, “Deep bilateral learning for real-time image enhancement,” *ACM Trans. Graph.*, vol. 36, no. 4, pp. 1–12, Jul. 2017
* **DSLR Quality Photos on Mobile Devices with Deep Convolutional Networks**  [[Pdf]](https://arxiv.org/abs/1704.02470)
  * A. Ignatov, N. Kobyshev, R. Timofte and K. Vanhoey, "DSLR-Quality Photos on Mobile Devices with Deep Convolutional Networks," *2017 IEEE International Conference on Computer Vision (ICCV)*, Venice, 2017
 * **Retinex-Net** [[Web]](https://daooshee.github.io/BMVC2018website/) [[Code]](https://github.com/weichen582/RetinexNet) [[Pdf]](https://arxiv.org/abs/1808.04560)
   * C. Wei, W. Wang, W. Yang, and J. Liu,"Deep Retinex Decomposition for Low-Light Enhancement." *BMVC 2018*, Oral Presentation.
   * :bookmark: retinex
* **Learning to See in the Dark** [[Web]](https://cchen156.github.io/SID.html) [[Code]](https://github.com/cchen156/Learning-to-See-in-the-Dark.git) [[Pdf]](https://cchen156.github.io/paper/18CVPR_SID.pdf)
  * C. Chen, Q. Chen, J. Xu, and V. Koltun, “Learning to See in the Dark,” *CVPR 2018*, May 2018
  * real  [dataset](https://github.com/cchen156/Learning-to-See-in-the-Dark)
* **GLADNet** [[Web]](https://daooshee.github.io/fgworkshop18Gladnet/) [[Code]](https://github.com/weichen582/GLADNet) [[Pdf]](https://github.com/daooshee/fgworkshop18Gladnet/blob/master/wwj_fg2018.pdf)
  * W. Wang, C. Wei, W. Yang and J. Liu, "GLADNet: Low-Light Enhancement Network with Global Awareness," *2018 13th IEEE International Conference on Automatic Face & Gesture Recognition*
  * synthetic [dataset](https://daooshee.github.io/fgworkshop18Gladnet/) generated from RAW images
* **A Pipeline Neural Network for Low-Light Image Enhancement** [[Pdf]](https://ieeexplore.ieee.org/document/8607964/)
  * Y. Guo, X. Ke, J. Ma, and J. Zhang, “A Pipeline Neural Network for Low-Light Image Enhancement,” *IEEE Access*, vol. 7
* **Kindling the Darkness** [[Pdf]](http://arxiv.org/abs/1905.04161)
  * Y. Zhang, J. Zhang, and X. Guo, “Kindling the Darkness: A Practical Low-light Image Enhancer,” *arXiv:1905.04161 [cs]*, May 2019
* **Learning Digital Camera Pipeline for Extreme Low-Light Imaging** [[Pdf]](https://arxiv.org/abs/1904.05939)
  * S. Waqas Zamir, A. Arora, S. Khan, F. Shahbaz Khan, and L. Shao, “Learning Digital Camera Pipeline for Extreme Low-Light Imaging,” *arXiv preprint arXiv:1904.05939*, 2019.
* **End-to-End Denoising of Dark Burst Images Using Recurrent Fully Convolutional Networks** [[Pdf]](https://arxiv.org/abs/1904.07483v1)
  * D. Zhao, L. Ma, S. Li, and D. Yu, “End-to-End Denoising of Dark Burst Images Using Recurrent Fully Convolutional Networks,” *arXiv:1904.07483 [cs]*, Apr. 2019 
* **DeepISP** [[Pdf]](https://arxiv.org/abs/1801.06724)
  * E. Schwartz, R. Giryes, and A. M. Bronstein, “DeepISP: Towards Learning an End-to-End Image Processing Pipeline,” *IEEE Trans. on Image Process.*, vol. 28, no. 2, pp. 912–923, Feb. 2019
* **DeepUPE** [[Code]](https://github.com/wangruixing/DeepUPE) [[Pdf]](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=8953588)
  * R. Wang, Q. Zhang, C. Fu, X. Shen, W. Zheng and J. Jia, "Underexposed Photo Enhancement Using Deep Illumination Estimation," *2019 IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR)*, Long Beach, CA, USA, 2019
  * :bookmark: retinex
* **Low-Light Image Enhancement via a Deep Hybrid Network**  [[Pdf]](https://ieeexplore.ieee.org/document/8692732)
  * W. Ren *et al*., "Low-Light Image Enhancement via a Deep Hybrid Network," in *IEEE Transactions on Image Processing*, vol. 28, no. 9, pp. 4364-4375, Sept. 2019

### Related methods

-  **Automatic Photo Adjustment Using Deep Neural Networks** [[Web]](https://sites.google.com/site/homepagezhichengyan/home/dl_img_adjust) [[Code]](https://github.com/stephenyan1984/dl-image-enhance/wiki) [[Pdf]](https://arxiv.org/abs/1412.7725v2)
  - Z. Yan, H. Zhang, B. Wang, S. Paris, and Y. Yu, “Automatic Photo Adjustment Using Deep Neural Networks,” *ACM Transactions on Graphics*, 2015.

## Reference

- https://zhuanlan.zhihu.com/p/140926754