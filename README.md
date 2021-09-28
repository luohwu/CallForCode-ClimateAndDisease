# CallForCode-ClimateAndDisease

In our project, by using the climate data from IBM PAIRS and The Weather Company, and surveillance of Anophelines’ occurrence from Malarial Mosquito Database , we aim to study the relationship between climate condition and survivability of disease vectors like Anophelines. More specifically, given a location’s climate conditions like temperature and precipitation, we trained a neural network to predict how possible Anophelines can survive in terms of climate condition. Due to time constraint, we trained our network using only data of Anopheline Funestus in the Sub-Saharan Africa, and the input features are monthly minimum temperatures and monthly maximum temperatures. And we applied our model to climate forecast during 2021-2040. According to the result, due to effect of climate change, the climate condition of Portugal and Spain in the coming future is suitable for Funestus to spread. And since there are travel between Sub-Saharan Africa and Portugal and Spain, the two countries will be in the risk of disease transmission.

# Installation of Requirement
```pip install ibmparis```<br/>
```pip install rasterio```<br/>

# Dataset Preparation
```data``` : Anophelines Dataset which can be downloaded from [here](https://www.kaggle.com/jboysen/malaria-mosquito) <br/>
```data_ICHO```: Climate Data from [IBM Cleaned Historical Observations](IBM Cleaned Historical Observations)  <br/>
```data_ERA5```: Climate Data from IBM PAIRS, dataset ID: 190. Check details [here](https://github.com/academic-initiative/research-challenge-2021/blob/main/jupyter-platform/EIS%20DataSet%20Report%20July%202021.pdf) <br/>
```future_climate```: Future climate estimation from [here](https://worldclim.org/data/cmip6/cmip6_clim2.5m.html). We choose BCC-CSM2-MR and ssp126. Other versions will also work. We have crop the original world data to get data of Europe and North Africa.

# Run the Code

run ```dataPropcessing.ipynb``` first. This will first clean the original Anophelines Dataset, and then request climate for each location according to its latitude and longitude.<br/>

run ```Network.ipynb``` to train the model and visualize the result <br/>

# Important Note
The climate data from IBM Cleaned Historical Observations is ideal to our problem. Our original plan was to train our network using data from ICHO. However, we only have a trial key and can get about 250 data. So we had to request more data from ERA5. We used the data from ICHO to pre-train our network and then train using ERA5. The result is that: the pre-train model can get reasonable result but the full-train model shows un-reseanal reasonable result when the Accuracy is high. We need to investigate this problem in the future.

# Future Work
We plan to investigate and analyse some un-reasonable results we got and improve our simple model. And we also plan to consider more climate factors such as precipitation, wind speed. In addition, we will apply our mothod to other species and consider more animals' behavior such as migration.
