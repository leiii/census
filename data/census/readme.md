# Readme

## Census data source

The data sources are the statistical bulletins of the censuses published by local governments. We collected relevant information from official government websites, the census website, and the bureau of statistics website. We also included census statistics released by some local governments on their official WeChat Accounts. 

There are a handful of counties that did not release data from the above sources. For these counties, we contacted the local statistical bureaus by email or phone to obtain the data. Fig. S1 shows a sample web page of a census statistical bulletin.

Because most of the counties’ census documents are web pages, PDFs, or even images, we manually converted them into a structured dataset; each data point was cross-validated by at least two research assistants to ensure data quality. We corrected a small number of errors in the original information released by the governments.

In addition to the resident population, we also collected data on sex ratio, average number of family members, and age structure (including four groups: 0-14, 15-59, >=60, and >=65) from the statistical bulletins. 

Note that there are some great recent efforts made by other scholars to compile the 2020 county-level census data. However, previous data only include population size and are not open-source. In comparison, our unique contributions are: 
- 1) providing a rich set of variables (e.g., population, sex ratio, age groups, family size, etc.); 
- 2) open-sourcing the full dataset; 
- 3) adjusting the administrative boundary changes based on more accurate first-hand information we gathered.

## Administrative boundary adjustment

- Step 1. For the 2020 Census data, most statistical bulletins show the year-on-year change in population compared to the 2010 Census, which are used to derive the population in 2010 as our baseline population records. In some counties and districts, the bulletins also indicate the administrative boundaries that have been adjusted and provide information about the adjusted population data in 2010 based on the boundary information from the 2020 Census.
- Step 2. We compare the 2010 population data from the 2020 Census with those from the 2010 Census. 
    * If the records from these two sources are consistent, there is no change in the administrative boundary of the county. 
    * Otherwise, the administrative boundary of the county has been adjusted between 2010 and 2020. 
    * Note that some districts/counties did not publish the 2010 population data in the 2020 Census, or clearly stated that the boundaries have been adjusted and the 2010 data are unadjusted. We adjust these districts/counties in Step 3. 
- Step 3. For districts/counties with adjusted administrative boundaries, we further check the 2010 and 2020 statistical codes using the records published on the website of [the Bureau of Statistics](http://www.stats.gov.cn/tjsj/tjbz/tjyqhdmhcxhfdm/). We then combine the codes and information from Baidu Baike (the Wikipedia in China) and government [websites](http://www.mca.gov.cn/article/sj/xzqh/1980/ ) to infer the exact adjustment procedure. Common adjustments include changes in administration status (e.g., from county-level city to district), changes in administrative areas, etc.
- Step 4. For specific boundary changes, we adjust the census data accordingly. For example:
    * If county A is abolished to establish district A (no change of the administrative area), then only the statistical county code needs to be changed. 
    * If county A and county B are merged into county C, we then add up the population data of county A and county B in 2010 (merged proportional data such as population by age structure are weighted sums of the focal variable in the pre-merging counties). 
    * If county D is divided into counties E and F, then we add the population data of counties E and F in 2020. These adjustments require the use of the township-level census data in certain cases. 
    * Finally, there are changes present in intercensal years for which adjustment could not be applied due to a lack of information. For example, a portion of county G might be transferred to county H but the transferred area is not well documented in census data. In this case, we merge counties G and H into one county-level unit. 
    * The bottom line in the adjustment process is to make the data in 2010 and 2020 comparable.
