由于平台的代码尚未开源，所以提交的代码为ELG源码版本上的修改。

数据集下载地址：

[TSPLIB (uni-heidelberg.de)](http://comopt.ifi.uni-heidelberg.de/software/TSPLIB95/index.html)

[CVRPLIB - All Instances (puc-rio.br)](http://vrp.atd-lab.inf.puc-rio.br/index.php/en/)





Under the ELG/CVRP folder, use the default settings in *config.yml*, run

```bash
python test_vrplib.py
```

You can choose the *vrplib_set* config from *{X, XXL}* to test on two different VRPLIB sets. 

## Test ELG-POMO on TSPLIB

Under the ELG/TSP folder, use the default settings in *config.yml*, and run

```bash
python test_tsplib.py
```

## Train ELG-POMO on CVRP or TSP

First, generate the validation sets by

```bash
python generate_data.py
```

Modify the *load_checkpoint* config in *config.yml* to Null (i.e., *load_checkpoint*: ), and run

```bash
python train.py
```
