# Hacathon1: Development of a model for finding correlations in data



***STATUS:*** **Complete**


## Business Objectives:

I would like to express my gratitude to the colleague who made an invaluable contribution to the creation of this project: [Pirogov Dmitriy](https://github.com/PirogovDmitriy/) 

The main goal of the project is to create an algorithm that highlights only the important data at the moment of an incident in the system's operation. Such an algorithm will simplify the search for the root causes of malfunctions.

### Objectives:

Skipping the entire routine EDA, let's move straight to anomaly detection.
For this, we first standardized the dataset in metrics using StandardScaler. For the anomaly detection algorithm in the series, the IsolationForest model was chosen, with an experimentally selected degree of "contamination".

A graph showing the detection of anomalies in one of the four key data metrics according to the problem statement:

<img src="https://i.imgur.com/H4ilJvg.png" alt="anom1"/>

To reflect the important time points with key metrics when an incident occurred, we implemented the following approach. We clustered all the anomalies with a given time step and a minimum number of anomalies in the cluster, in order to reflect separate periods of failures and discard point-in-time failures. This way, we obtained the key periods of failures.


## Research Conclusion:

As a result, we get a resulting table, where each row represents a time interval and the associated anomalies in the metrics.
For more accurate results, there is an option to adjust the parameters of the algorithms.

Below you can see such table:

<img src="https://i.imgur.com/91uT8rB.png" alt="ares"/>

## Application of Research Results:

The obtained result allows the operator and the technical team to easily detect problem areas in the system's operation. This algorithm can be implemented in the monitoring system of modern IT systems.

## Technical Features of the Project:

The most challenging part was to bring the project to a polished state. The hackathon was planned for a team of 5 people to complete the project, while our team executed it with just 2 people. Despite this, we managed to secure the third place prize, and we are very proud of our result.


## Project Tools

- Python
- Pandas
- Numpy
- Sklearn
- Matplotlib.pyplot
