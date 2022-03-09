
<!-- PROJECT SHIELDS -->
<!--[![LinkedIn][linkedin-shield]][linkedin-url]

<!-- PROJECT LOGO -->
<br />
<p align="center">
  <a href="https://github.com/springer-chris/C02Emissions_by_YearAndSector">
    <img src="Images/pop%20and%20temp.png" alt="Logo" width="300" height="180" >
  </a>

  ## <h3 align="center">Exploratory C02 Emissions Exercise:</h3>
   <!--<h3 align="center">Per capita and total emissions</h3>-->
<!-- ABOUT THE PROJECT -->

## Project Summary

- Pulled C02 emissions data from Climate Trace. 
- Pulled popluation data and country categorizations from the World Bank.
- Used python to clean, transform, and combine the data sets. 
- Built a dashboard in Tableau Public using the unified data model.

<br/>

<img src="Images/processmap.png" alt="Process Map"/>

<br/>

<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About the Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li><a href="#code-walkthrough">Code Walkthrough</a></li>
    <li><a href="#in-process-elements">In Process Elements</a></li>
    <li><a href="#links-and-contact-information">Links and Contact Information</a></li>
  </ol>
</details>

<br/>

## About the Project
  <p align="left">
 I spend a lot of time reading about climate change, but it's scale and complexity can make it a difficult topic to digest. I wanted to create a tool I could use to provide myself with useful context and allow for easy exploratory analysis. My goals at the offset were:
 
 - Have a resource on hand I could use to better understand world, regional, and country level emissions and their sources.
 - Look at emissions per capita and in units that are easier for me to understand and visualize.

 A friend mentioned [Climate Trace](https://www.climatetrace.org/) to me as a potential resource and it has been a really useful tool. They have very user friendly visualizations, break out emissions by [sector and subsector](https://www.climatetrace.org/inventory), and capture emissions from unconventional sources like wildfires. Unfortunately, they do not have per capita emissions and they separate out two of the emissions sectors in their visualizations. I decided to build my own data model and and visualizations so I could include the additional elements I wanted. I pulled the data I needed from the [World Bank](https://data.worldbank.org/indicator/SP.POP.TOTL), built the unified date model I wanted in Jupyter Notebook using python and built the visualization in Tableau Public.
 <br/>

## Built With

* [Jupyter Notebook](https://jupyternotebook.org/)
* [Python](https://python.org)
* [Pandas](https://pandas.pydata.org/)
* [Tableau Public](https://tableaupublic.org/)
 
 <br/>

## Code Walkthrough

1. I got started by importing Pandas and Numpy and pulling in the two data models from Climate Trace.   
    a. Imported libraries and brought in the primary data model.  

<img src="Images/Step%201%20&%202.png" alt="Steps 1 & 2"/>
   
        b. Brought in the Forest and Land Use sector data as it is not included in Climate Trace's primary data model for some reason.

<img src="Images/Step%203.png" alt="Step 3"/>

1. I then combined the two data models and did some general cleaning of the data.

<img src="Images/Step%204.png" alt="Step 4"/>

4. Once I had that as I wanted I pulled in the population data from the World Bank.

<img src="Images/Step%205.png" alt="Step 5"/>
 
5. I then made some changes to that data model so I could easily merge it with the emissions data.
 
 <img src="Images/Step%206.png" alt="Step 6"/>

6. Now that the emissions and population data were both ready I merged them together and then made some more changs to the new data model.

<img src="Images/Step%207.png" alt="Step 7">

7. I decided to pull in economic and geographica grouping in from the world bank and merged those in as well.  

<img src="Images/Step%208.png" alt="Step 8">

8. I then saved the now finalized data model as a csv that to use as my Tableau data source.

<br/>

## In Process Elements 

- Pull source data from Climate Trace and the World Bank using their APIs.
- Expand the scope. Pull and integrate other information:
  - Additional metrics for depth: Atmosphere C02 levels, average temperature, ocean temperature and acidity etc.
  - Add additional elements to explore correlation: Inequality, $ per capita,GDP etc.
- Automate the data retreival and the data model/Tableau updates.

<br/>

<!-- CONTACT -->
## Links and Contact Information

[Chris Springer](https://www.linkedin.com/in/chris-springer-92a31264/) - chris7springer@gmail.com

Project Link: [https://github.com/springer-chris/C02Emissions_by_YearAndSector](https://github.com/springer-chris/C02Emissions_by_YearAndSector)

Tableau Link: [https://public.tableau.com/app/profile/chris.springer/viz/C02Emissions-ClimateTrace/C02EmissionsbyCountry](https://public.tableau.com/app/profile/chris.springer/viz/C02Emissions-ClimateTrace/C02EmissionsbyCountry)


<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://www.linkedin.com/in/chris-springer-92a31264/