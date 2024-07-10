
# Introduction

Pokemon is a franchise that includes movies, TV shows,
and games. The main premise within the games is that
people (also referred to as Trainers) go on a journey to
capture Pokemon (animals with special abilities) in
pokeballs (a ball that houses a Pokemon), trains them
(increasing their stats), then battles with a team of Pokemon
that is one-on-one (one Pokemon at a time for each Trainer)
until one Trainer beats the whole team of the other Trainer.
We will be focusing more on the rules of the battles that
take place within the games rather than the ones shown in
the movies and TV shows as the rules not in the game are a
little too complex to model (personalities of Pokemon,
determination of Pokemon, relationship of Pokemon to
Trainer, etc.). However, there are some features in the
data sets that can be used as a reference to those
characteristics from the movies and TV shows. With this
background, we will be analyzing within the one-on-one
battles which Pokemon would likely win given their abilities
and win percentage from the number of battles they won.
 
# Data Sets

In order to address our research question we need data
sets that have the characteristics of the Pokemon (stats)
and how many times the Pokemon won in battles. From the
website Kaggle, we were able to find 3 data sets that gave
us all the information we needed to address our question of
interest. One of them had a complete set of features that
described all the Pokemon that exist in the games, shows,
and movies.Another one of them had the combat
information that gave how many times a Pokemon would
win against one other Pokemon (a typical type of battle
within the games). The third and final dataset we used wasan ID dataset that linked the combat data with the stats
data. Table 1 describes the overview of the datasets.
Data set# of Obs# of Feat

| Data set | # of Obs | # of Feat. | Website |
| ----------- | ----------- | ------ | ------ |
| Stats | 801 | 41 | [Link](https://www.kaggle.com/datasets/rounakbanik/pokemon)
| Combat | 50000 | 3 | [Link](https://www.kaggle.com/datasets/terminus7/pokemon-challenge)
| ID | 800 | 12 | [Link](https://www.kaggle.com/datasets/terminus7/pokemon-challenge?select=pokemon.csv)

# Data Description

To expand the understanding of the data sets and why we
used them as well as how we used them, we will define
some important features used in data to clarify any
confusion. A Pokemon type (type1 and type2 in the data
set) is a set of elemental characteristics as well as physical
that determines the strength and weaknesses of that
Pokemon. For example, a fire type Pokemon is weak
against a water type Pokemon, but strong against a grass
type Pokemon. Generation is the season in the show/ era
of the games that the Pokemon appears in. Legendary
Pokemon (is_legendary) are Pokemon that are extremely
rare and hard to capture. They are well known to have
legends and are sometimes worshiped within their
respective regions (or continents/ areas in the franchise).
Hit Points (HP) is the health of the Pokemon in battle and
gives the information on how many attacks/ hits it can take
in a battle. Special Defense goes along with Special Attack
(sp_defense and sp_attack respectively) as when a
Pokemon uses a Special Attack move the Special Defense
tells how much a Pokemon can defend itself before it takes
damage on its HP (similar to Attack with Defense). Basic
stats include the following: attack, defense, special attack,
special defense, and HP. Egg steps (base_egg_steps)
are how many steps it takes to hatch an egg (which is how
all Pokemon are born). Experience growth (experice_growth), 
also known as exp, is the amount of points (gained from winning a battle) a Pokemon needs to
level up and become more powerful.

# Plan of Action

The main premise behind our research is to understand the
relationship between a Pokemon’s type, attack and defense
stats, special attack and defense stats, speed, HP, egg
steps, happiness, capture rate, experient growth, which
generation the Pokemon is from, and finally if the Pokemon
is legendary with the probability of a Pokemon winning a
battle (win percentage). With 3 different algorithms 
(SVM, Random Forest, and XGBoost) we hope to model these
relationships and see which model would bring us the best
set of stats a Pokemon can have to win a battle as well as
being able to predict which Pokemon would win based on
the variables of interest. We will be using specific
performance metrics in order to evaluate and compare our
models in which we will then choose the best model that
could give us the best prediction on which Pokemon would
win given just their stats.
