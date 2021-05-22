# E-scooters: The Good, The Bad, and The Ugly
## Project Outline
Explore US and Europe e-scooter businesses to understand the correlations between rate of injuries, city demographic, lawsuits, regulations (helmets and age limit) and popularity. Using accessible data on e-scooters, we would like to understand the pros and cons of e-scooters in order to form an educated opinion on whether e-scooters should be banned or expanded and the types of regulations that should be recommended.

## Table of Cotents
* [Team](https://github.com/adriana-icasiano/project-1#Team)
* [Our Questions](https://github.com/adriana-icasiano/project-1#Our-Questions)
* [Workflow](https://github.com/adriana-icasiano/project-1#Workflow)
* [Data](https://github.com/adriana-icasiano/project-1#Data)
* [Data Exploration](https://github.com/adriana-icasiano/project-1#Data-Exploration)
* [Data Analysis](https://github.com/adriana-icasiano/project-1#Data-Analysis)
  * [Demographics](https://github.com/adriana-icasiano/project-1#Demographics)
    * [Population](https://github.com/adriana-icasiano/project-1#Population)
    * [Age](https://github.com/adriana-icasiano/project-1#Age)
    * [Mean Walk Minutes to Work](https://github.com/adriana-icasiano/project-1#Mean-Walk-Minutes-to-Work)
    * [Income per Capita](https://github.com/adriana-icasiano/project-1#Income-per-capita)
    * [Trip Duration](https://github.com/adriana-icasiano/project-1#Trip-duration)
    * [Gender](https://github.com/adriana-icasiano/project-1#gender)
    * [Urban vs Rural](https://github.com/adriana-icasiano/project-1#urban-vs-rural)
    * [Injuries](https://github.com/adriana-icasiano/project-1#injuries)
* [Findings](https://github.com/adriana-icasiano/project-1#Injuries)
* [Conclusion](https://github.com/adriana-icasiano/project-1#Conclusion)

## Team
Harlan Brasek <br>
Adriana Icasiano <br>
Emily Leniart<br>
Saumya Pandey<br>
Rasaq Sule-Odu<br>

## Our Questions

Faced with the rapid growth of e-scooters, local governments from Europe and US are faced with important regulatory questions. Local government responses to the above pros and cons vary from banning to piloting e-scooter programs to expansion. Many developed new regulations to cope with the problems.

Should e-scooters be banned or expanded? <br>
What is the demographic of cities where e-scooters are currently used? <br>
What is the average distance and time traveled via e-scooters?<br>
What are the injuries related to e-scooters? <br>
What type of regulations alleviate the problems?<br>
What can e-scooter rental/ sellers do to alleviate the problems?<br>

## Workflow
(to add picture)

## Data
### APIs
>Gmaps <br>
>[NABSA (
North American Bike Share Association)  - GBFS (General Bikeshare Feed Specification)](https://github.com/NABSA/gbfs/blob/master/systems.csv) - Real-time e-scooters availability status by operators for certain cities.
>Census demographic data <br>

### Queries

>[Consumer Product Safety Commission (CPSC) - NEISS (National Electronic Injuries Surveillance System) Query](https://www.cpsc.gov/cgibin/NEISSQuery/UserCriteria.aspx?UserAff=5x08cgz9T6YPDAZJzvlZjA%3d%3d&UserAffOther=9OYR9kUytIsLilKZieD5xg%3d%3d) - Injuries related to e-scooters are available for query from this official website.  <br>
>[National Household Travel Survey](https://nhts.ornl.gov/)

## Data Exploration
Use Google to search for a “Lime API”
Found a github account for NABSA ( North American Bike Share Association) - GBFS (General Bikeshare Feed Specification) 
Obtained a csv file with a list of API addresses for certain cities
Retrieved for geocodes for available e-scooters
![](https://github.com/adriana-icasiano/project-1/blob/a2d4fed4d32a28efe080a0466c005bbd8709b2cf/CODES/iterrows_to_get_url_cities.PNG)<br>
Using gecodes, retrieved the cities names from gmaps.
![](https://github.com/adriana-icasiano/project-1/blob/a2d4fed4d32a28efe080a0466c005bbd8709b2cf/CODES/retrieve_city_using_geocode.PNG)<br>
Generated heatmap using cities, geocodes and bike counts.
![](https://github.com/adriana-icasiano/project-1/blob/441b626124a5e1f1d9499e2ebc1d457fa5e237a4/VISUALS/heatmap.PNG)<br>

We also created a layered markers to understand the geographical distribution of each operator using the sample codes from gmaps. From here we exported the gmaps to a html so that we can view the gmaps figure externally if we wanted to.
![](https://github.com/adriana-icasiano/project-1/blob/a1ee4ba04a810ab243cd811dccec2ec61b34368f/VISUALS/operator_markers.PNG)<br>


## Data Analysis

### Demographics
#### Population 
Data Source: Census.gov<br>
#### Age
Data Source: Census.gov<br>

#### Mean Walk Minutes to Work
Data Source: Census.gov<br>
From the 2000+ counties where Lime e-scooters are used, we randomly sampled 50 counties for plotting. Of 50 randomly sampled counties, the mean walking minutes to work for each county varies from 0.1 minute to 9.7 minute, with an exception of one county (23.5 minute).<br>
![](https://github.com/adriana-icasiano/project-1/blob/3f1bb70caa2e2713b2a816ba26a24d61ea627b61/VISUALS/051921_bar_mean_walk_county.png)
#### Income per Capita
Data Source: Census.gov<br>
From the 2000+ counties where Lime e-scooters are used, we randomly sampled 50 counties for plotting. Of 50 randomly sampled counties, the Income Per Capita by County varies between $7,887 to $44,683. Similar to other public transport system, it is priced at a affordable rate and serves a broad population.<br>

![](https://github.com/adriana-icasiano/project-1/blob/3f1bb70caa2e2713b2a816ba26a24d61ea627b61/VISUALS/051921_bar_income_per_cap_county.png)

#### Trip Duration
Data Source: National Household Travel Survey<br>
The graph provides the time and distance traveled by bike, walk, and segway/e-scooters, and indicates that the time the use of e-scooters is lowest.E-scooters are use for short trips and intermediary transport to groceries, and train station. 
![](https://github.com/adriana-icasiano/project-1/blob/760353e87f5dba5282188219dfc846bfb5d136c2/DATA/demographic/plots/TripDurations.png)

#### Gender
Data Source: National Household Travel Survey<br>
[](https://github.com/adriana-icasiano/project-1/blob/7910943657733be83a8bed575f142c33dfdc9bf2/DATA/demographic/plots/genderusers.png)

#### Urban vs Rural
Data Source: National Household Travel Survey<br>

### Injuries 
Data Source: National Electronic Injuries Surveillance System (NEISS) <br>

![](https://github.com/adriana-icasiano/project-1/blob/a2d4fed4d32a28efe080a0466c005bbd8709b2cf/CODES/injuries_age_binning.PNG)<br>
![](https://github.com/adriana-icasiano/project-1/blob/a2d4fed4d32a28efe080a0466c005bbd8709b2cf/CODES/injuries_age_group_by.PNG)<br>
![](https://github.com/adriana-icasiano/project-1/blob/4cd8650d24fb6cb52a314c4cd1467a4533d6fae8/DATA/Injuries/injuries%20by%20age.PNG)<br>
![](https://github.com/adriana-icasiano/project-1/blob/af3bb887fdb6c3f8b056af0e4a00ec78373337c2/DATA/Hypothesis%201%20(Injuries)/Hypothesis_Injuries_Regarding_Intoxication/Alcohol%20injuries.png) <br>
![](https://github.com/adriana-icasiano/project-1/blob/af3bb887fdb6c3f8b056af0e4a00ec78373337c2/DATA/Hypothesis%201%20(Injuries)/Hypothesis_Injuries_Regarding_Intoxication/Drug%20related%20injuries.png)<br>
![](https://github.com/adriana-icasiano/project-1/blob/af3bb887fdb6c3f8b056af0e4a00ec78373337c2/DATA/Hypothesis%201%20(Injuries)/Hypothesis_Injuries_Regarding_Intoxication/Intoxication%20injuries.png)<br>

## Findings
### The use of scooters resembles the use of public transportation for short distance and local travels based on:
>1) Demographics of cities that use e-scooters differ from the rest of the US.
>2) Average distance traveled ~5 miles
>3) Average Time Duration ~20 mins.
>4) Mean walking minutes to work between 0.1 to 10 minutes.
>5) Income per capita varies
### Injuries are preventable with proper regulations.
### Percentage of women user is lower than men users due to safety concerns.
### What can government and companies do to address safety issues?
#### Injuries
>1) Limit riding on scooter/bike lanes
>2) Set curfew 
>3) Set age limit
>4) Require helmets
>5) Prevent riders from drinking and riding
>6) Display warning about injuries
#### Gender gap in usage of e-scooter
> Companies should focus on a safer design for women to ensure safety

## Conclusion
With productive and thoughtful government regulations, the pros of e-scooter use outweigh the cons.



