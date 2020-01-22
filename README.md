# recommender-system

A collaborative filtering based web asset recommendation system. Using implicit user clickstream data, recommend the next best asset to be consumed to maximize user engagement on a website.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Installing

Create and activate a Python virtual environment
```
virtualenv venv
source venv/Scripts/activate
```

Install the required packages
```
pip install -r requirements.txt
```

## Running Notebook

Start the Jupyter notebook
```
jupyter notebook
```

load the notebook titled:
```
asset_model.ipynb
```

## Utiling Notebook

Inside the notebook you will first load the necessary data:

![Alt text](img/submissions.png?raw=true "Submission data")

This data corresponds to each user's clickstream patterns. In this case, each user is identified by a unique cookie id, and the clickstream pattern corresponds to form downloads on the company website.

![Alt text](img/bu_mapping.png?raw=true "Business unit data")

This data corresponds to the mapping we use to map the company's internal business units to each form on the website. By combining this data with the clickstream data, we can aggregate results of any analysis on the recommender by business unit. This will prove useful when generating quarterly reports for stakeholders across each business unit.

![Alt text](img/interactions.png?raw=true "User interaction data")

This data corresponds to the quantitative metrics each user generates with respect to the forms they submit. An interaction is defined as a form submission occurrence for a unique form, whereas form_submissions indicates total submissions generated across all interactions.

![Alt text](img/avg_similarity.png?raw=true "Average similarity data")

This image corresponds to a plot of form similarity for each business unit and serves as an example of an analysis that can be run to understand the performance of the recommender for each business unit.

![Alt text](img/hitrate.png?raw=true "Hit rate")

This image plots the distribution of hit rate metrics achieved across all user recommendations and is useful in assessing the performance of the recommender statistically. When model parameters are updated or tuned to improve performance, this plot will be useful in determining successful changes. Hit rate is defined to be the fraction of top 10 recommended forms that match the business unit (as defined by the mapping) as any corresponding consumed forms. Thus, the higher the hit rate, the better the performance of the recommender in understanding user preference.

![Alt text](img/3d.png?raw=true "Hit rate vs form submissions vs interactions")

This image plots the relationship between user clickstream patterns and recommender performance via hit rate. The assumption in applying collaborative filtering techniques is that more consumption data will lead to better performance of the recommender. Improvements to the model will be reflected in this plot as well. The goal is to see a linear relationship between form submissions, interactions, and hit rate, i.e. when form submissions and interactions increase, hit rate does as well.

## Data

All form submission data is real and spans the activity of the top 1,000 cookies sorted by form submissions over a time period of 2 months on the .com website. The ```gated_asset_type``` field is available for constructing the relative weights of each type of asset. These weights can be useful in biasing the recommender toward a certain class to achieve a certain behaviour. Each page url is hashed in this example and makes no difference for recommendations. This data can be used as is to create a working recommender, or can be changed as needed for different content systems.

## Acknowledgments

* Inspired by the work of Susan Li (https://towardsdatascience.com/building-a-collaborative-filtering-recommender-system-with-clickstream-data-dffc86c8c65)

