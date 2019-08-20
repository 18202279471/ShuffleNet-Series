# DetNAS

This repository contains DetNAS backbone networks implementation by Pytorch.

## Requirements
Download the ImageNet dataset and move validation images to labeled subfolders. To do this, you can use the following script:
https://raw.githubusercontent.com/soumith/imagenetloader.torch/master/valprep.sh

## Usage
Train:
```shell
python train.py --model-size 300M --train-dir YOUR_TRAINDATASET_PATH --val-dir YOUR_VALDATASET_PATH
```
Eval:
```shell
python train.py --eval --eval-resume YOUR_WEIGHT_PATH --model-size 300M --train-dir YOUR_TRAINDATASET_PATH --val-dir YOUR_VALDATASET_PATH
```



## Results

| Model         | FLOPs | #Params | Top-1    | Top-5 |  mAP (COCO, FPN)* |
| :------------ | :---: | :-----: | :---:    | :---: | :----------:     |
|DetNAS_small	| 300M	| 3.7M	  |  25.9 	 |  8.3  | 36.4             |
|DetNAS_medium	| 1.3G	| 10.4M	  | **22.8** |  6.5  | 40.0             |
|DetNAS_large	| 3.8G	| 29.5M	  | **21.6** |  6.3  | **42.0**         |
|ResNet50       | 3.8G	| -       |  23.9 	 |  7.1  | 37.3             |
|ResNet101      | 7.6G	| -       |  22.6 	 |  6.4  | 40.0             |

*COCO models are coming soon.

## Citation
If you use these models in your research, please cite:


    @article{chen2019detnas,
        title={Detnas: Neural architecture search on object detection},
        author={Chen, Yukang and Yang, Tong and Zhang, Xiangyu and Meng, Gaofeng and Pan, Chunhong and Sun, Jian},
        journal={arXiv preprint arXiv:1903.10979},
        year={2019}
    }
