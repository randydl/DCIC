# DCIC

PMLR, 2020: Label-Noise Robust Domain Adaptation.

This is the basic implementation code (unofficial) for the paper:
[Label-Noise Robust Domain Adaptation](http://proceedings.mlr.press/v119/yu20c/yu20c.pdf). \
Xiyu Yu, Tongliang Liu, Mingming Gong, Kun Zhang, Kayhan Batmanghelich, Dacheng Tao.

## Dependencies
The methods are implemented by PyTorch on NVIDIA GeForce RTX 3080 Ti GPU. The environment is as bellow:
- [Ubuntu 20.04 Desktop](https://ubuntu.com/download)
- [PyTorch](https://PyTorch.org/), version = 1.10.2
- [CUDA](https://developer.nvidia.com/cuda-downloads), version = 11.3
- [Anaconda3](https://www.anaconda.com/)

### Install requirements.txt
~~~
pip install -r requirements.txt
~~~

## Experiments
I verify the effectiveness of the proposed method on synthetic noisy datasets. In this repository, I provide the used datasets in the folder "data" (mnist.npz, usps.npz). Here is a training example:
```bash
python main.py \
    --source mnist \
    --target usps \
    --batch_size 128 \
    --noise_rate 0.2 \
    --random_state 1
```
If you find this code useful in your research, please cite
```bash
@inproceedings{liu2020dcic,
  title={Label-Noise Robust Domain Adaptation},
  author={Xiyu Yu, Tongliang Liu, Mingming Gong, Kun Zhang, Kayhan Batmanghelich, Dacheng Tao},
  booktitle={PMLR},
  year={2020}
}
```