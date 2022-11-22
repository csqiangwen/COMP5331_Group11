# ST2Vec_new

<div align=center>
<img src=./fig/framework.jpg width="80%" ></img>
</div>


## Modification
- We only modified the file "model_network.py";
- We replace the LSTM module with the self-attention module;
- Instead of directly feeding the vector [temporal-embedding + spatial-embedding] into the LSTM, we adopt a self-attention module for temporal and spatial embeddings, respectively. Then, we add "LayerNorm" layer for nomarlizing the vector [temporal-embedding + spatial-embedding].


## Experiments (2022-11-22)
<div align=center>
<img src=./figs/tdrive.pic.jpg width="80%" ></img>
</div>
<div align=center>
<img src=./figs/roma.pic.jpg width="80%" ></img>
</div>
<div align=center>
<img src=./figs/ablation.pic.jpg width="80%" ></img>
</div>
