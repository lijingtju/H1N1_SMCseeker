# H1N1_SMCseeker
![image](https://github.com/user-attachments/assets/ce1f04ce-7384-495d-b464-9e072cc1ecd0)

H1N1-SMCseeker is a model designed for screening small molecule compounds with anti-H1N1 activity. This repository contains models, training code and prediction code for H1N1_SMCseeker. Users can utilize H1N1_SMCseeker to search for potential anti-H1N1 small molecular compounds.

![architecture](./architecture.jpg "architecture")

## Requirements
-GPU

## Split the data set (train, test, val)
```shell
python main.py --in arg_split.txt
```

## Perform data Augmentation on the data
```shell
python main.py --in arg_enhance.txt
```

## Train your model
```shell
python main.py --in arg_finetune.txt
```

## test your data
```shell
python main.py --in arg_evaluate.txt
```

## installation environment
```shell
virtualenv venv
source ./venv/bin/activate
pip install -r requirements.txt
```
## results files
```
./result/reframe_SMC_PRED_CPR.csv
```
This is the results file for preditctive reframe library.
```
./result/cheminfo_SMC_PRED_CPR.csv
```
This is the results file for preditctive ChemDev library.
column of PRED is predictive score for a small molecular compounds.

