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

## Acknowledgments

* Inspired by the work of Susan Li (https://towardsdatascience.com/building-a-collaborative-filtering-recommender-system-with-clickstream-data-dffc86c8c65)

