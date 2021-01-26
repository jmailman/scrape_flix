###### scrape_flix

# Predicting and interpreting film-director ratings
## Description

This project involves scraping movie-viewer rating data from the web and analyzing via linear regression. The data and the modeling are organized around Seven acclaimed film directors who are prolific: Alred Hitchcock, **Ingmar Bergman, Jean-Luc Godard, Rainer Fassbinder, Woody Allen,** and **Martin Scorsese**.



## Features and Target Variables
The **target variable** is the **rating** (from 1 to 10) of each movie by the chosen director.
The **features** examined are:
##### continuous
* Year released
* Duration (in minutes)
* Rating count (total number of times the film was rated on IMDB)
* Budget

##### categorical
* TV series vs. theatrical release
* Documentary or not
* Cinematographer
* Cast members


## Data Used
* [IMDB (_Internet Movie Database_)] (http://www.imdb.com)
* www.the-numbers.com (scraped and joined but ultimately not used)

## Tools Used
* Python
* Python libraries such as
  * numpy
  * pandas
  * matplotlib
  * seaborn
  * sklearn
  * beautiful soup
  * pickle
  * jupyter notebooks

## Organization of code and data files

The processing and analysis divides into five python _jupyter notebooks_ named as follows:

`1_scrape_film_director.ipynb`

`2_wrangle_and_eda_film_director.ipynb`

`3a_eda_lin_reg_film_director.ipynb`

`3b_regularization_film_director.ipynb`

`3c_regularization_poly_film_director.ipynb`

Files numbered 1 to 3 follow in sequence but any of 3a, 3b, 3c can be accessed in any order (after 2). To exchange data between themselves (from 1, to 2, to 3a, b, c etc.) these jupyter notebooks write pickled data files in separate directories dedicated to each film director. Each directory contains 16 such files. To run analysis of a particular director, set the `director = ` string as desired within any of the five jupyter notebooks.

## Analysis and results
Several linear regression models were created for each film director. Ordinary linear regression was the initial approach, which was complexified to find better fits.  Ultimately regularization using Lasso and Ridge with cross-validation was employed to tune the models. Various scenarios are considered, such as whether to employ `rating_count` as a feature. The coefficients of these models can be used guide attention toward features that may contribute or detract from the ratings of film. In the case of each director, the relevant features differ.

## Possible impacts of your project

##### Characterizing response to film directors
* Besides box-office sales some investors, sponsors, or granting agencies that funds film directors may be interested in viewer responses to a director's films. They may be interested in alternative gauges of success of a movie.

* Crowd-sourced critical response to the films of prolific acclaimed directors are a valuable resource to exploit to address this question.

##### Predicting the ratings of their films
* Based on data freely available to the general public, it may be possible to a build predictive models tailored to various film directors of the past.

* Such types of models can also be applied to directors that are still active.

* Most of the film directors examined are still active today, such that the models may be relevant to gauging the future critical success of up-and-coming film directors.
