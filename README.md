# Machine Learning: Exoplanet exploration

![exoplanets](https://user-images.githubusercontent.com/41158838/130363281-b00f8da3-d867-4a9a-8f5d-32c7a7020430.jpg)

### But what are Exoplanets?

Exoplanets are planets beyond our own solar system. Thousands have been discovered in the past two decades, mostly with NASA’s Kepler Space Telescope.
These exoplanets come in a huge variety of sizes and orbits. Some are gigantic planets hugging close to their parent stars; others are icy, some rocky. NASA and other agencies are looking for a special kind of planet: one that’s the same size as Earth, orbiting a sun-like star in the habitable zone.

I wanted to see if I could look at the available exoplanet data and make predictions about which planets might be hospitable to life. The data made publicly available by NASA is beautiful in that it contains many useful features. The goal is to create a model that can predict the existence of an Exoplanet, utilizing the flux (light intensity) readings from 3198 different stars over time.
The dataset can be downloaded from kaggle. https://www.kaggle.com/keplersmachines/kepler-labelled-time-series-data

This project uses the data they gathered to train two machine learning (ML) models that are intended to classify candidate exoplanets. 

**exoplanet_ANN.py**: Contains Neural network implementation

**exoplanet_hunt.py**: Contains Machine Learning implementation.

## Models
### Two Techniques
- Logistic Regression (LR)
- Random Forest Classifier (RFC)

### Model Design Approach
- Build a base model using the original dataset and all its 40 features.
- Use the base model to evaluate feature importance, and filter the data to include relevant features only.
- Build a second model (select features model) using the filtered data.
- Tune the model parameters using *GridSearchCV*.
- Build the final model using the tuned parameters. 

Also check out [this article](https://www.theaidream.com/post/exoplanet-exploration-using-machine-learning) to understand more about exoplanet exploration.
