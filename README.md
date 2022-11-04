# ST2Vec

<div align=center>
<img src=./fig/framework.jpg width="80%" ></img>
</div>


This is our Pytorch implementation for the paper:

> Ziquan Fang, Yuntao Du, Xinjun Zhu, Danlei Hu, Lu Chen, Yunjun Gao and Christian S. Jensen. (2022). Spatio-Temporal Trajectory Similarity Learning in Road Networks. Paper in [ACM DL](https://dl.acm.org/doi/abs/10.1145/3534678.3539375) or Paper in [arXiv](https://arxiv.org/abs/2112.09339). In KDD'22, Washington DC, USA, August 14-18, 2022.

## Modification
- we 


## Experiments (2022-11-)
| Input        | Loss         | Network      | Output      | Tese Size    | PSNR_u    | PSNR_L    | iterarion    |
| ----------- | ----------- | ----------- | ----------- | ----------- | ----------- | ----------- | ----------- |
| LDR & HDR | L1(w/o tm) & VGG(w tm) & GAN | no depth-wise, downx2 | w/o tm | 0.5 | 38.2018 | 37.3917 | 81000 |
| LDR & HDR & Dark & Bright | L1(w/o tm) & VGG(w tm) & GAN | no depth-wise, downx2 | w/o tm | 0.5 | 38.6227 | 39.2300 | 43000 |
| LDR & HDR & Dark & Bright | L1(w/o tm) & VGG(w tm) | depth-wise SA and res1, downx2 | w/o tm | 0.5 | 41.1059 | 40.3678 | 198000 |
| LDR & HDR & Dark & Bright (1) | L1(w/o tm) & VGG(w tm) | depth-wise SA, downx2 | w/o tm | 0.5 | 41.7571 | 41.6140 | 213000 |
| LDR & HDR & Dark & Bright (2) | L1(w/o tm) & VGG(w tm) | depth-wise SA, downx3 | w/o tm | full | 40.3329 | 38.6264 | 447000 |
| LDR & HDR & Dark & Bright (3) | L1(w/o tm) & VGG(w tm) | restoremers (w/o bias) w skip, downx2 | w/o tm | full | 40.8111 | 39.6580 | 103000 |
| LDR & HDR & Dark & Bright (4) | L1(w/o tm) & VGG(w tm) | restoremers (w bias) w skip, downx2 (pixelshuffle w/o norm) | w/o tm | full | **43.2394** | **41.3333** | 275000 |
| LDR & HDR & Dark & Bright (5) | L1(w/o tm) & VGG(w tm) | restoremers (w bias) w skip, downx2 (pixelshuffle w norm) | w/o tm | full | N/A | N/A | N/A |


