# ST2Vec

<div align=center>
<img src=./fig/framework.jpg width="80%" ></img>
</div>


This is our Pytorch implementation for the paper:

> Ziquan Fang, Yuntao Du, Xinjun Zhu, Danlei Hu, Lu Chen, Yunjun Gao and Christian S. Jensen. (2022). Spatio-Temporal Trajectory Similarity Learning in Road Networks. Paper in [ACM DL](https://dl.acm.org/doi/abs/10.1145/3534678.3539375) or Paper in [arXiv](https://arxiv.org/abs/2112.09339). In KDD'22, Washington DC, USA, August 14-18, 2022.

## Modification
- We only modified the file "model_network.py";
- We replace the LSTM module with the self-attention module;
- Instead of directly feeding the vector [temporal-embedding+spatial embedding] into the LSTM, we adopt a self-attention module for temporal and spatial embeddings, respectively. Then, we add "LayerNorm" layer for nomarlizing the vector [temporal-embedding+spatial embedding]


## Experiments (2022-11-04)
|            | TP     | TP     | TP     | DITA   | DITA   | DITA   |
|------------|--------|--------|--------|--------|--------|--------|
|            | HR@10  | HR@50  | R10@50 | HR@10  | HR@50  | R10@50 |
| ST2Vec_new | 0.5039 | 0.6150 | 0.8737 | 0.4445 | 0.5376 | 0.8314 |

