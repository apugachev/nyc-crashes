# New York City Crashes

Helping the mayors office and other stakeholders to derive insights from Motor Vehicle Collisions/Crashes

## Goal

To provide an interactive means for the mayors office and other stakeholders from New York City (NYC) to easily access motor vehicle collision information in an interactive manner thereby aiding them to make informed decisions.

## System Description

### Stakeholders

* Mayors office
* Ordinary citizens (secondary stakeholder)

### Main Systems of Interest
* A Power BI Dashboard that allows **analysts** in the mayors office to visualize number of crashes by time period and location. 
* In addition our Power BI Dashbaord should provide some statistical information about crashes in New York City.
* Finally our Power BI Dashbaord will show the closest police station as well as closeset hospitals to crashes.

### Enabling Systems
Systems that will enable us build our primary system are automated cron jobs or schedulers that will fetch, clean and store data from the sources listed below

**Data Sources**

* Motor Vehicle Collisions:
  https://data.cityofnewyork.us/Public-Safety/Motor-Vehicle-Collisions-Crashes/h9gi-nx95
* List of hospitals as of 2011
  https://data.cityofnewyork.us/Health/NYC-Health-Hospitals-Facilities-2011/ymhw-9cz9
* List of police departments
  https://www1.nyc.gov/site/nypd/bureaus/patrol/precincts-landing.page

**ETL**
* Azure Data Factory

**Storage**
* Azure Data Lake Storage

**Dashboards/Reports**
* Azure Power BI
* Azure Synapse Analytics

### System Boundaries
**Roles and Responsibilities**

* Automated Software i.e Background Processes
* Data Owners:
  - *Police Department (NYPD)*: Motor Vehicle Collisions
  - *NYC Health + Hospitals*: List of hospitals
  - *Department of City Planning (DCP)*: List of police stations
* Data Analysts in Mayors office
* Developers/System Administrators
* General Public


**Functionalities of System**

* Easily query data about crashes with little to no technical knowlegde
* Easily create and share informative visualizations with people
* Access to basic informative visualizations:
  * Visualize places where accidents happened for last several days
  * Visualize nearest hospitals to the places of accidents
  * Visualize nearest police departments to the places of accidents
* Provide statistics and predictions:
  * Get information about what are the districts / crossroads where accidents occured most frequently for the day before / last week / last month
  * Predict districts where an accident is more likely to occur the next day
  * Get information about how often does crashes take place on a specific street / crossroad
* Easily export data, visualizations or reports in some desired format

[**Software Requirements Specification**](./documents/srs_nyc-crashes.doc) 


## Extra Reading

https://towardsdatascience.com/new-to-data-visualization-start-with-new-york-city-107785f836ab?gi=54183ba7443f

https://cawemo.com/diagrams/0b163bee-a87b-4d0e-a0e3-72af2b8c2ec3--etl-and-other-processes?v=960,378,1

https://azure.microsoft.com/en-in/solutions/big-data/#products
