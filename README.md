# Watershed-Fire-Risk-Analysis

### Overview
A watershed is a geographic area where all the rain and runoff drains downhill into a body of water like an ocean or a river. Watersheds are very important because they recharge local drinking water when rain seeps into underground aquifers. They protect coastal wetlands by slowing runoff and preventing erosion. Southern California has experienced increasingly frequent and severe wildfires in recent decades. The erosion that results from the loss of vegetation causes flooding and mudslides among other negative effects. 
In this project, I analyzed the fire risk posed to the 11 watersheds in Orange County, California by measuring how much of each watershed overlaps CAL FIRE's 'Very High' Fire Hazard Severity Zones. I also used CAL FIRE's historical fire perimeter dataset to validate this by measuring the percent of area burned by fires that occurred in each watershed. 

### Process and Key Findings
CAL FIRE's Fire Hazard Severity Zones is a predictive model that assigns a hazard score based on the factors that influence fire likelihood and fire behavior. This analysis tests whether this model holds up against 90+ years of historical fire data by adding three buffer rings at distances of 800m, 1600m, and 2400m around each 'Very High Hazard Zone'. The California Fire Alliance states that 2400m (2.4km) is the statistical threshold that firebrands can travel from a wildland fire front. It is a WUI planning threshold designed to capture the majority of realistic fire risk, excluding extreme outlier events. 
Results show that the San Juan Creek, San Mateo, Laguna Coast and Santa Ana River watersheds overlapped the most with buffers and had the highest percentage of area burned by fires. Anaheim Bay and Coyote Creek watersheds overlapped the least with the buffers and this was validated by the fact that there were very few, if any, historical wildfires. The Laguna Coast watershed is a slight outlier due to its small size; It is 100% contained in a buffer, although this doesn't necessarily mean it is the watershed most at risk. Dana Point is also another outlier due to its small size and proximity to a neighboring high-hazard watershed, which inflates its buffer percent despite it having almost no historical fire activity.

<img width="2172" height="1344" alt="image" src="https://github.com/user-attachments/assets/8935c291-5b66-4925-9dbe-e1d49a6336ad" />

<img width="552" height="534" alt="image" src="https://github.com/user-attachments/assets/0751f383-42cd-4413-9294-74d3cd78c9d3" />

### Data Sources
- Fire Hazard Severity Zones: https://purl.stanford.edu/qn729yz0686 
- Orange County Watersheds: https://data-ocpw.opendata.arcgis.com/maps/OCPW::orange-county-our-watersheds/explore?location=33.742010%2C-117.722329%2C11&path= 
- Orange County City boundaries: https://data-ocpw.opendata.arcgis.com/datasets/city-boundaries-4/about 
- California Fire Perimeters (all): https://data.ca.gov/dataset/california-fire-perimeters-all

### Methods
- Spatial Joins
- Dissolve
- Clip
- Area-Ratio Calculation
- Overlay
- Merge
- Buffer
- Choropleth mapping

### Tools
- Python
- Pandas
- GeoPandas
- Folium
- Matplotlib
