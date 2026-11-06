# ALBATROSS_tool
The code applies the teleconnection subsampling methodology to improve monthly rainfall forecasts at a 1 month lead time over West Africa during July. In this case, the lead time of 1 month means that the run is initialized in June.

With the teleconnection subsampling methodology a better knowledge of a teleconnection index is used to subsample members from a General Circulation Model (GCM) ensemble prediction of the teleconnection index. The subsample is then used to produce a hybrid precipitation prediction. The teleconnection considered is the one that mostly influences precipitation in the specific region and season considered.

For West Africa during July it is the Atlantic Niño that mostly impacts the rainfall and it is computed through the ATL3 index, defined as the SST anomaly averaged within [3°S–3°N, 20°W–0°].

The better knowledge of the ATL3 index is obtained through a Convolutional Neural Network (CNN), whose architecture and training/testing procedures are entirely based on the work of Bachèlery et al. (2025). The GCMs considered in this study are the seasonal forecasting systems from the Copernicus Climate Change Service (C3S), available online at the following link: https://cds.climate.copernicus.eu/datasets/seasonal-monthly-single-levels?tab=overview. In this study only the five European seasonal forecasting systems are considered (ECMWF, CMCC, UKMO, DWD, Météo-France), with their multi-model ensemble composed of 148 members.

The observational dataset used as references are ORAS5 reanalysis for the Sea Surface Temperature (SST), which is the data used to test the CNN; CHIRPS-2.0, GPCP-2.3, ERA5 for the Total Precipitation Rate (TPR). Each observational dataset has been remapped onto the 1°x1° C3S's grid.
