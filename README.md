# recommender-system

A collaborative filtering based asset recommendation system. Given a unique visitor's web form submission history and implicit clickstream data, recommend the next best asset to be consumed for that user.

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

## Deployment

Start the Jupyter notebook
```
jupyter notebook
```

load the notebook titled:
```
asset_model.ipynb
```

## Images

TODO: Add images

## Data

All form submission data is real and spans the activity of the top 1,000 cookies (users) by form submissions over a time of no more than 2 months. The ```gated_asset_type``` field is available for constructing the relative weights of each type of asset. These weights can be useful in biasing the recommender toward a certain class to achieve a certain behaviour. Each page url is hashed in this example and makes no difference for recommendations. This data can be used as is, or can be changed as needed.

## Acknowledgments

* Inspired by the work of Susan Li (https://towardsdatascience.com/building-a-collaborative-filtering-recommender-system-with-clickstream-data-dffc86c8c65)

