# ST2Vec_new

<div align=center>
<img src=./fig/framework.jpg width="80%" ></img>
</div>


## Modification
- We only modified the file "model_network.py";
- We replace the LSTM module with the self-attention module;
- Instead of directly feeding the vector [temporal-embedding+spatial embedding] into the LSTM, we adopt a self-attention module for temporal and spatial embeddings, respectively. Then, we add "LayerNorm" layer for nomarlizing the vector [temporal-embedding+spatial embedding].


## Experiments (2022-11-04)
|  T-Drive   | TP     | TP     | TP     | DITA   | DITA   | DITA   | LCRS   | LCRS   | LCRS   |
|------------|--------|--------|--------|--------|--------|--------|--------|--------|--------|
|            | HR@10  | HR@50  | R10@50 | HR@10  | HR@50  | R10@50 | HR@10  | HR@50  | R10@50 |
| ST2Vec     | 0.4624 | 0.5868 | 0.8361 | 0.3773 | 0.5037 | 0.7031 | 0.1806 | 0.5469 | 0.7293 |
| ST2Vec_new | 0.5039 | 0.6150 | 0.8737 | 0.4211 | 0.5241 | 0.8102 | 0.1744 | 0.5278 | 0.6438 |

