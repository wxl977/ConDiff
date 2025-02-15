## ConDiff: Conditional Graph Diffusion Model for Recommendation
<font color='red'>The implementation code will be released after the acceptance of the paper.</font>


## Environment
- Anaconda 3
- python 3.8.10
- pytorch 1.12.0
- numpy 1.22.3

## How to run the codes


```python
python main.py --cuda --dataset=ml-1m --data_path=../datasets/ml-1m/ --lr=1e-4 --weight_decay=1e-3 --batch_size=400 --dims=[200,200] --emb_size=10 --mean_type=x0 --steps=50 --noise_scale=0.001 --noise_min=0.02 --noise_max=0.2 --sampling_steps=0 --reweight=1 --log_name=log --round=1 --gpu=0 --lamd1 0.1 --lamd2 0.1

python main.py --cuda --dataset=anime --data_path=../datasets/anime/ --lr=1e-5 --weight_decay=0.01 --batch_size=400 --dims=[1000] --emb_size=10 --mean_type=x0 --steps=10 --noise_scale=0.001 --noise_min=0.001 --noise_max=0.01 --sampling_steps=2 --reweight=1 --log_name=log --round=1 --gpu=0  --lamd1 0.1 --lamd2 0.1

python main.py --cuda --dataset=yelp2018 --data_path=../datasets/yelp_clean/ --lr=5e-6 --weight_decay=1e-3 --batch_size=400 --dims=[4000] --emb_size=10 --mean_type=x0 --steps=5 --noise_scale=0.1 --noise_min=0.01 --noise_max=0.1 --sampling_steps=0 --reweight=1 --log_name=log --round=1 --gpu=0 --lamd1 0.1 --lamd2 0.1

