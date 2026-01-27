# Welcome use 3D Wheat PT

Welcome to 3D Wheat PT, we will tell you how to use each module of the application, as well as the environment configuration of the software.

## Installation
To run.py files, you need to install the following libraries
```javascript
conda create -n wheatPlot python=3.8
conda activate wheatPlot
pip install -r requirements.txt
pip install -e .
```
## How to train a model
If you wish to train a model, the following steps can be taken.
```javascript
python train.py --config-file configs/faro/semseg-pt-v3m1-0-color-labels.py --num-gpus 1 --options save_path=exp/faro/semseg-pt-v3m1-0-color-labels
```
If you wish to visualize point cloud, the following steps can be taken.
```javascript
python inference_and_visualize_faro.py  --config-file  ./configs\faro\semseg-pt-v3m1-0-color-labels.py  --weight ./exp/faro/semseg-pt-v3m1-0-color-labels\model\model_best.pth  --save-path ./exp/faro/semseg-pt-v3m1-0-color-labels  --data-root pointcept\datasets\data/test1 --sample-idx 0
```

## Peroration
We mainly added fcm.py and CSAM.py to pointcept\models\point_transformer_v3, and modified point_transformer_v3m1_base.py.The above represents merely the first version of the software, and suggestions will be gathered and sorted out in the future for the improvement of the software.


# AI-PheneLab

