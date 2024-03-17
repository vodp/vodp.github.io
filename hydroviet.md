---
layout: page
title: HydroViet
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


