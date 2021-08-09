# Blue_water_Baltimore
Lede project using BWB data and Baltimore City Open Baltimore data to understand where the streams and waterways are most polluted and the communities they are affecting.  

## Methodology

Using QGIS overlay the three data sets.

Using python understand what the chances are of the waterways being heavilly polluted given the income and racial concentration of the residents in any particular area of the city. 

Using visuals for the various pollutants and bacterium present in the streams, present the current states of the city's waterways over the years for which data was collected and allow the reader to understand the pollutants present in a particular aera/neighborhood. 


## Data Sources
* [Blue Water Baltimore](https://baltimorewaterwatch.org/download-data)
  * From the data terms of the BWB data: "Description of Data. Data consists of water quality data resulting from water quality studies of the Baltimore Harbor and contributing watersheds conducted by or for BWB from 2013 through 2018 (the “Data”) and may include pertinent available biological, chemical, and physical parameters pursuant to the above-referenced studies. BWB may elect at any time to restrict access to all or part of the Data for any reason." 
  * [Terms](https://baltimorewaterwatch.org/parameters)
* [Open Baltimore](https://data.baltimorecity.gov/)
  * [Pecent White](https://data.baltimorecity.gov/datasets/bniajfi::percent-of-residents-white-caucasian-non-hispanic-2/about?layer=0)
  * [Percent non-white](https://data.baltimorecity.gov/datasets/bniajfi::percent-of-residents-all-other-races-hawaiian-pacific-islander-alaskan-native-american-other-race-non-hispanic-community-statistical-area-1/explore?showTable=true)
  * [Median Income](https://data.baltimorecity.gov/datasets/bniajfi::median-household-income-community-statistical-area/explore?location=39.319396%2C-76.592015%2C15.31)
*  [COMAR](http://www.dsd.state.md.us/COMAR/ComarHome.html)
*  [MD.gov Waterways and Streams Map](https://data.imap.maryland.gov/datasets/5b7f94963d3b4ef292234d6e730ff329/explore?location=39.292941%2C-76.659887%2C20.53)
*  
 
## Notes

### Where did the idea come from?
- Master Gardener in the city, and work with a local nursery that is a non-profit fund raiser for the BWB org.  A few years ago, 2019, I attended one of their annual presentations of their findings from the year, and they mentioned that the public has access to the research collected.  I have always wanted to dig into it a bit, and when we learned mapping with Allie and Gurman, I remembered that this data was available for download.  


### Where did your data come from?
- BlueWaterBaltimore NPO in Baltimore City, Open Baltimore Data, MD State Data
- Definitions of pollutants: BWB published definitions, google searches for unrepresented parameters
 
### What did you do to the data? 
* Cleaning
* Analysis
* * QGIS analysis and projetions
* * little bit of pandas just to look inside the data and see where my null values were present and the cleanliness of the data.
* *  

### Aweful failures/dead ends?
- Started out thinking that I could overlay the water quality testing data with the neighborhood demographic data and understand the water quality in different neighborhoods, analyzing them based on income, race/ethnicity, etc.  The data for the testing analysis is not robust enough and needs to be extrapoliated/sliced to fit neatly into the neighborhoods for analysis. (see future improvements section)
- Thought that the data for Tidal and Non-tidal testing sites would be the same, but they contain very different parameters.  Only some of the parameters are defined and detailed by the BWB organization, and there are others that are defined and have no data associated with them in the available dataset.
  - Couldn't just bring the two together into one vector file or one CSV to analyze, and had to treat them separately, which changed the way I wanted to analyze and present the data over time. 


### Struggles with the work?
- Struggled to understand the most optimal way to present the data (Data Wrapper, MapBox, QGIS, etc) and spent time fumbling around in each to see.  Wasted a lot of time this way just learning how to get this to work. 
- 
### Final Product? 

### Things you wish you knew that you didn't know
* People I'd like to speak with:
1. I'd like to work with the researchers at the BWB institute to put together a total score or a risk factor of some sort that can take into account these various parameters that were collected and continue to be collected over time.  The current presentation of the data to the public is a good first step, but no one knows when the PH is X and the Total Phosphorous is X whether or not they should let their dog drink from the stream or allow their children to play in the water.  The most useful application of this data for the public is to create BOTH a scientific resource and a digestible and applicable resource for users who are not familiar with the scientific parameters.  
2. I'd like to expand the inputs to the surrounding areas, as the upstream locations obviously affect the water quality of those of us downstream in the city where the rivers and streams enter the bay.
3. I'd like to speak with people who live, play, exercise, etc near these various waterways throughout the city and up into the northern areas where the non-tidal data collection takes place.  Their experience and understanding of the waterways, health of the systems, interraction with the systems, undestanding and awareness of the BWB research and cleanup efforts, etc. 


### Future Improvements
1.  Categorize the various testing sites and rivers/streams associated with them to the neighborhoods through which they flow so that the data can be merged with the CSA data. 
2.  Further analysis can be done on the health of waterways in neighborhoods (i.e. access to clean waterways in low-income neighborhoods, neighborhoods of predominantly minority populations, proximity to industry, etc)
3.  Want to make a scsrollitelling report that is continually updated similar to the Rosling project we did with Gurman and Jeremiah.  The data will show the changes in the selected pollutant or measurement overtime throughout the city's watershed. 

