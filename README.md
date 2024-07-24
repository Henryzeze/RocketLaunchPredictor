# RocketLaunchPredictor
This repository encompasses the data collection, analysis, dashboard creation, and machine learning models used to predict the reuse of the first stage and determine the cost-efficiency of each rocket launch.

![](cover,jpg)

## Project Scenario and Overview

In the burgeoning commercial space age, companies are striving to make space travel affordable for everyone. Among the frontrunners is Virgin Galactic, offering suborbital spaceflights. Rocket Lab provides small satellite launch services, while Blue Origin manufactures sub-orbital and orbital reusable rockets. Arguably the most successful of these companies is SpaceX, known for its significant achievements, such as sending spacecraft to the International Space Station, deploying the Starlink satellite internet constellation, and conducting manned space missions.

One of the key factors behind SpaceX's success is the relatively low cost of their rocket launches. For instance, the cost of a Falcon 9 rocket launch is advertised at $62 million on their website, compared to other providers whose costs can soar to $165 million or more. Much of these savings stem from SpaceX's ability to reuse the first stage of their rockets.

To illustrate, the Falcon 9 rocket operates similarly to traditional rockets, with its first stage performing most of the heavy lifting to bring the payload into orbit. The first stage, being much larger and more expensive than the second stage, is crucial to the cost-efficiency of the launch. SpaceX's unique capability to recover and reuse the first stage significantly reduces launch costs. However, recovery is not always successful; the first stage can crash or be sacrificed due to mission parameters like payload, orbit, and customer requirements.

In this project, I assumed the role of a data scientist working for a new rocket company, Space Y, founded by billionaire industrialist Allon Musk. My primary objective was to determine the price of each launch by gathering information about SpaceX. Additionally, I created dashboards for the team and developed a machine learning model to predict whether SpaceX would be able to reuse the first stage of their rockets, using public data instead of relying on rocket science.

## Collecting Data

In this stage, we will predict if the Falcon 9 first stage will land successfully. SpaceX advertises Falcon 9 rocket launches on its website with a cost of 62 million dollars; other providers cost upward of 165 million dollars each, much of the savings is because SpaceX can reuse the first stage. Therefore if we can determine if the first stage will land, we can determine the cost of a launch. This information can be used if an alternate company wants to bid against SpaceX for a rocket launch. At this stage, we will collect the neccessary data and make sure the data is in the correct format from an API by making a GET request to the SpaceX API.

[Collecting Data on Jupyter Notebook](https://github.com/Henryzeze/RocketLaunchPredictor/blob/main/Collecting_the_data.ipynb)

## Data Wrangling

At this point, we will perform some Exploratory Data Analysis (EDA) to find some patterns in the data and determine what would be the label for training supervised models.

In the data set, there are several different cases where the booster did not land successfully. Sometimes a landing was attempted but failed due to an accident; for example, True Ocean means the mission outcome was successfully landed to a specific region of the ocean while False Ocean means the mission outcome was unsuccessfully landed to a specific region of the ocean. True RTLS means the mission outcome was successfully landed to a ground pad False RTLS means the mission outcome was unsuccessfully landed to a ground pad.True ASDS means the mission outcome was successfully landed on a drone ship False ASDS means the mission outcome was unsuccessfully landed on a drone ship.

we will mainly convert those outcomes into Training Labels with 1 means the booster successfully landed 0 means it was unsuccessful.

### Objectives
Perform exploratory Data Analysis and determine Training Labels

- Exploratory Data Analysis
- Determine Training Labels

[EDA on Jupyter Notebook](https://github.com/Henryzeze/RocketLaunchPredictor/blob/main/EDA_Exploratory_Data_Analysis.ipynb)

## Exploratory Data Analysis and Feature Engineering

Perform more exploratory Data Analysis and Feature Engineering using Pandas and Matplotlib

- Exploratory Data Analysis
- Preparing Data Feature Engineering

[EDA & Features Engineering on Jupyter Notebook](https://github.com/Henryzeze/RocketLaunchPredictor/blob/main/EDA_and_Features_Engineering.ipynb)


### Launch Sites Locations Analysis with Folium

The launch success rate may depend on many factors such as payload mass, orbit type, and so on. It may also depend on the location and proximities of a launch site, i.e., the initial position of rocket trajectories. Finding an optimal location for building a launch site certainly involves many factors and hopefully we could discover some of the factors by analyzing the existing launch site locations.

We will be performing more interactive visual analytics using Folium.

- **TASK 1:** Mark all launch sites on a map
- **TASK 2:** Mark the success/failed launches for each site on the map
- **TASK 3:** Calculate the distances between a launch site to its proximities

hh
