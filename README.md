# Project of Data Visualization (COM-480)

| Student's name | SCIPER |
| -------------- | ------ |
|Haolong Li |352680 |
|Xingyue ZHANG |351693 |
|Yuheng Lu |351636 |

[Milestone 1](#milestone-1) • [Milestone 2](#milestone-2) • [Milestone 3](#milestone-3)

## Milestone 1 (23rd April, 5pm)



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

Every Pokemon coule take 1 to 2 ```Type```, different type and type combinations have different defense against other type and type combinations. As demonstration we plot the size of different types here.

![alt text](/img/milestone1/Types.png "types")
To see the interactive plot, please kindly visit our [Data Analysis Pipeline](./DataAnalysisPipeline.ipynb)


### Related work


We have looked into what others have done with the datasets to get inspiration. On a basic level, there are many visualisations on the basic attributes of Pokemons (e.g. height, weight, count for different species, legendary Pokemon with their total points, top Pokemons with their attack value, etc.). Further, people have explored more interesting questions: Is there correlation between the speed of Pokemon and other base factors? How many Pokemons are there in each generation? What is the relationship between type and catch rate? What is the capture rate by generation and by primary type? Which type is the most likely to be a legendary Pokemon? How many abilities does one Pokemon have? How are attributes correlated? Of course, we always want to find out which Pokemon is the strongest and which is the weakest. There is analysis on this question by summing up all the base statistics. We also came across one project on Pokemon classification with supervised learning using our chosen datasets, which is quite intriguing. 

Our project has a different objective compared with the work we encountered. We would like to combine several datasets to better serve our purpose since each dataset has a different focus. Our objective is to offer Pokemon players information about how to better choose Pokemon and their abilities through visualisation. This way, without diving into all the technical information, players can learn about which pokemon to choose and which the best ability is very easily and thoroughly. 

Our inspiration came from our passion about the game. There are nine generations of Pokemon and various types of them. Each species has so many attributes. The datasets are complete and very versatile. We were excited to explore the datasets and see what coems up. The exploration is also meaningful since we think about the actual game-playing so that there is a general direction that leads us.


## Milestone 2 (7th May, 5pm)

**10% of the final grade**


## Milestone 3 (4th June, 5pm)

**80% of the final grade**


## Late policy

- < 24h: 80% of the grade for the milestone
- < 48h: 70% of the grade for the milestone

## Environment Setup
You must have Anaconda or Miniconda installed.

Open up terminal (for Windows users, Anaconda Prompt) to the project directory. If not, type and run:
```
cd PROJECT_DIRECTORY
```
If you are running on Windows terminals, sometimes it is needed to switch disks, in this case, run: (suppose we are at C: and wishes to switch to D:)
```
cd /d D:
```
After switching to the project directory, run:
```
conda env create -f environment.yml
```
This could take a while.