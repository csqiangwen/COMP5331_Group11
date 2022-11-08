# ST2Vec_new

<div align=center>
<img src=./fig/framework.jpg width="80%" ></img>
</div>


## Modification
- We only modified the file "model_network.py";
- We replace the LSTM module with the self-attention module;
- Instead of directly feeding the vector [temporal-embedding + spatial-embedding] into the LSTM, we adopt a self-attention module for temporal and spatial embeddings, respectively. Then, we add "LayerNorm" layer for nomarlizing the vector [temporal-embedding + spatial-embedding].


## Experiments (2022-11-07)
|  T-Drive   | TP     | TP     | TP     | DITA   | DITA   | DITA   | LCRS   | LCRS   | LCRS   |
|------------|--------|--------|--------|--------|--------|--------|--------|--------|--------|
|            | HR@10  | HR@50  | R10@50 | HR@10  | HR@50  | R10@50 | HR@10  | HR@50  | R10@50 |
| ST2Vec     | 0.4624 | 0.5868 | 0.8361 | 0.3773 | 0.5037 | 0.7031 | **0.1806** | **0.5469** | **0.7293** |
| ST2Vec_new | **0.4801** | **0.5950** | **0.8556** | **0.4211** | **0.5241** | **0.8102** | 0.1744 | 0.5278 | 0.6438 |
| ST2Vec_new_wo_norm | 0.4553 | 0.5838 | 0.8482 | 0.3986 | 0.5159 | 0.7931 | N/A | N/A | N/A |
| ST2Vec_new_wo_intra | 0.4679 | 0.5816 | 0.8522 | 0.4057 | 0.5047 | 0.7934 | N/A | N/A | N/A |

|    Roma    | TP     | TP     | TP     | DITA   | DITA   | DITA   | LCRS   | LCRS   | LCRS   |
|------------|--------|--------|--------|--------|--------|--------|--------|--------|--------|
|            | HR@10  | HR@50  | R10@50 | HR@10  | HR@50  | R10@50 | HR@10  | HR@50  | R10@50 |
| ST2Vec     | 0.3834 | 0.5051 | 0.7221 | 0.2421 | 0.3689 | 0.5614 | **0.3178** | **0.3942** | **0.7244** |
| ST2Vec_new | **0.4635** | **0.5694** | **0.8052** | **0.3668** | **0.4916** | **0.7416** | 0.1336 | 0.2110 | 0.3377 |
| ST2Vec_new_wo_norm | N/A | N/A | N/A | 0.2848 | 0.3773 | 0.6800 | N/A | N/A | N/A |
| ST2Vec_new_wo_intra | 0.3291 | 0.4313 | 0.7129 | 0.2416 | 0.3741 | 0.5711 | N/A | N/A | N/A |
