# QANet
A Pytorch implementation of [QANet](https://arxiv.org/pdf/1804.09541.pdf)  
The code is mostly based on the two repositories:
[hengruo/QANet-pytorch](https://github.com/hengruo/QANet-pytorch)
[NLPLearn/QANet](https://github.com/NLPLearn/QANet)

## Performance
| Training Steps | Size | Attention Heads |  EM  |  F1  |
|:--------------:|:----:|:---------------:|:----:|:----:|
|     35,000     |  96  |        1        | 65.3 | 76.3 |
|     60,000     |  96  |        1        | 66.2 | 77.2 |

## Requirements
  * python 3.6
  * pytorch 0.4.0
  * tqdm
  * spacy 2.0.11
  * tensorboardX
  * absl-py

## Usage
Download and preprocess the data
```bash
# download SQuAD and Glove
$ sh download.sh
# preprocess
$ python3.6 main.py --mode data
```

Train the model
```bash
# model/model.pt will be generated every epoch
$ python3.6 main.py --mode train
```
## Tensorboard
```bash
# Run tensorboard for visualisation
$ tensorboard --logdir ./log/
```
## TODO
- [X] Add Exponential Moving Average
- [ ] Reach the performance of the paper, still not sure where to improve.
