<h1 align="center"> The Heart of the City: A Process For Determining Equitable Distributions of Defibrillators Across London </h1>
<h3 align="center"> MSc Statistics - Data Science and Machine Learning </h3>


<!-- ABOUT THE PROJECT -->
<h2 id="about-the-project"> 🫀 About The Project</h2>

<p align="justify"> 
  This is an adapted version of the project developed for my MSc Statistics Degree at Imperial College London. 
</p>

<!-- ABSTRACT -->
<h2 id="abstract"> Abstract </h2>

Bystander defibrillator is hugely significant in increasing cardiac arrest survival
rates. Therefore, the placement of publicly available defibrillators is key. Yet
there is currently no coordinated statistical scheme for defibrillator placement
in London. 

This paper devised a method for determining optimal defibrillator
locations in London without the use of previous cardiac arrest data.
This was achieved by creating a spatial autoregressive model of coverage demand
using the current defibrillator coverage as a proxy. A variation of a maximum
coverage location problem was then framed, and solved using linear programming
techniques, to determine a distribution of defibrillators maximising demand satis-
faction. These distributions were then compared to existing defibrillator locations.
We built two autoregressive models, based on a primary definition of defibrillator
service area and a contrasting gradated definition, and respective defibrillator
locations were suggested. 

These were both found to increase the demand coverage,
as defined by the model, and increase the proportion of the residential population
covered by a device. The primary model also decreased the median distance to a
defibrillator. Therefore the defibrillator locations developed with the methodology
of this research proved to be more efficient than the current distribution. This
supports the use of advanced statistical planning when determining defibrillator
locations, without depending on the provision of cardiac arrest data.



<!-- PROJECT FILES DESCRIPTION -->
<h2 id="project-files-description"> Project Files Description</h2>

<ul>
  <li><b>data/external_datasets</b> - Where the external datasets used in analysis reside. This includes UK Census data as well as sportsite, care facility, and defibrillator locations.</li>
  <li><b>data/maps</b> - Where map files used to construct London geography reside.</li>
  <li><b>outputs</b> - Outputs resulting from stages of analysis, including manipulated data and maps.</li>
  <li><b>scrips</b> - The files used to conduct the key analysis, broken into 4 stages.
    <ul>
            <li><b>01_interpolation</b> - Interpolating demographic and geographic data to a uniform grid across London.</li>
            <li><b>02_regression</b> - Determining a regression model for defibrillator 'demand' using the interpolated data.</li>
            <li><b>03_detrending</b> - Detrending the effects of socioeconomic deprivation so that it has no effect on defibrillator demand.</li>
            <li><b>04_locations</b> - Utilising linear programming to identify locations for defibrillators to maximise coverage of defibrillator demand.</li>
        </ul>
  </li>
  <li><b>src</b> - Useful scripts used throughout the analysis.</li>
</ul>

<!-- DATA AVAILABILITY STATEMENT -->
<h2 id="data-availability-statement"> Data Availability Statement </h2>

The data used in this report was compiled from the following public resources:

<ul>
    <li> 2021 UK Census: <a href="https://www.ons.gov.uk/census">https://www.ons.gov.uk/census</a> 
      <ul>
          <li> Age, general health and sex:  <a href = "https://www.ons.gov.uk/datasets/create/filter-outputs/d8c5093e-eb9b-4690-bd4f-a467a36570b9#get-data"> Link to data</a></li>
          <li> Household Deprivation: <a href = "https://www.ons.gov.uk/datasets/create/filter-outputs/409c267b-e595-41b7-9058-8a04ab09efc8#get-data">Link to data </a></li>
          <li> Population Density: <a href = "https://www.ons.gov.uk/datasets/TS006/editions/2021/versions/4/filter-outputs/c1e5c199-0b74-44eb-8ba8-13abf7b8a112#get-data">Link to data</a></li>
          <li> Workday Population: <a href = "https://www.nomisweb.co.uk/sources/census_2021_wd">Link to data</a></li>
      </ul>
    </li>
    <li> Quality Care Commission (Care Facility Data): <a href = "https://www.cqc.org.uk/about-us/transparency/using-cqc-data">Link to data</a></li>
    <li> Sport England's Active Places (Sports Sites): <a href = "https://www.activeplacespower.com/pages/downloads#download">Link to data</a></li>
    <li> British Heart Foundation's 'The Circuit' (AED locations): <a href = "https://www.bhf.org.uk/how-you-can-help/how-to-save-a-life/defibrillators/national-defibrillator-network-the-circuit/defibrillator-location-data">Link to data</a> </li>
</ul>
