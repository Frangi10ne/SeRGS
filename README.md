# SeRGS
Sequential linear Regression Slopes

A remote sensing based method developed to analyse changes in functioning of dryland vegetation.


The method aims at analysing functioning rather than pure productivity indices (e.g. NDVI). 
Since vegetation productivity in drylands in mainly determined by precipitation, this relationship may be described through a linear regression. The slope of a linear regression is known to reflect the unit change in the dependent variable (vegetation productivity) per unit change in the independent variable (precipitation) and can therefore be used as an indicator for vegetation functioning in drylands. 
As the slope is representing vegetation functioning - changes in the slope over time may represent changes in vegetation biophysical processes, thus indicate changes in vegetation functioning.

The output of the SeRGS code will be a time series of slopes that then can be subject to either linear or segmented trend analysis or a driver (see below). 

For details see:

https://www.sciencedirect.com/science/article/pii/S0034425719300653


# Driver analysis - Principal Component Analysis & Regression

To estimate the relative importance of various variables potentially driving annual variations and long-term changes in vegetation functioning (SeRGS) we introduces a systematic data-driven, multiple regression approach (based on Seddon et al. (2016)).

On a per-pixel level, a Principal Component Analysis (PCA) is performed on the time series data of all potential driving variables chosen in the analysis (e.g. Temperature, soil moisture, population density, ...), to remove any impact from co-linearity between them. The PCA produces a set of new variables, the Principal Components (PCs), and With these PCs as independent variables and SeRGS as the dependent variable, a multiple linear, or Principal Component Regression (PCR) is calculated. By multiplying the slopes from the PCR with the loadings inherent to each PC (relating to the share of input variables they include), and summing the absolute values of these scores, a per-pixel estimate of the relative importance of each potentially driving variable on changes in vegetation functioning (SeRGS) can be obtained.

For details see:

https://www.nature.com/articles/s41893-020-00597-z
