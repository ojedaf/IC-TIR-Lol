# Interpretable Contextual Team-aware Item Recommendation: Application in Multiplayer Online Battle Arena Game

<a href="https://colab.research.google.com/github/ojedaf/IC-TIR-Lol/blob/master/model.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>

See paper in [arXiv](https://arxiv.org/abs/2007.15236)

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

The used dataset is available [here](https://drive.google.com/drive/folders/1lsCjmVrOA0stNiUguGWKN46fEqzzsXPH?usp=sharing).

## Code

We develop this project using Google Colab. That's why you must have a Google Account and the dataset in a gDrive folder. Furthermore, you have to change these paths according to the location of the dataset.

```python
train_path = '/content/gdrive/My Drive/Proyecto_RecSys/dataset/train_splits.pkl'
test_path = '/content/gdrive/My Drive/Proyecto_RecSys/dataset/test_splits.pkl'
champion_path = '/content/gdrive/My Drive/Proyecto_RecSys/dataset/champion_types.pkl'
```

And the comet parameters (api_key, project_name, workspace)

```python
comet_logger = CometLogger(
    experiment_name=conf['exp_name'],
    api_key = 'YOUR_KEY',
    project_name="YOUR_PROJECT_NAME",
    workspace = 'YOUR_WORKSPACE'
)
```

## Baselines

This work uses the proposed models in [Data mining for item recommendation in MOBA games paper](https://github.com/vgaraujov/RecSysLoL) as baselines.

## Results

This method outperforms the state of the art approaches and explains the result. 

Method | Precision@6 | Recall@6 | F1@6 | MAP@6 |
--- | --- | --- | --- |--- |
TTIR | 0.492 | 0.756 | 0.596 | 0.805 |
CNN | 0.484 | 0.744 | 0.586 | 0.795 | 
ANN | 0.476 | 0.732 | 0.566 | 0.785 |

![tir-att](https://github.com/ojedaf/IC-TIR-Lol/blob/master/images/attn-1.png)

## Citation

If you find this repository useful for your research, please consider citing our paper: 
```
@inproceedings{ttir,
    author = {Villa, Andrés and Araujo, Vladimir and Cattan, Francisca and Parra, Denis},
    title = {Interpretable Contextual Team-aware Item Recommendation: Application in Multiplayer Online Battle Arena Games},
    year = {2020},
    isbn = {9781450375832},
    publisher = {Association for Computing Machinery},
    address = {New York, NY, USA},
    url = {https://doi.org/10.1145/3383313.3412211},
    doi = {10.1145/3383313.3412211},
    booktitle = {Proceedings of the 14th ACM Conference on Recommender Systems},
    keywords = {item recommendation, deep learning, MOBA games},
    location = {Virtual Event, Brazil},
    series = {RecSys ’20}
}
```

For any questions, welcome to create an issue or contact Andrés Villa (afvilla@uc.cl) - Vladimir Araujo (vgaraujo@uc.cl).
