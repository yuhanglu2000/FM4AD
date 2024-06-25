# Prerequisites

**Please ensure you have prepared the environment and the nuScenes dataset.**

**Note: ** Please change the "data_root" of each config file to your own (since it's not a relative path)

# Train and Test

## Train  with multi GPUs 
```shell
cd /path/to/VAD
conda activate vad
./tools/dist_train.sh [path to the config file] [num of GPUs]
```

## Eval  with 1 GPU
```shell
cd /path/to/VAD
conda activate vad
CUDA_VISIBLE_DEVICES=0 python tools/test.py [path to the config file] [/path/to/ckpt.pth] --launcher none --eval bbox --tmpdir tmp
```

