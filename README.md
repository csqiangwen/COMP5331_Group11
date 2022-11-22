# ST2Vec++

<div align=center>
<img src=./figs/framework.jpg width="100%" ></img>
</div>

## Introduction
This is a COMP5311 project by WEN Qiang, XU Shuanjie, ZHU Jiapeng.

## Requirements

- Ubuntu OS
- Python >= 3.5 (Anaconda3 is recommended)
- PyTorch 1.4+
- A Nvidia GPU with cuda 10.2+

## Reproducibility & Training

1. Data preprocessing (Time embedding and node embedding)

   ```shell
   python preprocess.py
   ```

2. Ground truth generating (It will take a while...)

   ```shell
   python spatial_similarity.py
   python temporal_similarity.py
   ```

3. Triplets generating

   ```shell
   python data_utils.py
   ```

4. Training

   ```shell
   python main.py
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
