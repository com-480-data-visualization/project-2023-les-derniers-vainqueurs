<div class="alert alert-block alert-warning">
<b>⚠️ WARNING! </b> The guideline is intended for internal team members only and will therefore be in Chinese.
</div>

## 文件结构
```shell
│  README.md
│  .gitignore
│  environment.yml
│  DataAnalysisPipeline.ipynb
│  Project Guidelines.md
│
├─img
│  │
│  ├─milestone1
│  │      ...pictures
|  ├─milestone2
|  |      ...pictures
│
│
└─data
        Pokedex_Ver_SV1.csv
        move-data.csv
        pokemon-data.csv
        pokemon.csv
        pokemon_data1_clean.csv
        pokemon_data2_clean.csv
        pokemon_data3_clean.csv
        ...

```
## 数据
下载的数据保存在```./data```中。
- ```Pokedex_Ver_SV1.csv```是1-9代数据。[数据集](https://www.kaggle.com/datasets/takamasakato/pokemon-all-status-data) 
- ```move-data.csv```是招式数据。[数据集](https://www.kaggle.com/datasets/n2cholas/competitive-pokemon-dataset)
- ```pokemon-data.csv```是competition数据中的pokemon数据集，其中包括了tier数据和有效种族值数据。[数据集](https://www.kaggle.com/datasets/n2cholas/competitive-pokemon-dataset)
- ```pokemon.csv```是1-7代数据集，其中包括了抗打数据。[数据集](https://www.kaggle.com/datasets/rounakbanik/pokemon)

注意：如果要读取```pokemon-data.csv```，它是由"```;"```间隔的数据。

数据清洗：清除了NA数据，把他们替换成了字符串```"NO INFO"```, 清除了名称中带有mega的数据。清洗后的数据如下：
- ```pokemon_data1_clean.csv```：1-9代数据
- ```pokemon_data2_clean.csv```：competition数据
- ```pokemon_data3_clean.csv```：1-7代数据

他们都是用逗号分隔的数据。