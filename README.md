# ST2Vec++

<div align=center>
<img src=./figs/framework.jpg width="100%" ></img>
</div>

## Introduction
This is a COMP5311 project by WEN Qiang, XU Shuangjie, ZHU Jiapeng.

## Requirements

- Ubuntu OS
- Python >= 3.5 (Anaconda3 is recommended)
- PyTorch 1.4+
- A Nvidia GPU with cuda 10.2+

## Data Preparation

1. Data preprocessing (Time embedding and node embedding)

   ```shell
   python3 preprocess.py
   ```

2. Ground truth generating (It will take a while...)

   ```shell
   python3 spatial_similarity.py
   python3 temporal_similarity.py
   ```

3. Triplets generating

   ```shell
   python3 data_utils.py
   ```
## Training

1. Training

   ```shell
   python3 main.py
   ```
   
## Testing

1. We share the models pretrained on T-Drive dataset in the directory './model/'

2. Change 'load_model_name' and turn 'STsim.ST_eval()' on in the file 'main.py'

   ```shell
   python3 main.py
   ```

## Experiments
<div align=center>
<img src=./figs/tdrive.pic.jpg width="80%" ></img>
</div>
<div align=center>
<img src=./figs/roma.pic.jpg width="80%" ></img>
</div>
<div align=center>
<img src=./figs/ablation.pic.jpg width="80%" ></img>
</div>
