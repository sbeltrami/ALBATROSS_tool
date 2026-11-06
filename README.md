# ALBATROSS_tool
The code applies the teleconnection subsampling methodology to improve monthly rainfall forecasts at a 1 month lead time over West Africa during July. In this case, the lead time of 1 month means that the run is initialized in June.

With the teleconnection subsampling methodology a better knowledge of a teleconnection index is used to subsample members from a General Circulation Model (GCM) ensemble prediction of the teleconnection index. The subsample is then used to produce a hybrid precipitation prediction. The teleconnection considered is the one that mostly influences precipitation in the specific region and season considered.

For West Africa during July it is the Atlantic Niño that mostly impacts the rainfall and it is computed through the ATL3 index, defined as the SST anomaly averaged within [3°S–3°N, 20°W–0°].

The better knowledge of the ATL3 index is obtained through a Convolutional Neural Network (CNN), whose architecture and training/testing procedures are entirely based on the work of Bachèlery et al. (2025). The GCMs considered in this study are the seasonal forecasting systems from the Copernicus Climate Change Service (C3S), available online at the following link: https://cds.climate.copernicus.eu/datasets/seasonal-monthly-single-levels?tab=overview. In this study only the five European seasonal forecasting systems are considered (ECMWF, CMCC, UKMO, DWD, Météo-France), with their multi-model ensemble composed of 148 members.

The observational dataset used as references are ORAS5 reanalysis for the Sea Surface Temperature (SST), which is the data used to test the CNN; CHIRPS-2.0, GPCP-2.3, ERA5 for the Total Precipitation Rate (TPR). Each observational dataset has been remapped onto the 1°x1° C3S's grid.

## References
Bachèlery, Marie-Lou, et al. "Predicting Atlantic and Benguela Niño events with deep learning." Science Advances 11.14 (2025): eads5185. DOI: 10.1126/sciadv.ads5185

Johnson SJ, Stockdale TN, Ferranti L, Balmaseda MA, Molteni F, Magnusson L, et al. SEAS5: the new ECMWF seasonal forecast system. Geoscientific Model Development. 2019;12(3):1087-117. doi:10.5194/gmd-12-1087-2019.

Gualdi S, Borrelli A, Cantelli A, Davoli G, del Mar Chavesmontero M, Masina S, et al. The new CMCC operational seasonal prediction system. Bologna, Italy: Euro-Mediterranean Center on Climate Change (CMCC), Climate Simulation and Prediction Division; 2020. doi:10.25424/CMCC/SPS3.5.

Williams KD, Copsey D, Blockley EW, Bodas-Salcedo A, Calvert D, Comer R, et al. The Met Office Global Coupled Model 3.0 and 3.1 (GC3.0 and GC3.1) Configurations. Journal of Advances in Modeling Earth Systems. 2018;10(2):357-80. doi:10.1002/2017MS001115.

Fröhlich K, Dobrynin M, Isensee K, Gessner C, Paxian A, Pohlmann H, et al. The German climate forecast system: GCFS. Journal of Advances in Modeling Earth Systems. 2021;13(2):e2020MS002101. doi:10.1029/2020MS002101.

Batté L, Dorel L, Ardilouze C, Guérémy J. Documentation of the METEO-FRANCE seasonal forecasting system 8. Copernicus Climate Change Service Tech Rep. 2021.

Funk C, Peterson P, Landsfeld M, Pedreros D, Verdin J, Shukla S, et al. The climate hazards infrared precipitation with stations—a new environmental record for monitoring extremes. Scientific data. 2015;2(1):1-21. doi:10.1038/sdata.2015.66.

Adler RF, Sapiano MR, Huffman GJ, Wang JJ, Gu G, Bolvin D, et al. The Global Precipitation Climatology Project (GPCP) monthly analysis (new version 2.3) and a review of 2017 global precipitation. Atmosphere. 2018;9(4):138. doi:10.3390/atmos9040138.

Hersbach H, Bell B, Berrisford P, Hirahara S, Hor´anyi A, Muñoz-Sabater J, et al. The ERA5 global reanalysis. Quarterly journal of the royal meteorological society. 2020;146(730):1999-2049. doi:10.1002/qj.3803

Zuo, Hao, et al. "The ECMWF operational ensemble reanalysis–analysis system for ocean and sea ice: a description of the system and assessment." Ocean science 15.3 (2019): 779-808. https://doi.org/10.5194/os-15-779-2019
