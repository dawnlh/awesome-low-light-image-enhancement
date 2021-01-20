# Resources for Low Light Image Enhancement
**This is a resource list for low light image enhancement, including datasets, methods/codes/papers, metrics, blogs and so on.**

**Maintained by:** [Zhihong Zhang](https://github.com/dawnlh)

Looking forward to your sharing! You can come up with your ideas and suggestions in the [issue](https://github.com/dawnlh/low-light-image-enhancement-resources/issues)



## Introduction

Low light imaging and low light image enhancement have wild applications in our daily life and different scientific research fields, like night surveillance, automated driving, fluorescence microscopy, high speed imaging and so on. However, there is still a long way to go in dealing with these tasks, considering the great challenges in low photon counts, low SNR, complicated noise models, etc. Here, we collect a list of resources related to low light image enhancement, including datasets, methods/codes/papers, metrics, and so on. We hope this can help to provide some help to the development of new methods and solutions to the low light tasks.

---



## Table of Contents
- [Highlights](#highlights)
- [Datasets](#datasets)
- [Methods](#methods)
  * [HE-based methods](#he-based-methods)
  * [Retinex-based methods](#retinex-based-methods)
  * [CRM&fusion-based methods (Camera Respond Model)](#crm-fusion-based-methods--camera-respond-model-)
  * [Learning-based methods](#learning-based-methods)
  * [Other methods](#other-methods)
  * [Latest methods](#latest-methods)
  * [Related works](#related-works)
- [Reviews](#reviews)
- [Metrics](#metrics)
- [Blogs & Slices](#blogs---slices)
- [Reference](#reference)
- [Supplementary](#supplementary)

---



## Highlights

:high_brightness: <font color='red'> **highlight!** </font>

- [**Benchmarking Low-Light Image Enhancement and Beyond**](recommended/recommended.md) [[Pdf]](https://link.springer.com/article/10.1007%2Fs11263-020-01418-8) [[Summary]](recommended/recommended.md)
  -  J. Liu, D. Xu, W. Yang, M. Fan, and H. Huang, “Benchmarking Low-Light Image Enhancement and Beyond,” *Int J Comput Vis*, Jan. 2021, doi: [10.1007/s11263-020-01418-8](https://doi.org/10.1007/s11263-020-01418-8).

------



## Datasets

|              dataset              |                      brief introduction                      |                             link                             |
| :-------------------------------: | :----------------------------------------------------------: | :----------------------------------------------------------: |
|           VIP-LowLight            |  Eight Natural Images Captured in Very Low-Light Conditions  | https://uwaterloo.ca/vision-image-processing-lab/research-demos/vip-lowlight-dataset |
|              ReNOIR               | RENOIR - A Dataset for Real Low-Light Image Noise Reduction  | [http://ani.stat.fsu.edu/~abarbu/Renoir.html](http://adrianbarburesearch.blogspot.com/p/renoir-dataset.html) |
|    Raw Image Low-Light Object     |                              -                               |        https://wiki.qut.edu.au/display/cyphy/Datasets        |
|              **SID**              | Learning to see in the dark; <br />light level (outdoor scene 0.2 lux - 5 lux; indoor scene: 0.03 lux - 0.3 lux) | http://vladlen.info/publications/learning-see-dark （including codes） |
|              ExDARK               | Getting to Know Low-light Images with The Exclusively Dark Dataset | https://github.com/cs-chan/Exclusively-Dark-Image-Dataset （including codes） |
|          MIT-Adobe FiveK          | Learning Photographic Global Tonal Adjustment with a Database of Input / Output Image Pairs<br />(with ~4% low light images) |          https://data.csail.mit.edu/graphics/fivek           |
|          LRAICE-Dataset           |   A Learning-to-Rank Approach for Image Color Enhancement    |                              -                               |
|         The 500px Dataset         |    Exposure: A White-Box Photo Post-Processing Framework     |                              -                               |
|               DPED                | DSLR-quality photos on mobile devices with deep convolutional networks |              http://people.ee.ethz.ch/~ihnatova              |
|              **LOL**              |     Deep Retinex Decomposition for Low-Light Enhancement     |          https://daooshee.github.io/BMVC2018website          |
|    VV - most challenging cases    | Busting image enhancement and tone-mapping algorithms: A collection of the most challenging cases<br />from [Vassilios Vonikakis](https://sites.google.com/site/vonikakis/) | https://sites.google.com/site/vonikakis/datasets/challenging-dataset-for-enhancement |
|             VV - Phos             | A color image database of 15 scenes captured under different illumination conditions<br />from [Vassilios Vonikakis](https://sites.google.com/site/vonikakis/) |            http://robotics.pme.duth.gr/phos2.html            |
|               SICE                | A large-scale multi-exposure image dataset, which contains 589 elaborately selected high-resolution multi-exposure sequences with 4,413 images |                https://github.com/csjcai/SICE                |
| The Extended Yale Face Database B | The extended Yale Face Database B contains 16128 images of 28 human subjects under 9 poses and 64 illumination conditions. | http://vision.ucsd.edu/~iskwak/ExtYaleDatabase/ExtYaleB.html |
|    the nighttime image dataset    | A dataset which contains source images in bad visibility and their enhanced images processed by different enhancement algorithms |                  http://mlg.idm.pku.edu.cn/                  |
|              VE-LOL               | A large-scale low-light image dataset serving both low/high-level vision with diversified scenes and contents as well as complex degradation in real scenarios, called Vision Enhancement in the LOw-Light condition (VE-LOL). |                                                              |

---



## Methods

### HE-based methods

- **HE** [[Code]](codes/he.m)
- **CLAHE** [[Pdf]](https://ieeexplore.ieee.org/document/109340?arnumber=109340)
  - S.M. Pizer, and R. E. Johnston, “Contrast limited adaptive histogram equalization: speed and effectiveness,”*IEEE Transl. on Consumer Electronics*,1990
- **BPDHE**  [[Code]](codes/bpdhe.m) [[Pdf]](https://ieeexplore.ieee.org/document/4429280)
  - H. Ibrahim and N. S. Pik Kong, "Brightness Preserving Dynamic Histogram Equalization for Image Contrast Enhancement," in *IEEE Transactions on Consumer Electronics*, vol. 53, no. 4, pp. 1752-1758, Nov. 2007
- **DHE** [[Pdf]](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=4266947)
  - Abdullah-Al-Wadud M , Kabir M H , Dewan M A A , et al. A Dynamic Histogram Equalization for Image Contrast Enhancement[J]. *IEEE Transactions on Consumer Electronics*, 2007, 53(2):p.593-600.
- **WTHE** [[Pdf]](https://ieeexplore.ieee.org/document/4266969?arnumber=4266969)
  - Q. Wang and R. K. Ward, "Fast Image/Video Contrast Enhancement Based on Weighted Thresholded Histogram Equalization," in *IEEE Transactions on Consumer Electronics*, vol. 53, no. 2, pp. 757-764, May 2007
- **CVC** [[Pdf]](http://ieeexplore.ieee.org/abstract/document/5773086/)
  -  T. Celik and T. Tjahjadi, "Contextual and Variational Contrast Enhancement," in *IEEE Transactions on Image Processing*, vol. 20, no. 12, pp. 3431-3441, Dec. 2011
- **LDR** [[Web]](http://mcl.korea.ac.kr/cwlee_tip2013/)
  -  Chulwoo Lee, Chul Lee, and Chang-Su Kim, “Contrast enhancement based on layered difference representation,” in *Proc. International Conference on Image Processing (ICIP)*, Orlando, USA, pp. 965-968, Sept.-Oct. 2012. [[doi\]](http://dx.doi.org/10.1109/ICIP.2012.6467022) [[pdf\]](http://mcl.korea.ac.kr/projects/LDR/2012_icip_cwlee_final.pdf) [[pptx\]](http://mcl.korea.ac.kr/projects/LDR/2012_icip_cwlee_poster.pptx)
  - Chulwoo Lee, Chul Lee, and Chang-Su Kim, “Contrast enhancement based on layered difference representation of 2D histograms,” *IEEE Transactions on Image Processing*, vol. 22, no. 12, pp. 5372-5384, Dec. 2013. [[doi\]](http://dx.doi.org/10.1109/TIP.2013.2284059) [[pdf\]](http://mcl.korea.ac.kr/projects/LDR/2013_tip_cwlee_final_hq.pdf)
- **POHE** [[Pdf]](http://150.162.46.34:8080/icassp2013/pdfs/0002444.pdf)
  - Liu, Y.F., Guo, J.M., Lai, B.S. and Lee, J.D., "High efficient contrast enhancement using parametric approximation,"  In 2013 *IEEE International Conference on Acoustics, Speech and Signal Processing*
- **See also: [link](https://github.com/elliestath/HelpTest/blob/c7e269239a9d67bffc60f44ff1cae70d20770748/docs/Image%20Preprocessing.md)**

### Retinex-based methods

:bookmark: retinex

- **SSR** [[Pdf]](https://ieeexplore.ieee.org/document/557356)
  - D. J. Jobson, Z. Rahman and G. A. Woodell, "Properties and performance of a center/surround retinex," in *IEEE Transactions on Image Processing*, vol. 6, no. 3, pp. 451-462, March 1997
- **MSR**  [[Code]](codes/multiscaleRetinex.m) 
- **MSRCR** [[Code1]](http://www.ipol.im/pub/art/2014/107/) [[Code2]](https://github.com/upcAutoLang/MSRCR-Restoration) [[Pdf]](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=597272)
  - Z. Rahman, D. J. Jobson and G. A. Woodell, "Multi-scale retinex for color image enhancement," *Proceedings of 3rd IEEE International Conference on Image Processing*, Lausanne, Switzerland, 1996
  - D. J. Jobson, Z. Rahman and G. A. Woodell, "A multiscale retinex for bridging the gap between color images and the human observation of scenes," in *IEEE Transactions on Image Processing*, vol. 6, no. 7, pp. 965-976, July 1997
- **AMSR** [[Code]](codes/amsr.m) [[Pdf]](https://doi.ieeecomputersociety.org/10.1109/SITIS.2013.19)
  - C. Lee, J. Shih, C. Lien and C. Han,  "Adaptive Multiscale Retinex for Image Contrast Enhancement," in *2013 International Conference on Signal-Image Technology & Internet-Based Systems (SITIS)*, Kyoto, Japan, 2013
- **NPE**  [[Web]](https://shuhangwang.wordpress.com/2015/12/14/naturalness-preserved-enhancement-algorithm-for-non-uniform-illumination-images/) [[Code1]](https://www.dropbox.com/s/096l3uy9vowgs4r/Code.rar) [[Code2]](codes/NPE.rar) [[Pdf]](https://ieeexplore.ieee.org/document/6512558)
  - S. Wang, J. Zheng, H. Hu and B. Li, "Naturalness Preserved Enhancement Algorithm for Non-Uniform Illumination Images," in *IEEE Transactions on Image Processing*, vol. 22, no. 9, pp. 3538-3548, Sept. 2013
- **SRIE** [[Pdf_1]](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=7229296) [[Pdf_2]](https://www.cv-foundation.org/openaccess/content_cvpr_2016/papers/Fu_A_Weighted_Variational_CVPR_2016_paper.pdf) [[Code_1]](codes/PM_SIRE.zip) [[Code_2]](codes/WV_SIRE.zip)
  - X. Fu, Y. Liao, D. Zeng, Y. Huang, X. Zhang and [X. Ding](https://xmu-smartdsp.github.io/teamindex/xhding.html), "A Probabilistic Method for Image Enhancement With Simultaneous Illumination and Reflectance Estimation," in *IEEE Transactions on Image Processing*, vol. 24, no. 12, pp. 4965-4977, Dec. 2015
  - X. Fu, D. Zeng, Y. Huang, X.-P. Zhang, and [X. Ding](https://xmu-smartdsp.github.io/teamindex/xhding.html), “A Weighted Variational Model for Simultaneous Reflectance and Illumination Estimation,” in *2016 IEEE Conference on Computer Vision and Pattern Recognition (CVPR)*, Las Vegas, NV, USA, Jun. 2016
- **LIME** [[Web]](https://sites.google.com/view/xjguo/lime) [[Code_official]](https://drive.google.com/file/d/0BwVzAzXoqrSXb3prWUV1YzBjZzg/view) [[Code1]](https://github.com/Sy-Zhang/LIME) [[Code2]](https://github.com/estija/LIME) [[Code3]](https://github.com/pvnieo/Low-light-Image-Enhancement) [[Pdf]](http://ieeexplore.ieee.org/document/7782813/) [[Report]](https://drive.google.com/file/d/1aph-GUsr_Br2dMLTR3e0kYqAM5aThmj1/view)
  - [X. Guo](https://sites.google.com/view/xjguo/homepage?authuser=0), “LIME: A Method for Low-light IMage Enhancement,” in *Proceedings of the 2016 ACM on Multimedia Conference - MM ’16*, Amsterdam, The Netherlands, 2016
  - [X. Guo](https://sites.google.com/view/xjguo/homepage?authuser=0), Y. Li, and H. Ling, “LIME: Low-Light Image Enhancement via Illumination Map Estimation,” *IEEE Trans. on Image Process.*, vol. 26, no. 2, pp. 982–993, Feb. 2017
- **MF (Multi-deviation Fusion method)** [[Code]](codes/MF.rar) [[Pdf]](https://doi.org/10.1016/j.sigpro.2016.05.031)
  - X. Fu, D. Zeng, Y. Huang, Y. Liao, X. Ding, and J. Paisley, “A fusion-based enhancing method for weakly illuminated images,” *Signal Processing*, vol. 129, pp. 82–96, Dec. 2016
- **JieP**  [[Web]](http://caibolun.github.io/JieP/) [[Code]](https://github.com/caibolun/JieP/) [[Pdf]](http://caibolun.github.io/papers/JieP.pdf)
  - B. Cai, X. Xu, K. Guo, K. Jia, B. Hu, and D. Tao, “A Joint Intrinsic-Extrinsic Prior Model for Retinex,” in *IEEE International Conference on Computer Vision (ICCV)*, 2017.
- **Robust Retinex Model** [[Code1]](https://github.com/martinli0822/Low-light-image-enhancement)  [[Code2]](codes/robustRetinex.m) [[Pdf]](https://www.microsoft.com/en-us/research/uploads/prod/2018/04/2018-TIP-Structure-Revealing-Low-Light-Image-Enhancement-Via-Robust-Retinex-Model.pdf)
  - M. Li, J. Liu, W. Yang, X. Sun, and Z. Guo, “Structure-Revealing Low-Light Image Enhancement Via Robust Retinex Model,” *IEEE Trans. on Image Process.*, vol. 27, no. 6, pp. 2828–2841, Jun. 2018
- **A Smart System for Low-Light Image Enhancement with Color Constancy and Detail Manipulation in Complex Light Environments** [[Pdf]](https://www.mdpi.com/2073-8994/10/12/718/pdf)
  - Z. Rahman, M. Aamir, Y.-F. Pu, F. Ullah, and Q. Dai, “A Smart System for Low-Light Image Enhancement with Color Constancy and Detail Manipulation in Complex Light Environments,” *Symmetry*, vol. 10, no. 12, p. 718, Dec. 2018
- **Fractional-Order Fusion Model for Low-Light Image Enhancement** [[Pdf]](https://www.mdpi.com/2073-8994/11/4/574/pdf)
  - Q. Dai, Y.-F. Pu, Z. Rahman, and M. Aamir, “Fractional-Order Fusion Model for Low-Light Image Enhancement,” *Symmetry*, vol. 11, no. 4, p. 574, Apr. 2019
- **Hybrid L2 −LP Variational Model** [[Pdf]](https://ieeexplore.ieee.org/document/8803197)
  - G. Fu, L. Duan and C. Xiao, "A Hybrid L2 −LP Variational Model For Single Low-Light Image Enhancement With Bright Channel Prior," *2019 IEEE International Conference on Image Processing (ICIP)*, Taipei, Taiwan, 2019
- **NIPM** [[Pdf]](https://ieeexplore.ieee.org/document/8911585)
  - Y. Wu, J. Zheng, W. Song and F. Liu, "Low light image enhancement based on non-uniform illumination prior model," in *IET Image Processing*, vol. 13, no. 13, pp. 2448-2456, 14 11 2019
- **Dual Illumination Estimation for Robust Exposure Correction** [[Pdf]](https://arxiv.org/pdf/1910.13688.pdf) [[Code1]](https://github.com/pvnieo/Low-light-Image-Enhancement)
  - Qing Zhang, Yongwei Nie, and Wei-Shi Zheng. Dual illumination estimation for robust exposure correction. In Computer Graphics Forum, 2019
- **NPLIE** [[Pdf]](https://doi.org/10.36227/techrxiv.12236780.v1)
  - D. A. S. Parihar and K. Singh, “Illumination Estimation for Nature Preserving low-light image enhancement,” May 2020
- **A comparative analysis of illumination estimation based Image Enhancement techniques** [[Pdf]](https://ieeexplore.ieee.org/document/9077919)
- K. Singh and A. S. Parihar, "A comparative analysis of illumination estimation based Image Enhancement techniques," *2020 International Conference on Emerging Trends in Information Technology and Engineering (ic-ETITE)*, Vellore, India, 2020
- **LR3M** [[Pdf]](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9056796)
  - X. Ren, W. Yang, W. Cheng and J. Liu, "LR3M: Robust Low-Light Enhancement via Low-Rank Regularized Retinex Model," in *IEEE Transactions on Image Processing*, vol. 29, pp. 5862-5876, 2020

### CRM&fusion-based methods (Camera Respond Model)

- **A New Low-Light Image Enhancement Algorithm Using Camera Response Model** [[Code]](https://github.com/baidut/OpenCE/blob/master/ours/Ying_2017_ICCV.m) [[Pdf]](http://ieeexplore.ieee.org/document/8265567/) 
  * [Z.Ying](https://baidut.github.io/about/), G. Li, Y. Ren, R. Wang and W. Wang, "A New Low-Light Image Enhancement Algorithm Using Camera Response Model," *2017 IEEE International Conference on Computer Vision Workshops (ICCVW)*, Venice, 2017
- **BIMEF** [[Code]](https://github.com/baidut/BIMEF) [[Pdf]](http://arxiv.org/abs/1711.00591)
  - [Z.Ying](https://baidut.github.io/about/), G. Li, and W. Gao, “A Bio-Inspired Multi-Exposure Fusion Framework for Low-light Image Enhancement,” *arXiv:1711.00591 [cs]*, Nov. 2017
- **Exposure Fusion Framework** [[Web]](https://baidut.github.io/OpenCE/caip2017.html) [[Code_matlab]](https://github.com/baidut/OpenCE/blob/master/ours/Ying_2017_CAIP.m) [[Code_python]](https://github.com/AndyHuang1995/Image-Contrast-Enhancement) [[Pdf]](https://link.springer.com/chapter/10.1007%2F978-3-319-64698-5_4)
  - [Z.Ying](https://baidut.github.io/about/), G. Li, Y. Ren, R. Wang, and W. Wang, “A New Image Contrast Enhancement Algorithm Using Exposure Fusion Framework,” in *International Conference on Computer Analysis of Images and Patterns*, 2017, pp. 36–46.



### Learning-based methods

* **MSR-net** [[Pdf]](https://arxiv.org/pdf/1711.02488v1.pdf)
  * L. Shen, Z. Yue, F. Feng, Q. Chen, S. Liu, and J. Ma, “MSR-net:Low-light Image Enhancement Using Deep Convolutional Network,” *arXiv:1711.02488 [cs]*, Nov. 2017
* **Deep Burst Denoising** [[Pdf]](http://arxiv.org/abs/1712.05790)
  * C. Godard, K. Matzen, and M. Uyttendaele, “Deep Burst Denoising,” *arXiv:1712.05790 [cs, stat]*, Dec. 2017 
* **LLCNN** [[Pdf]](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=8305143)
  * L. Tao, C. Zhu, G. Xiang, Y. Li, H. Jia and X. Xie, "LLCNN: A convolutional neural network for low-light image enhancement," *2017 IEEE Visual Communications and Image Processing (VCIP)*, St. Petersburg, FL, 2017
  * [dataset](http://decsai.ugr.es/cvg/dbimagenes/)
* **LLNet** [[Pdf]](https://doi.org/10.1016/j.patcog.2016.06.008)
  * K. G. Lore, Adedotun Akintayo, and S. Sarkar, “LLNet: A deep autoencoder approach to natural low-light image enhancement,” *Pattern Recognition*, vol. 61, pp. 650–662, Jan. 2017
* **HDRNet** [[Web]](https://groups.csail.mit.edu/graphics/hdrnet/) [[Code]](https://github.com/google/hdrnet) [[Pdf]](https://arxiv.org/abs/1707.02880)
  * M. Gharbi, J. Chen, J. T. Barron, S. W. Hasinoff, and F. Durand, “Deep bilateral learning for real-time image enhancement,” *ACM Trans. Graph.*, vol. 36, no. 4, pp. 1–12, Jul. 2017
* **DSLR Quality Photos on Mobile Devices with Deep Convolutional Networks**  [[Pdf]](https://arxiv.org/abs/1704.02470)
  * A. Ignatov, N. Kobyshev, R. Timofte and K. Vanhoey, "DSLR-Quality Photos on Mobile Devices with Deep Convolutional Networks," *2017 IEEE International Conference on Computer Vision (ICCV)*, Venice, 2017
 * **Retinex-Net** [[Web]](https://daooshee.github.io/BMVC2018website/) [[Code]](https://github.com/weichen582/RetinexNet) [[Pdf]](https://arxiv.org/abs/1808.04560)
   * C. Wei, W. Wang, W. Yang, and J. Liu,"Deep Retinex Decomposition for Low-Light Enhancement." *BMVC 2018*, Oral Presentation.
   * :bookmark: retinex
* **MBLLEN** [[Web]](http://phi-ai.org/project/MBLLEN/default.htm) [[Code]](https://github.com/Lvfeifan/MBLLEN) [[Pdf]](http://bmvc2018.org/contents/papers/0700.pdf)
  * F. Lv, “MBLLEN: Low-light Image/Video Enhancement Using CNNs,” presented at the British Machine Vision Conference, 2018, p. 13.
* **LightenNet** [[Pdf]](https://doi.org/10.1016/j.patrec.2018.01.010)
  * C. Li, J. Guo, F. Porikli, and Y. Pang, “LightenNet: A Convolutional Neural Network for weakly illuminated image enhancement,” *Pattern Recognition Letters*, vol. 104, pp. 15–22, Mar. 2018
  * :bookmark: retinex
* **Learning to See in the Dark** [[Web]](https://cchen156.github.io/SID.html) [[Code]](https://github.com/cchen156/Learning-to-See-in-the-Dark.git) [[Pdf]](https://cchen156.github.io/paper/18CVPR_SID.pdf)
  * C. Chen, Q. Chen, J. Xu, and V. Koltun, “Learning to See in the Dark,” *CVPR 2018*, May 2018
  * real  [dataset](https://github.com/cchen156/Learning-to-See-in-the-Dark)
* **SICE** [[Code]](https://github.com/csjcai/SICE) [[Pdf]](https://doi.org/10.1109/TIP.2018.2794218)
  * J. Cai, S. Gu, and Z. Lei, “Learning a Deep Single Image Contrast Enhancer from Multi-Exposure Images,” *IEEE Transactions on Image Processing*, vol. 27, no. 4, pp. 2049–2062, 2018
* **White-Box** [[Code]](https://github.com/yuanming-hu/exposure) [[Pdf]](https://doi.org/10.1145/3181974)
  * [Y. Hu](http://taichi.graphics/me/), H. He, C. Xu, B. Wang, and S. Lin, “Exposure: A White-Box Photo Post-Processing Framework,” *ACM Trans. Graph.*, vol. 37, no. 2, pp. 1–17, Jul. 2018, doi: [10.1145/3181974](https://doi.org/10.1145/3181974).
* **GLADNet** [[Web]](https://daooshee.github.io/fgworkshop18Gladnet/) [[Code]](https://github.com/weichen582/GLADNet) [[Pdf]](https://github.com/daooshee/fgworkshop18Gladnet/blob/master/wwj_fg2018.pdf)
  * W. Wang, C. Wei, W. Yang and J. Liu, "GLADNet: Low-Light Enhancement Network with Global Awareness," *2018 13th IEEE International Conference on Automatic Face & Gesture Recognition*
  * synthetic [dataset](https://daooshee.github.io/fgworkshop18Gladnet/) generated from RAW images
* **A Pipeline Neural Network for Low-Light Image Enhancement** [[Pdf]](https://ieeexplore.ieee.org/document/8607964/)
  * Y. Guo, X. Ke, J. Ma, and J. Zhang, “A Pipeline Neural Network for Low-Light Image Enhancement,” *IEEE Access*, vol. 7, pp. 13737–13744, 2019
* **KinD** [[Code]](https://github.com/zhangyhuaee/KinD) [[Code+]](https://github.com/zhangyhuaee/KinD_plus) [[Pdf]](http://arxiv.org/abs/1905.04161)
  * Y. Zhang, J. Zhang, and [X. Guo](https://sites.google.com/view/xjguo/homepage?authuser=0),, “Kindling the Darkness: A Practical Low-light Image Enhancer,” *arXiv:1905.04161 [cs]*, May 2019
* **Learning Digital Camera Pipeline for Extreme Low-Light Imaging** [[Pdf]](https://arxiv.org/abs/1904.05939)
  * S. Waqas Zamir, A. Arora, S. Khan, F. Shahbaz Khan, and L. Shao, “Learning Digital Camera Pipeline for Extreme Low-Light Imaging,” *arXiv preprint arXiv:1904.05939*, 2019.
* **End-to-End Denoising of Dark Burst Images Using Recurrent Fully Convolutional Networks** [[Pdf]](https://arxiv.org/abs/1904.07483v1)
  * D. Zhao, L. Ma, S. Li, and D. Yu, “End-to-End Denoising of Dark Burst Images Using Recurrent Fully Convolutional Networks,” *arXiv:1904.07483 [cs]*, Apr. 2019 
* **A Bit Too Much** [[Pdf]](https://ieeexplore.ieee.org/document/8747325/)
  * P. Chandramouli, Claudio Bruschini, and  and A. Kolb, “A Bit Too Much? High Speed Imaging from Sparse Photon Counts,” in *2019 IEEE International Conference on Computational Photography (ICCP)*, Tokyo, Japan, May 2019
* **DeepISP** [[Pdf]](https://arxiv.org/abs/1801.06724)
  * E. Schwartz, R. Giryes, and A. M. Bronstein, “DeepISP: Towards Learning an End-to-End Image Processing Pipeline,” *IEEE Trans. on Image Process.*, vol. 28, no. 2, pp. 912–923, Feb. 2019
* **DeepUPE** [[Code]](https://github.com/wangruixing/DeepUPE) [[Pdf]](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=8953588)
  * R. Wang, Q. Zhang, C. Fu, X. Shen, W. Zheng and J. Jia, "Underexposed Photo Enhancement Using Deep Illumination Estimation," *2019 IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR)*, Long Beach, CA, USA, 2019
  * :bookmark: retinex
* **Low-Light Image Enhancement via a Deep Hybrid Network**  [[Pdf]](https://ieeexplore.ieee.org/document/8692732)
  * W. Ren *et al*., "Low-Light Image Enhancement via a Deep Hybrid Network," in *IEEE Transactions on Image Processing*, vol. 28, no. 9, pp. 4364-4375, Sept. 2019
* **RDGAN** [[Code]](https://github.com/WangJY06/RDGAN/) [[Pdf]](https://ieeexplore.ieee.org/document/8785047)
  * J. Wang, W. Tan, X. Niu and B. Yan, "RDGAN: Retinex Decomposition Based Adversarial Learning for Low-Light Enhancement," *2019 IEEE International Conference on Multimedia and Expo (ICME)*, Shanghai, China, 2019
  * :bookmark: retinex
* **Deep Fusion Networks** [[Pdf]](https://ieeexplore.ieee.org/document/8803041)
  * Y. Cheng, J. Yan and Z. Wang, "Enhancement of Weakly Illuminated Images by Deep Fusion Networks," *2019 IEEE International Conference on Image Processing (ICIP)*, Taipei, Taiwan, 2019
* **Llrnet** [[Pdf]](https://ieeexplore.ieee.org/document/8803765)
  * S. Malik and R. Soundararajan, "Llrnet: A Multiscale Subband Learning Approach for Low Light Image Restoration," *2019 IEEE International Conference on Image Processing (ICIP)*, Taipei, Taiwan, 2019
* **Low-Lightgan** [[Pdf]](https://ieeexplore.ieee.org/document/8803328)
  * G. Kim, D. Kwon and J. Kwon, "Low-Lightgan: Low-Light Enhancement Via Advanced Generative Adversarial Network With Task-Driven Training," *2019 IEEE International Conference on Image Processing (ICIP)*, Taipei, Taiwan, 2019
* **EnlightenGAN** [[Code]](https://github.com/TAMU-VITA/EnlightenGAN) [[Pdf]](https://arxiv.org/abs/1906.06972)
  * Y. Jiang *et al.*, “EnlightenGAN: Deep Light Enhancement without Paired Supervision,” *arXiv:1906.06972 [cs, eess]*, Jun. 2019
* **An Effective Network with ConvLSTM for Low-Light Image Enhancement** [[Pdf]](https://doi.org/10.1007/978-3-030-31723-2_19)
  * Y. Xiang, Y. Fu, L. Zhang, and H. Huang, “An Effective Network with ConvLSTM for Low-Light Image Enhancement,” in *Pattern Recognition and Computer Vision*, Cham, 2019.
* **Enhancing Low Light Videos by Exploring High Sensitivity Camera Noise** [[Pdf]](https://ieeexplore.ieee.org/document/9011000)
  * W. Wang, X. Chen, C. Yang, X. Li, X. Hu and T. Yue, "Enhancing Low Light Videos by Exploring High Sensitivity Camera Noise," 2019 IEEE/CVF International Conference on Computer Vision (ICCV), Seoul, Korea (South), 2019, pp. 4110-4118, doi: 10.1109/ICCV.2019.00421.
* **Low-Light Image Enhancement with Attention and Multi-level Feature Fusion** [[Pdf]](https://ieeexplore.ieee.org/document/8794872)
  * L. Wang, G. Fu, Z. Jiang, G. Ju and A. Men, "Low-Light Image Enhancement with Attention and Multi-level Feature Fusion," *2019 IEEE International Conference on Multimedia & Expo Workshops (ICMEW)*, Shanghai, China, 2019
* **Zero-DCE** [[Web]](https://li-chongyi.github.io/Proj_Zero-DCE.html) [[Code]](https://github.com/Li-Chongyi/Zero-DCE) [[Pdf]](https://openaccess.thecvf.com/content_CVPR_2020/papers/Guo_Zero-Reference_Deep_Curve_Estimation_for_Low-Light_Image_Enhancement_CVPR_2020_paper.pdf)
  * C. Guo *et al.*, “Zero-Reference Deep Curve Estimation for Low-Light Image Enhancement,” in *2020 IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR)*, Seattle, WA, USA, Jun. 2020, pp. 1777–1786, doi: [10.1109/CVPR42600.2020.00185](https://doi.org/10.1109/CVPR42600.2020.00185).
* **Learning to Restore Low-Light Images via Decomposition-and-Enhancement** [[Pdf]](https://ieeexplore.ieee.org/document/9156446)
  * K. Xu, X. Yang, B. Yin and R. W. H. Lau, "Learning to Restore Low-Light Images via Decomposition-and-Enhancement," *2020 IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR)*, Seattle, WA, USA, 2020, pp. 2278-2287, doi: 10.1109/CVPR42600.2020.00235.
* **DRBN** [[Pdf]](https://ieeexplore.ieee.org/document/9156559)
  * W. Yang, S. Wang, Y. Fang, Y. Wang and J. Liu, "From Fidelity to Perceptual Quality: A Semi-Supervised Approach for Low-Light Image Enhancement," 2020 IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR), Seattle, WA, USA, 2020, pp. 3060-3069, doi: 10.1109/CVPR42600.2020.00313.
*  **STARnet**[[Web]](https://alterzero.github.io/projects/STAR.html) [[Code]](https://github.com/alterzero/STARnet) [[Pdf]](https://alterzero.github.io/projects/star_cvpr2020.pdf)
  * Muhammad Haris, Greg Shakhnarovich, and Norimichi Ukita, "Space-Time-Aware Multi-Resolution Video Enhancement", Proc. of IEEE Conference on Computer Vision and Pattern Recognition (CVPR), 2020.
*  **DeepLPF** [[Code]](https://github.com/sjmoran/DeepLPF)[[Pdf]](https://arxiv.org/abs/2003.13985)
  * Moran, S., Marza, P., McDonagh, S., Parisot, S., Slabaugh, G. DeepLPF: Deep Local Parametric Filters for Image Enhancement, in: Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR), 2020.
* **Image-Adaptive-3DLUT** [[Code]](https://github.com/HuiZeng/Image-Adaptive-3DLUT) [[Pdf]](https://ieeexplore.ieee.org/document/9206076)
  * H. Zeng, J. Cai, L. Li, Z. Cao and L. Zhang, "Learning Image-adaptive 3D Lookup Tables for High Performance Photo Enhancement in Real-time," in IEEE Transactions on Pattern Analysis and Machine Intelligence, 2020.

### Other methods

- **Fast centre-surround contrast modification** [[Pdf]](https://ieeexplore.ieee.org/document/4455541)
  - V. Vonikakis, I. Andreadis and A. Gasteratos, "Fast centre-surround contrast modification," in *IET Image Processing*, vol. 2, no. 1, pp. 19-34, Feb. 2008
- **Fast efficient algorithm for enhancement of low lighting video** [[Pdf]](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=6012107) [[Code]](codes/XuanDong-Method.m)
  - Xuan Dong *et al*., "Fast efficient algorithm for enhancement of low lighting video," *2011 IEEE International Conference on Multimedia and Expo*, Barcelona, 2011
- **ALSM** [[Pdf]](https://doi.org/10.1109/TIP.2019.2922106)
  - Y.-F. Wang, H.-M. Liu, and Z.-W. Fu, “Low-Light Image Enhancement via the Absorption Light Scattering Model,” *IEEE Transactions on Image Processing*, vol. 28, no. 11, pp. 5679–5690, Nov. 2019
- **Maximum and Guided Filters** [[Pdf]](file:///D:/ZoteroData/storage/JBKLL8T5/8803591.html)
  - D. Zhu, G. Chen, P. N. Michelini and H. Liu, "Fast Image Enhancement Based on Maximum and Guided Filters," *2019 IEEE International Conference on Image Processing (ICIP)*, Taipei, Taiwan, 2019

### Latest methods

* Y. Zhang, X. Di, B. Zhang, and C. Wang, “Self-supervised Image Enhancement Network: Training with Low Light Images Only,” *arXiv:2002.11300 [cs, eess]*, Feb. 2020, Accessed: May 25, 2020. [Online]. Available: http://arxiv.org/abs/2002.11300.
* F. Lv, Y. Li, and F. Lu, “Attention Guided Low-light Image Enhancement with a Large Scale Low-light Simulation Dataset,” *arXiv:1908.00682 [cs, eess]*, Mar. 2020, Accessed: May 25, 2020. [Online]. Available: http://arxiv.org/abs/1908.00682.
* X. Li *et al.*, “Visual Perception Model for Rapid and Adaptive Low-light Image Enhancement,” *arXiv:2005.07343 [cs, eess]*, May 2020, Accessed: May 25, 2020. [Online]. Available: http://arxiv.org/abs/2005.07343.
* W. Xiong, D. Liu, X. Shen, C. Fang, and J. Luo, “Unsupervised Real-world Low-light Image Enhancement with Decoupled Networks,” *arXiv:2005.02818 [cs, eess]*, May 2020, Accessed: May 25, 2020. [Online]. Available: http://arxiv.org/abs/2005.02818.
* Q. Fu, X. Di, and Y. Zhang, “Learning an Adaptive Model for Extreme Low-light Raw Image Processing,” *arXiv:2004.10447 [cs, eess]*, Apr. 2020, Accessed: May 25, 2020. [Online]. Available: http://arxiv.org/abs/2004.10447.

### Related works

-  **Improving the robustness in feature detection by local contrast enhancement** [[Pdf]](https://ieeexplore.ieee.org/document/6295482)
  - V. Vonikakis, D. Chrysostomou, R. Kouskouridas and A. Gasteratos, "Improving the robustness in feature detection by local contrast enhancement," *2012 IEEE International Conference on Imaging Systems and Techniques Proceedings*, Manchester, 2012
  - [dataset VV](https://sites.google.com/site/vonikakis/datasets)
-  **Automatic Photo Adjustment Using Deep Neural Networks** [[Web]](https://sites.google.com/site/homepagezhichengyan/home/dl_img_adjust) [[Code]](https://github.com/stephenyan1984/dl-image-enhance/wiki) [[Pdf]](https://arxiv.org/abs/1412.7725v2)
  - Z. Yan, H. Zhang, B. Wang, S. Paris, and Y. Yu, “Automatic Photo Adjustment Using Deep Neural Networks,” *ACM Transactions on Graphics*, 2015.
-  **Distort-and-Recover** [[Code]](https://sites.google.com/view/distort-and-recover/) [[Pdf]](https://doi.org/10.1109/CVPR.2018.00621)
   -  J. Park, J. Y. Lee, D. Yoo, and I. S. Kweon, “Distort-and-Recover: Color Enhancement using Deep Reinforcement Learning,” presented at the CVPR, 2018, doi: [10.1109/CVPR.2018.00621](https://doi.org/10.1109/CVPR.2018.00621).

---



## Reviews

-  **Benchmarking Low-Light Image Enhancement and Beyond** [[Pdf]](https://link.springer.com/article/10.1007%2Fs11263-020-01418-8)
   -  J. Liu, D. Xu, W. Yang, M. Fan, and H. Huang, “Benchmarking Low-Light Image Enhancement and Beyond,” *Int J Comput Vis*, Jan. 2021, doi: [10.1007/s11263-020-01418-8](https://doi.org/10.1007/s11263-020-01418-8).
   -  :high_brightness: <font color='red'> **highlight!** </font>

---



## Metrics

- MSE
- SSIM
- entropy (DE)
- EME
- AB
- PixDist
- LOE

---



## Blogs & Slices

- [重磅干货｜低光图像处理方案](https://zhuanlan.zhihu.com/p/140926754), by [Happy](https://www.zhihu.com/people/wsp_tcl)
- [基于深度学习的图像增强调研](https://zhuanlan.zhihu.com/p/63218165)， by [庄小p](https://www.zhihu.com/people/zhuang-xiao-p)
- [基于深度学习的低光照图像增强方法总结 (2017-2019)](https://blog.csdn.net/hyk_1996/article/details/99641652), by [hyk_1996](https://blog.csdn.net/hyk_1996)
- [图像暗光增强-直方图增强](https://blog.csdn.net/Cody_/article/details/102517445)， by [若，只如初见](https://blog.csdn.net/Cody_)
- [Retinex算法在暗光增强应用以及Python实现](https://blog.csdn.net/Cody_/article/details/104793796)， by [若，只如初见](https://blog.csdn.net/Cody_)
- [Learning based methods in low light image enhancement](slides/dl-low-light-imaging-enhancement-review.pdf), by [Zhihong Zhang](https://github.com/dawnlh)



---



## Reference

- https://zhuanlan.zhihu.com/p/140926754
- https://github.com/baidut/OpenCE
- https://github.com/tiandaoxiaowu/image-enhancement-about-Retinex



## Supplementary

### Tags

- :high_brightness: <font color='red'> **highlight!** </font>
- :bookmark: retinex