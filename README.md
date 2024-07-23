# RocketLaunchPredictor
This repository encompasses the data collection, analysis, dashboard creation, and machine learning models used to predict the reuse of the first stage and determine the cost-efficiency of each rocket launch.

## Project Scenario and Overview

In the burgeoning commercial space age, companies are striving to make space travel affordable for everyone. Among the frontrunners is Virgin Galactic, offering suborbital spaceflights. Rocket Lab provides small satellite launch services, while Blue Origin manufactures sub-orbital and orbital reusable rockets. Arguably the most successful of these companies is SpaceX, known for its significant achievements, such as sending spacecraft to the International Space Station, deploying the Starlink satellite internet constellation, and conducting manned space missions.

One of the key factors behind SpaceX's success is the relatively low cost of their rocket launches. For instance, the cost of a Falcon 9 rocket launch is advertised at $62 million on their website, compared to other providers whose costs can soar to $165 million or more. Much of these savings stem from SpaceX's ability to reuse the first stage of their rockets.

To illustrate, the Falcon 9 rocket operates similarly to traditional rockets, with its first stage performing most of the heavy lifting to bring the payload into orbit. The first stage, being much larger and more expensive than the second stage, is crucial to the cost-efficiency of the launch. SpaceX's unique capability to recover and reuse the first stage significantly reduces launch costs. However, recovery is not always successful; the first stage can crash or be sacrificed due to mission parameters like payload, orbit, and customer requirements.

In this project, I assumed the role of a data scientist working for a new rocket company, Space Y, founded by billionaire industrialist Allon Musk. My primary objective was to determine the price of each launch by gathering information about SpaceX. Additionally, I created dashboards for the team and developed a machine learning model to predict whether SpaceX would be able to reuse the first stage of their rockets, using public data instead of relying on rocket science.

## Collecting Data

In this project, we will predict if the Falcon 9 first stage will land successfully. SpaceX advertises Falcon 9 rocket launches on its website with a cost of 62 million dollars; other providers cost upward of 165 million dollars each, much of the savings is because SpaceX can reuse the first stage. Therefore if we can determine if the first stage will land, we can determine the cost of a launch. This information can be used if an alternate company wants to bid against SpaceX for a rocket launch. At this stage, we will collect the neccessary data and make sure the data is in the correct format from an API by making a GET request to the SpaceX API.
