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

## Results

This method outperforms the state of the art approaches and explains the result. 

Method | Precision@6 | Recall@6 | F1@6 | MAP@6 |
--- | --- | --- | --- |--- |
TTIR | 0.492 | 0.756 | 0.596 | 0.805 |
CNN | 0.484 | 0.744 | 0.586 | 0.795 | 
ANN | 0.476 | 0.732 | 0.566 | 0.785 |

