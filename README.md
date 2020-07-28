# Interpretable Contextual Team-aware Item Recommendation: Application in Multiplayer Online Battle Arena Game

See paper in [arXiv]()

![tir-model](https://github.com/ojedaf/IC-TIR-Lol/blob/master/images/model-1.png)

We release the PyTorch code of the TTIR model.

## Content

- [Prerequisites](#prerequisites)
- [Dataset](#dataset)
- [Code](#code)
- [Result](#testing)

## Prerequisites

The code is built with following libraries:

- [PyTorch](https://pytorch.org/) 1.0 or higher
- [Comet-ml](https://www.comet.ml/site/)
- [PyTorchLightning](https://github.com/PyTorchLightning/pytorch-lightning)
- [Google Colab](https://colab.research.google.com/)

## Dataset

The used dataset is available [here](https://drive.google.com/drive/folders/1lsCjmVrOA0stNiUguGWKN46fEqzzsXPH?usp=sharing)

## Code

We develop this project using Google Colab. That's why you must have a Google Account and the dataset in a gDrive folder. Furthermore, you have to change these paths according to the location of the dataset. 

```python
train_path = '/content/gdrive/My Drive/Proyecto_RecSys/dataset/train_splits.pkl'
test_path = '/content/gdrive/My Drive/Proyecto_RecSys/dataset/test_splits.pkl'
champion_path = '/content/gdrive/My Drive/Proyecto_RecSys/dataset/champion_types.pkl'

```
