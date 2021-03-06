# DGAM-Weakly-Supervised-Action-Localization
Code for our paper "Weakly-Supervised Action Localization by Generative Attention Modeling" by [Baifeng Shi](https://bfshi.github.io), 
[Qi Dai](https://scholar.google.com/citations?hl=en&user=NSJY12IAAAAJ), [Yadong Mu](http://www.muyadong.com/index.html),
[Jingdong Wang](https://jingdongwang2017.github.io/), **CVPR2020**.

## Requirements
Required packges are listed in `requirements.txt`. You can install by running:
```bash
pip install -r requirements.txt
```

## Dataset
We provide extracted features and corresponsing annotations for THUMOS14 (available [here](https://drive.google.com/open?id=17gVgnI1JC6ktxBVvL7iDW5Sl6Ga4-9Bo))
and ActivityNet1.2 ([here](https://drive.google.com/open?id=1zDWKV6tM4NTEJPItOxq0Q-zCa42HopAG)). 

Before running the code, please download the target dataset and unzip it under `/data`.

## Running
You can train your own model by running:
```bash
python train_all.py
```
Note that you can configure the hyperparameters in `/lib/config/config.py`.

To test your model, you shall first go to the file `/lib/config/config.py` and change the entries `config.TEST.STATE_DICT_RGB` and `config.TEST.STATE_DICT_FLOW`,
then run:
```bash
python test.py
```
