# Relational Surrogate Loss Learning (ReLoss)
Official implementation for paper "[Relational Surrogate Loss Learning](https://openreview.net/forum?id=dZPgfwaTaXv)" in International Conference on Learning Representations (ICLR) 2022. 

By Tao Huang, Zekang Li, Hua Lu, Yong Shan, Shusheng Yang, Yang Feng, Fei Wang, Shan You, Chang Xu.

## Usage
### Install ReLoss
```shell
pip install git+https://github.com/hunto/ReLoss.git
```
Or install for development:
```shell
git clone https://github.com/hunto/ReLoss
cd ReLoss
pip install -e .
```

### Train models with ReLoss
All the inputs and outputs of ReLoss are the same as the original loss.
* classification
    ```python
    from reloss.cls import ReLoss
    loss_fn = ReLoss()
    ```
* human pose estimation
    ```python
    from reloss.pose import ReLoss
    loss_fn = ReLoss(heatmap_size=(64, 48))
    ```
* non-autoregressive neural machine translation

    The loss should be used in fairseq framework. You can add it into the criterions.

### Train ReLoss

You can train your own ReLoss, please see [example/train_reloss/README.md](example/train_reloss/README.md) for instructions.


## Citation
```
@inproceedings{
huang2022relational,
title={Relational Surrogate Loss Learning},
author={Tao Huang and Zekang Li and Hua Lu and Yong Shan and Shusheng Yang and Yang Feng and Fei Wang and Shan You and Chang Xu},
booktitle={International Conference on Learning Representations},
year={2022},
url={https://openreview.net/forum?id=dZPgfwaTaXv}
}
```
