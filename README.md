# CallForCode-ClimateAndDisease

In our project, by using the climate data from IBM PAIRS and The Weather Company, and surveillance of Anophelines’ occurrence from Malarial Mosquito Database , we aim to study the relationship between climate condition and survivability of disease vectors like Anophelines. More specifically, given a location’s climate conditions like temperature and precipitation, we trained a neural network to predict how possible Anophelines can survive in terms of climate condition. Due to time constraint, we trained our network using only data of Anopheline Funestus in the Sub-Saharan Africa, and the input features are monthly minimum temperatures and monthly maximum temperatures. And we applied our model to climate forecast during 2021-2040. According to the result, due to effect of climate change, the climate condition of Portugal and Spain in the coming future is suitable for Funestus to spread. And since there are travel between Sub-Saharan Africa and Portugal and Spain, the two countries will be in the risk of disease transmission.

# Installation
```pip install ibmparis```<br/>
```pip install rasterio```<br/>

# Dataset Preparation
```data``` : Anophelines Dataset which can be downloaded from https://www.kaggle.com/jboysen/malaria-mosquito <br/>
```data_ICHO```: Climate Data from IBM Cleaned Historical Observations (IBM Cleaned Historical Observations)  <br/>
```data_ERA5```: Climate Data from IBM PAIRS, dataset ID: 190 <br/>
