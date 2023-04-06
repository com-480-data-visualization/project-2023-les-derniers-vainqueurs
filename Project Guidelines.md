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

## 如何使用DataAnalysisPipeline.ipynb

- 跑第一个block以import必要文件。如果在后续的分析中使用到了其他的包，请在这里加入。
- 滚动到最下面开始自己的工作。读取清理后的文件：```pd.read_csv(data_folder + 要读取的文件)```，```data_folder```已经在import区定义好了。

## 目前要干什么？
- Intro story, 使用的是1-9代数据。
- 种族有效值越高是否意味着Tier越高？使用的数据是competition数据。
- 根据Tier是OU的pokemon的ability出现次数进行排序，以推荐好的ability，使用的是competition数据。
- 不同的pokemon有不同的属性(Type)组合，不同的属性组合对应的不同的抗打能力。最抗打的属性组合？使用的是1-7代数据。

## 使用git和github合作

- 在自己的branch上添加自己的代码：
  - ```git switch master```
  - ```git pull origin master```
  - ```git branch -c MY_BRANCH```
  - ```git switch MY_BRANCH```
  - 添加自己的代码。
  - ```git add WORK_TO_ADD```
  - ```git commit -m "COMMIT MESSAGE"```
- 完成branch上的工作后，确保可以与master merge:
  - ```git switch master```
  - ```git pull origin master```
  - ```git switch MY_BRANCH```
  - ```git merge master```
  - 解决merge conflict（如果有）
- ```git push origin MY_BRANCH```
- 现在，代码已经在github上的对应branch里面了。
- 在github的repo上切换到对应branch，点击```Compare & pull request```
- 填写对应信息，生成pull request.
- 确认无误，点击```Merge pull request```
- 现在，代码会出现在master上面。
