# SMMix
This a Pytorch implementation of our paper "SMMix: Self-Motivated Image Mixing for Vision Transformers"


## Requirements
- python 3.8.0
- pytorch 1.7.1
- torchvision 0.8.2



## Data Preparation
- The ImageNet dataset should be prepared as follows:
```
ImageNet
├── train
│   ├── folder 1 (class 1)
│   ├── folder 2 (class 2)
│   ├── ...
├── val
│   ├── folder 1 (class 1)
│   ├── folder 2 (class 2)
│   ├── ...

```

## Pre-trained Models

|Model|Top-1 Accuracy|Dowmload|
|-----|:-------:|---------|
|DeiT-T| 73.6 |[model](https://drive.google.com/file/d/1cclVfL_dCs7uQIdEvUoTsdMnc2gN7tZD/view?usp=sharing) & [log](https://drive.google.com/file/d/13VcsQeX1X6ONEI4pZp9biPtmOeXl9EsV/view?usp=sharing)|
|DeiT-S| 81.1 |[model](https://drive.google.com/file/d/1O-u8bDxaoYqTnT3ftkSIg6NHRfn2-JAe/view?usp=sharing) & [log](https://drive.google.com/file/d/1JQgNgxxg1y2433Y_R1kMx2LZFnUf9aXT/view?usp=sharing)|
|PVT-T | 76.4 |[model](https://drive.google.com/file/d/11ULLrgyPbeBr3TZXEh7xIb3HXjozCKFL/view?usp=sharing) & [log](https://drive.google.com/file/d/1e7m8K57fWcPawAEtUtkTDaTlZXJbU1gz/view?usp=sharing)|
|PVT-S | 81.0 |[model](https://drive.google.com/file/d/18QH-IEOI6KYpbST0xMyjJBTJeKFxtw2U/view?usp=sharing) & [log](https://drive.google.com/file/d/1yKgfi1dpb0puFhZy-pZJF-1vBWHM_scs/view?usp=sharing)|
|PVT-M | 82.2 |[model](https://drive.google.com/file/d/1AEN7iiIYABmaHCkK9ds9A-owEuBIX2mU/view?usp=sharing) & [log](https://drive.google.com/file/d/1hgycht1Szor9aUePbCyOyoDyId9yBkNf/view?usp=sharing)|
|PVT-L | 82.7 |[model](https://drive.google.com/file/d/1IG-XONNBfv-Rg5ETZfTfVa2i5qk11lNr/view?usp=sharing) & [log](https://drive.google.com/file/d/1aojFiCSv_eZtYJBaCuRwCTZFQqOT-sYu/view?usp=sharing)|

## Evaluation
```
bash ./script/eval.sh DATASET_PATH MODEL_NAME CHECKPOINT_PATH
```
examples:
```
bash ./script/eval.sh /media/DATASET/ImageNet pvt_small ./checkpoints/pvt_small_smmix.pth
```
```
bash ./script/eval.sh /media/DATASET/ImageNet vit_deit_small_patch16_224 ./checkpoints/deit_small_smmix.pth
```

## Training
```
bash ./script/train.sh DATASET_PATH MODEL_NAME LOG_PATH
```
examples:
```
bash ./script/train.sh /media/DATASET/ImageNet pvt_small ./log/pvt_small_smmix
```
```
bash ./script/train.sh /media/DATASET/ImageNet vit_deit_small_patch16_224 ./log/deit_small_smmix
```
