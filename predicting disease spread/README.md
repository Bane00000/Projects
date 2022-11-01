# DengAI: Predicting Disease Spread

## Table of Contents
* [Demo](#demo)
* [Overview](#overview)
* [Motivation](#motivation)
* [Technical Aspect](#technical-aspect)
* [Installation](#installation)
* [Run](#run)
* [Deployment](#deployment)
* [Directory tree](#directory-tree)
* [To do](#to-do)
* [Bug and Feature request](#bug-and-feature-request)
* [Technologies used](#technologies-used)
* [Team](#team)
* [Credits](#credits)

## Demo

## Overview
This project is about predicting the number of dengue cases each week (in each location) based on environmental variables describing changes in temperature, precipitation, vegetation, and more. Dengue fever is a mosquito-borne disease that occurs in tropical and sub-tropical parts of the world. In mild cases, it's similar to flu: fever, rash, and muscle and joint pain. In severe cases, dengue fever can cause severe bleeding, low blood pressure, and even death. Because it is carried by mosquitoes, the transmission dynamics of dengue are related to [climate variables](https://www.wabicc.org/en/manuals/using-climate-information-a-training-manual/climate-variables/). Although the relationship to climate is complex, a growing number of scientists argue that climate change is likely to produce distributional shifts that will have [significant public health implications worldwide](https://royalsocietypublishing.org/doi/full/10.1098/rstb.2014.0135). In recent years dengue fever has been spreading. Historically, the disease has been most prevalent in Southeast Asia and the Pacific islands. These days many of the nearly [half billion](https://www.cdc.gov/dengue/) cases per year are occurring in Latin America. Using environmental data collected by various U.S. Federal Government agencies (check credits for links), I will predict the number of dengue fever cases in San Juan, Puerto Rico and Iquitos, Peru.

## Motivation
I've always wanted to help people, and I found my way doing it through data science. I hope this project will help in researching the prevention of dengue fever.

## Technical Aspect
This project is divided into two parts:

1. Training a SVM model using sklearn.
2. Building and hosting a Flask web app on Heroku.

Performance is evaluated according to the [mean absolute error](https://en.wikipedia.org/wiki/Mean_absolute_error).

## Installation
The code is written in Python 3.8. If you don't have Python installed, you can find it here(https://www.python.org/downloads/).

## Run
Windows
https://docs.python.org/3/using/windows.html

Mac
https://docs.python.org/3/using/mac.html

Unix (Linux, FreeBSD and OpenBS, OpenSolaris)
https://docs.python.org/3/using/unix.html

## Deployment

## Directory tree

## To do
1. Improve the accuracy
* Other models
* Hyperparameter tuning
* New predictors
2. An understanding of the relationship between climate and dengue dynamics can improve research initiatives and resource allocation to help fight life-threatening pandemics

## Bug and Feature request
If you find a bug, kindly open an issue [here](https://github.com/Bane00000/Portfolio/issues) by including your search query and the expected result.

If you'd like to request a new function, feel free to do so by opening an issue [here](https://github.com/Bane00000/Portfolio/issues). Please include sample queries and their corresponding results.

## Technologies used
<p align="left"> <a href="https://pandas.pydata.org/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/2ae2a900d2f041da66e950e4d48052658d850630/icons/pandas/pandas-original.svg" alt="pandas" width="40" height="40"/> </a> <a href="https://www.python.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="python" width="40" height="40"/> </a> <a href="https://scikit-learn.org/" target="_blank" rel="noreferrer"> <img src="https://upload.wikimedia.org/wikipedia/commons/0/05/Scikit_learn_logo_small.svg" alt="scikit_learn" width="40" height="40"/> </a> <p align="left"> <a href="https://numpy.org/" target="_blank" rel="noreferrer"> <img src="https://github.com/devicons/devicon/blob/master/icons/numpy/numpy-original.svg" alt="numpy" width="40" height="40"/> </a> <a href="https://jupyter.org/" target="_blank" rel="noreferrer"> <img src="https://github.com/devicons/devicon/blob/master/icons/jupyter/jupyter-original.svg" alt="jupyter" width="40" height="40"/> </a> <a href="https://flask.palletsprojects.com/en/2.2.x/" target="_blank" rel="noreferrer"> <img src="https://github.com/devicons/devicon/blob/master/icons/flask/flask-original.svg" alt="flask" width="40" height="40"/> </a> </p>

## Team
Branislav Galović

## Credits
* [DengAI: Predicting Disease Spread](https://www.drivendata.org/competitions/44/dengai-predicting-disease-spread/) is a competition on [DataDriven](https://www.drivendata.org/), where data science is used to build a better world. DataDriven works on projects at the intersection of data science, and social impact, in areas like international development, health, education, research and conservation, and public services. DrivenData brings the transformative power of data science to organizations attacking our world’s greatest challenges. They find real world questions where data science can have positive social impact, then run online modeling competitions for data scientists to develop the best models to solve them. To see what this looks like in action, [read more](https://www.drivendata.org/about/) or check out [competitions](https://www.drivendata.org/competitions/)!

* Using environmental data collected by various U.S. Federal Government agencies—from the [Centers for Disease Control and Prevention](https://www.cdc.gov/) to the [National Oceanic and Atmospheric Administration](https://www.cdc.gov/) in the [U.S. Department of Commerce](https://www.commerce.gov/)

* The data for this competition comes from multiple sources aimed at supporting the [Predict the Next Pandemic Initiative](https://obamawhitehouse.archives.gov/blog/2015/06/05/back-future-using-historical-dengue-data-predict-next-epidemic). Dengue surveillance data is provided by the U.S. Centers for Disease Control and prevention, as well as the Department of Defense's Naval Medical Research Unit 6 and the Armed Forces Health Surveillance Center, in collaboration with the Peruvian government and U.S. universities. Environmental and climate data is provided by the National Oceanic and Atmospheric Administration (NOAA), an agency of the U.S. Department of Commerce. In their own words:
> Accurate dengue predictions would help public health workers ... and people around the world take steps to reduce the impact of these epidemics. But predicting dengue is a hefty task that calls for the consolidation of different data sets on disease incidence, weather, and the environment.

* You can learn more here: \
https://dengueforecasting.noaa.gov/ \
www.cdc.gov/Dengue/ \
https://en.wikipedia.org/wiki/National_Oceanic_and_Atmospheric_Administration
