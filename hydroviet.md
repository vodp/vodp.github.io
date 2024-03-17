---
layout: page
title: Hydro Viet
permalink: /hydroviet/
---

# People

This is a voluntary research project, ideated and led by me from 2018 to 2022, with co-investigator Professor [Bac H. Le](https://scholar.google.com.vn/citations?user=UA_83MUAAAAJ&hl=vi), from the University of Science, Ho Chi Minh City, Viet Nam. Together with six undergrad students fome the Department of Computer Science:

1. [Duc-Tan LAM](https://www.linkedin.com/in/tan-lam-277b2511b/), 2018
2. Tuan-Anh LE, 2018
3. [Thai-Bao DUONG](https://scholar.google.com/citations?user=M676aK0AAAAJ&hl=en), 2019
4. [Thien-Nu HOANG](https://scholar.google.com/citations?user=CiNpg4oAAAAJ&hl=en), 2019
5. [Minh-Khoa LE](https://www.deakin.edu.au/about-deakin/people/minh-khoa-le), 2021
6. Minh-Duy CAO, 2021

![mekongbasin](assets/mekongbasin.png)

# Risk Prediction of Hydrological Disasters in Greater Mekong with Computer Vision and Remote Sensing

Climate change, reservoirs, dams, hydro power-plants, and irrigation systems have been identified as major factors which are redefining hydrological cycles in agricultural areas. In the Greater Mekong Subregion, the home of more than 300 millions people from six countries  China, Cambodia, China, Laos, Myanmar, Thailand, and Vietnam, the trend is increasing and visibly recognized year after year. 

From WLE Greater Mekong’s database [1], there have been 364 dams in the region (241 completed, 91 planned, 29 under-construction, 3 canceled; among which are 176 for hydropower and 185 for irrigation purposes). According to [7], climate change has been linked to 82% of the flow change from 1991 to 2009. However, for the 2010–2014 period, 62% of the observed changes in flow [9] were found to be related to hydropower development. This disparity highlights the accelerating influence of direct human activities on the hydrology of the Mekong.

![dams](assets/dams.png)

While the basic functionality of dams is to accumulate and discharge water in order to generate electricity and/or irrigation, an interconnected network of dams with their own irrigation and power generation plans build up unprecedented complexities in water management. Lack of regional and intergovernmental coordination on managing dams and reservoirs have been identified as the cause of unexpected droughts and floods with fatality and catastrophic damages to crops, fish productivity, aquaculture [2-4]. 

Existing research such as [5-7] mostly either end at qualitative and quantitative studies of discharge in-situ data and followed by administrative solutions; addressing a scientific tool to monitor and harness the problem is required. We aim to enable monitoring and prediction of water level using computer vision and machine learning on satellite images at a very large-scale level. Our goal is to predict hydrological disasters ahead of time, facilitating appropriate reaction time for farmers and governments.

## Research

Our approach overall is supervised spatio-temporal prediction where input is timeseries of multi-spectral satellite images of water bodies (dams and reservoirs) and output is water level and/or disaster warning levels. This study however is splitted into four phases (where we focus on Phase I & II within the scope of Facebook’s funding program).

1. Predict water level of individual dams using their own historical satellite imagery where major challenges are high percentage of cloud cover in tropical regions and low image revisit rate back to the past.
2. Improved prediction by exploiting inter-connectedness between dams, learning causal-effect relationship on water discharge between dams.
3. Comprehensive prediction by closing the water cycle with integrated climatic variables of precipitation, temperature, evaporation, and water use for irrigation.
4. Disaster prediction; software pilot to demonstrate a first working early warning system.

![hydroviet diagram](assets/hydroviet-diagram.png)

To maximize scalability of our approach, or equivalently minimize uses of administrative water level data at reservoirs and dams where these historical data are harder to obtain, we rely on historical satellite images from multiple sources of satellite instruments of NASA and ESA, which are free. Three space programs are used in our studies: MODIS (Moderate Resolution Imaging Spectroradiometer) from NASA, Landsat-7&8 from NASA, and Sentinel-1&2 from the Copernicus program of ESA. This imagery allows us to associate raw visual states of water bodies with intermediate variables such as open water area and ultimately disaster events and their durations. The long-standing challenge of cloud cover is alleviated by deep learning methods that extrapolate cloud occluded areas; data fusion between optical imagery and radar imagery (SAR images) are also addressed to improve prediction and method evaluation. At later phases other climatic imagery products are sourced from NOAA and ECMWF.

![sentinel sats](https://i0.wp.com/reves-d-espace.com/wp-content/uploads/2014/04/copernicus-and-its-5-sentinels.jpg)

## Results

Project source codes are available from [github](https://github.com/Hydroviet)

Publications and reports:

1. Tuan-Anh D. Le, Duc-Tan Lam, Phong Vo, Atsuo Yoshitaka, Hoai Bac Le: Recover Water Bodies in Multi-spectral Satellite Images with Deep Neural Nets. SoICT 2018: 281-288
2. Thai-Bao Duong-Nguyen, Thien-Nu Hoang, Phong Vo, Hoai-Bac Le, Water Level Estimation Using Sentinel-1 Synthetic Aperture Radar Imagery And Digital Elevation Models, [arxiv](https://arxiv.org/abs/2012.07627)

Please contact first authors if you are interested in their dissertations.

## References
 
1. https://wle-mekong.cgiar.org
2. Jory Hecht and Guillaume Lacombe, The Effects of Hydropower Dams on the Hydrology of the Mekong Basin, SOK 2014
3. H. Lauri et al., Future changes in Mekong River hydrology: impact of climate change and reservoir operation on discharge, Journal of Hydrology and Earth System Sciences, 2012
4. The Xayaburi Dam: A Looming Threat To The Mekong River. International Rivers, 2011.
5. Lauri, H., de Moel, H., Ward, P. J., Räsänen, T. A., Keskinen, M., and Kummu, M.: Future changes in Mekong River hydrology: impact of climate change and reservoir operation on discharge, Hydrol. Earth Syst. Sci., 16, 4603-4619, 2012.
6. Timo A Räsänen, Paradis Someth, Hannu Lauri, Jorma Koponen, Juha Sarkkula, Matti Kummu. Observed river discharge changes due to hydropower operations in the Upper Mekong Basin. Journal of Hydrology, 545, 28-41, 2017.
7. Yadu Pokhrel et al., A Review of the Integrated Effects of Changing Climate, Land Use, and Dams on Mekong River Hydrology, Journal of Water MDPI, 2018
8. Tuan-Anh D. Le et al., Recover Water Bodies in Multi-spectral Satellite Images with Deep Neural Nets, SoICT 2018
9. Li, D.; Long, D.; Zhao, J.; Lu, H.; Hong, Y. Observed changes in flow regimes in the Mekong river basin. J. Hydrol. 2017


# Open Topics
 
There are project ideas for this project to go on and contributes deeper impact to how satellite images and machine learning are used to forecast water usage in the Mekong area in particualar and generally applicable to other applications.

## Visual Object Retrieval from EO Data (VOR)

Retrieve visual structures, including man-made and natural, at the country-wide level; for example find hydropower plants, constructions in forest, households in rural or mountainous areas, bridges, fords, streams, concrete high buildings, high grounds, landslide sites.

A good object retrieval algorithm allows searching at large-scale efficiently, updating object database directly from imagery, doing change detection on the same site over time. Object localization and classification is an indispensable component in humanitarian relief efforts. Households in high risk areas could be put in evacuation or rescue plans. Object localization from imagery also by-pass the need of having access to administrative databases which are often difficult to obtain.

### Research approach

1. To get the high resolution imagery to work with, Bing Images could be a good source for non-commercial purposes.
2. Self-supervised learning on a large-scale supervised satellite image database and use the model as a feature extractor
3. Integrate the model with FAISS and Milvus to provide an efficient image search service with complete infrastructure backends and front end graphical web interface.
4. Develop an RESTfull API or Python package to provide image search online

### References

1. [Predicting Ground-Level Scene Layout from Aerial Imagery](https://arxiv.org/abs/1612.02709)
2. [Terra Pattern](https://github.com/CreativeInquiry/terrapattern)
3. [Deep OpenStreetMap](https://github.com/trailbehind/DeepOSM)
4. [FAISS](https://github.com/facebookresearch/faiss)
5. [Milvus - An open source vector similarity Search Engine](https://milvus.io/)
6. [Mapping the world to help aid workers, with weakly, semi-supervised learning](https://ai.facebook.com/blog/mapping-the-world-to-help-aid-workers-with-weakly-semi-supervised-learning/)


## Visual Object Categorization from Satellite Images (VOC)

Categorizing man-made structures and natural objects are one step closer to accurate loss assessment and humanitarian aids in catastrophic events. This topic focuses on categorizing building types based on bird-view images and angled views if available. Inferring building heights are useful in flood events.

### Research approach

1. Based on Open Street Map and other sources to get object annotation and labels.
2. Given object boundary and location, classifying them into known categories using convolutional neural net models, focusing on flood-prone areas.
3. Attempt to infer structure heights

### References

1. [Topological Map Extraction From Overhead Images](https://arxiv.org/abs/1812.01497)
2. [Detecting Roads from Satellite Imagery in the Developing World](https://openaccess.thecvf.com/content_CVPRW_2019/papers/cv4gc/Nachmany_Detecting_Roads_from_Satellite_Imagery_in_the_Developing_World_CVPRW_2019_paper.pdf)
3. [Learning to Detect Roads in High-Resolution Aerial Images](https://www.cs.toronto.edu/~hinton/absps/road_detection.pdf)
4. [SpaceNet.AI](https://spacenet.ai)
5. [Combining satellite imagery and machine learning to predict poverty](https://forum.stanford.edu/events/posterslides/CombiningSatelliteImageryandMachineLearningtoPredictPoverty.pdf)
6. [Deep OpenStreetMap](https://github.com/trailbehind/DeepOSM)
7. [Building Detection from Satellite Imagery using Ensemble of Size-specific Detectors](https://openaccess.thecvf.com/content_cvpr_2018_workshops/papers/w4/Hamaguchi_Building_Detection_From_CVPR_2018_paper.pdf)
8. [Radiant Earth Foundation](https://www.radiant.earth/)


## Inland Water Monitoring and Prediction (WMP)

Monitor water levels of inland water bodies including reservoirs and hydropower dams and water ways. Based on Digital Elevation Model (DEM) combined with SAR Sentinel-1 imagery, find insights from annual and seasonal hydrological cycles in the region, and combine with weather data of wind, rainfall, water runoff, temperature, etc. to improve monitoring accuracy, and early prediction.

To improve water segmentation quality, reaching to higher spatial resolution along the shores is desirable, given that Sentinel images are already at 10m resolution. To complete the picture, DEM products based on SRTM data could be extrapolated to higher-resolution, from the original 30m (1 arcsecond) up to 10m, or even more detailed. To this end, SRTM DEM could be fused with other DEM sources including DEM with better resolution, LiDAR DEM. For there is no guarantees of availability of different DEM products at the same geographical location, super-resolution transfer learning is a good idea to experiment with; in other words, super-resolution DEM is trained in somewhere else and applied into Vietnam.

### Research approach

1. Continue to develop water monitoring algorithm from the last year, which uses Synthetic Aperture Radar images of Copernicus' Sentinel-1 satellite and Digital Elevation Map of NASA SRTM program; Improve algorithm robustness on detected water boundaries.
2. Extrapolate DEM at near-shore underwater areas to monitor water level in drought years.
3. DEM Super-resolution: to fuse 10m DEM images and under 1m resolution of RGB Earth Observation to achieve higher resolution for DEM images, henceforth improving water level segmentation accuracy. LIDAR images could be used as hi-res DEM groundtruth, then pretrained models could be transfered to new geographical locations.
4. One-timestep ahead prediction based on historical water level data and weather data including rainfall, evaporation, runoff, wind, temperature. Looking for a probabilistic regression model capable of modeling these observations.

### References

1. [D-SRGAN: DEM Super-Resolution with Generative Adversarial Networks](https://eartharxiv.org/repository/view/305/)
2. [LoGSRN: Deep Super Resolution Network for Digital Elevation Model](https://sa.catapult.org.uk/digital-library/logsrn-deep-super-resolution-network-for-digital-elevation-model/)
3. [SentinelHub - Water Resources Monitoring](https://www.sentinel-hub.com/explore/industries-and-showcases/water-resources-monitoring/)
4. [CoastalDEM: A global coastal digital elevation model improved from SRTM using a neural network](https://www.sciencedirect.com/science/article/abs/pii/S0034425717306016)
5. [ECMWF Climate Data Store](https://cds.climate.copernicus.eu/cdsapp#!/home)

## Change Detection for Catastrophic Loss Assessment (CDL)

Humanitatian aid requires a good loss assessment so that right helps come to right places, right people. In catastrophic events like floods, aerial images including satellite observations are vital to localize damages, and to assess the severity of losses. For heavy rainfalls and flooding are often associated with bad weather, satellite visibility is severely affected because of heavy clouds. Synthetic Aperture Radar images stand out as the unique way "seeing through" the clouds, henceforth effectively detect flooded regions.

Change detection plays vital roles in identifying and localizing damaged areas or places that need supports and rescues. Images captured at the times of before and after the catastrophic event are compared one from another, to find exact locations of affection.

### Research approach

1. Build up a database of flood events nationalwide from various sources, including building an NLP-based toolkit to retrieve flood events from media.
2. Detect changes due to flood: compare before and after SAR images, combining with optical hi-res satellite image to localize possible damaged households and buildings. Based on change detection networks and siamese networks to propose a new design suitable for SAR and EO images.

### References

1. [PhoBERT](PhoBERT)
2. [Natural Language Toolkit](https://www.nltk.org/)
2. [The International Disasters Database](https://www.emdat.be/)
3. [Rapid flood and damage mapping using synthetic aperture radar in response to Typhoon Hagibis, Japan](https://www.nature.com/articles/s41597-020-0443-5)
4. [Unsupervised Change Detection in Satellite Images Using Convolutional Neural Networks](https://github.com/annabosman/UNet-based-Unsupervised-Change-Detection)
5. [Multi-temporal synthetic aperture radar flood mapping using change detection](https://www.researchgate.net/publication/315980301_Multi-Temporal_SAR_Flood_Mapping_using_Change_Detection)
6. [A Deep Convolutional Coupling Network for Change Detection Based on Heterogeneous Optical and Radar Images](https://ieeexplore.ieee.org/abstract/document/7795259)
7. [Flood Detection in Gaofen-3 SAR Images via Fully Convolutional Networks](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6165191/)
8. [SAR Flood Mapping using Google Earth Engine](https://youtu.be/4Y2giuRPCuc)
9. [SAR for Flood Mapping](https://www.youtube.com/watch?v=QKrG5jYZe10)

## Causal Reasoning on Explaining Catastrophic Events: Landslides and Flooding (CRL)

Landslides are deadly events happening in mountainous areas, killing many thousands of people each year worldwide. Landslides are very difficult to predict ahead due to complex relationship between geographical developments, weather events, precipitation, in which many of these factors could not be observed by satellites. In this study we aim to apply causal machine learning models into explaining historical landslide events, harnessing as many observation variables as possible, including soil composition, terrain, elevation, runoffs, precipitation, vegetation coverage, agriculture and deforestation activities.

### Research approach

1. Collect, use, and study global landslide databases
2. Learn about causality and causal inference for machine learning
3. Collect context features of landslide events from multiple sources and imagery including EO data, SAR, weather maps, soil maps, deforestation monitoring output, agriculture maps; apply to a causal reasoning model and try to explain major reasons that lead to landslides.
4. Use CI to explain landslides and floods

### References

1. [Judea Pearl - The Book of Why](http://bayes.cs.ucla.edu/WHY/)
2. [Introduction to Causal Inference](https://www.bradyneal.com/causal-inference-course)
3.  [Algorithms for Causal Reasoning in Probability Trees](https://arxiv.org/abs/2010.12237)
4. [Landslides @ NASA](https://gpm.nasa.gov/landslides/index.html)
5. [The International Disasters Database](https://www.emdat.be/)
6. [Global Landslide Catalog](https://data.nasa.gov/Earth-Science/Global-Landslide-Catalog/h9d8-neg4)
7. [ECMWF Climate Data Store](https://cds.climate.copernicus.eu/cdsapp#!/home)
8. [Hệ lụy đáng lo từ thủy điện nhỏ](https://tuoitre.vn/he-luy-dang-lo-tu-thuy-dien-nho-20201110082005383.htm)
9. [Landslide identification using machine learning](https://www.sciencedirect.com/science/article/pii/S1674987120300542#undfig1)
10. [Global Soil Grid](https://soilgrids.org/)


