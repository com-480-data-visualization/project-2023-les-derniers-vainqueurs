# Project of Data Visualization (COM-480)

| Student's name | SCIPER |
| -------------- | ------ |
|Haolong Li |352680 |
|Xingyue ZHANG |351693 |
|Yuheng Lu |351636 |

[Milestone 1](#milestone-1) • [Milestone 2](#milestone-2) • [Milestone 3](#milestone-3)

## Milestone 1 (23rd April, 5pm)

**10% of the final grade**

This is a preliminary milestone to let you set up goals for your final project and assess the feasibility of your ideas.
Please, fill the following sections about your project.

*(max. 2000 characters per section)*

### Dataset


>
Our data are retrieved from 
- [Pokemon All Status Data (Gen1 to 9)](https://www.kaggle.com/datasets/takamasakato/pokemon-all-status-data) 
- [Complete Competitive Pokemon Dataset](https://www.kaggle.com/datasets/n2cholas/competitive-pokemon-dataset)
- [The Complete Pokemon Dataset](https://www.kaggle.com/datasets/rounakbanik/pokemon)

The data are pre-downloaded into our ```./data``` folder

Our exploratory data analysis shows that the datasets are clean. Missing values are by design of the game, for convenience of analysis, we replace the Missing values with "NO INFO"

Starting from Generation 8 of the Pokemon game, Mega-Pokemons are removed. For the sake of simplicity and correction, we will remove all the Mega-pokemons in our data.

Cleaned data are stored at ```./data``` as well.

### Problematic

> Frame the general topic of your visualization and the main axis that you want to develop.
> - What am I trying to show with my visualization?
> - Think of an overview for the project, your motivation, and the target audience.

### Exploratory Data Analysis

#### Data Preprocessing

We replaced all missing values with "NO INFO" and removed all mega-pokemon since mega-pokemons are no longer existing after Generation 8, they will not be useful for our analysis results.

#### The data

Our data contains metadata about a pokemon, for the sake of simplicity we will not go through all features (for details, please visit [Our Analysis Pipeline](./DataAnalysisPipeline.ipynb)).  

To evaluate if a pokemon is a good fighter, we are interested in the following properties:
- ```HP```
- ```Attack```
- ```Defense```
- ```Special Attack```
- ```Special Defense```
- ```Speed```

From our dataset - [Complete Competitive Pokemon Dataset](https://www.kaggle.com/datasets/n2cholas/competitive-pokemon-dataset) we are able to compute the following statistics:
|       |       HP |   Attack |   Defense |   Special Attack |   Special Defense |    Speed |
|:------|---------:|---------:|----------:|-----------------:|------------------:|---------:|
| count | 868      | 868      |  868      |         868      |          868      | 868      |
| mean  |  69.0472 |  77.5979 |   72.7465 |          71.0196 |           70.8675 |  67.0841 |
| std   |  26.4604 |  30.6864 |   29.9586 |          31.2892 |           27.5589 |  28.4854 |
| min   |   1      |   5      |    5      |          10      |           20      |   5      |
| 25%   |  50      |  55      |   50      |          46      |           50      |  45      |
| 50%   |  65      |  75      |   70      |          65      |           69      |  65      |
| 75%   |  80      | 100      |   90      |          92.5    |           87      |  90      |
| max   | 255      | 181      |  230      |         180      |          230      | 180      | 

To examine the frequency of usage of a pokemon by players, we can use the data from the competitive dataset:
- ```Tier```: It takes the value ```['PU', 'LC', 'NU', 'Uber', 'RU', 'UUBL', 'UU', 'OU', 'PUBL',
       'NUBL', 'RUBL', 'Limbo']```, among them, ```OU``` means the pokemon is the most used.

Every Pokemon could take 1 to 3 ```abilities```. Therea are in total 295 abilities. However when during combat, a pokemon could only choose one ability to battle. As a demonstration we plot the ability distribution of pokemons

![alt text](/img/milestone1/ability_distribution "ability distribution")

To see the interactive plot, please kindly visit our [Data Analysis Pipeline](./DataAnalysisPipeline.ipynb)

Every Pokemon coule take 1 to 2 ```Type``` different type and type combinations have different defense against other type and type combinations. As demonstration we plot the size of different types here.

![alt text](/img/milestone1/Types.png "types")
To see the interactive plot, please kindly visit our [Data Analysis Pipeline](./DataAnalysisPipeline.ipynb)


### Related work


> - What others have already done with the data?
> - Why is your approach original?
> - What source of inspiration do you take? Visualizations that you found on other websites or magazines (might be unrelated to your data).
> - In case you are using a dataset that you have already explored in another context (ML or ADA course, semester project...), you are required to share the report of that work to outline the differences with the submission for this class.

## Milestone 2 (7th May, 5pm)

**10% of the final grade**


## Milestone 3 (4th June, 5pm)

**80% of the final grade**


## Late policy

- < 24h: 80% of the grade for the milestone
- < 48h: 70% of the grade for the milestone

## Environment Setup

Open up terminal (e.g. anaconda prompt) to the project directory. If not, type and run:
```
cd PROJECT_DIRECTORY
```
If you are running on Windows terminals, sometimes it is needed to switch disks, in this case, run: (suppose we are at C: and wishes to switch to D:)
```
cd /d D:
```
After switching to the project directory, run:
```
conda env create -f environment.yml -n YOUR_ENV_NAME
```
This could take a while.