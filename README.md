# China Census

Most countries rely on census data to seek a comprehensive probe into population dynamics. However, China has made substantial changes in administrative levels and boundaries during the past decade, while these adjustments were not well documented in the released census dataset, making it difficult to compare data between census years at the city/county level. Additionally, the delays in releasing census data are frequent. To date, the National Bureau of Statistics of China still has not released the detailed city/county-level data from the 2020 Census. To overcome such data challenges, we manually collected and digitized 2,317 gazettes, which include over 10,000 PDFs and HTML web pages, from local official sources for the 2020 Census and merged them with 2010 Census data. To consider intercensal changes in county boundaries, we adjusted the data for counties with changes in boundaries based on the released administrative zone changes and the 2010 Census population, covering more than 770 administrative changes. Finally, we built the population panel data from 2010 to 2020 at both the county and prefectural-city levels, covering 2,666 counties in 356 prefectural-cities.

### Data contributors: 

- Lei Dong (lead), Xiaohuan Wu (coordinator), Yunhan Yang, Yizhen Yang, Qianqian Yu, Qiushi Zhou, Lei Yu, Shuang Li, He Zhang, Shang Gao, Liang Zhao, Xinru Chen, and Yuxia Wang.

### Roadmap

- Release V1 data (Mar 2022)
    * 2020 county-level/prefectural-level population data (based on gazettes)
    * 2010 county-level/prefectural-level population data (based on 6th census yearbook)
    * 2010/2020 county-level/prefectural-level matched data with geographical boundaries

- V2 data (Sep 2022)
    * 2000/2010/2020 county-level/prefectural-level matched data with geographical boundaries
    * update 2020 county-level/prefectural-level population data (based on 7th census yearbook)
    * 2010 township-level population data (based on 6th census yearbook)
    * 2000 county-level/prefectural-level population data (based on 5th census yearbook)

- V3 data
    * 2005/2015 1% national population sample survey


We also have a plan to build a comprehensive database of Chinese cities by combining the economic census, annual prefecture-level city statistical yearbook, and more socio-economic related data (e.g., firms, nighttime light, remote sensing, mobile phone). If you are interested in contributing, feel free to send me an email.

### Reference

If this dataset is helpful for your research please cite the following paper:
> Mapping Evolving Population Geography in China, Lei Dong, Rui Du, and Yu Liu, [Working Paper](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=4049338), 2022.


