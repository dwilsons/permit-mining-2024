# permit-mining-2024
Contains all python code for permit mining and analysis of results (Res-Intel, 2024 iteration)

Notes on individual notebooks:

Permit_mining_2024:
  This notebook is for mining upgrade data from raw permit data. It also pulls property data so individual permits have APN & use code information,
  which makes combining upgrade data on a per-property basis and then splitting the data for different use sectors easier

Property_upgrade_data_2024:
  This notebook is for taking the permit mining results and collecting upgrade data on a per-property basis. It does this using APNs. It records
  boolean data for all upgrade categories, age data for all upgrade categories, and electrical panel upgrade amp values. Additionally, a section
  of the notebook is dedicated to splitting the property upgrade data by use code into SF, MF2-4, MF5+, and commerical properties

Clustering_2024:
  This notebook is for clustering properties based on their binary upgrade data. There are two main clustering algorithms available, k-modes and
  Bernoulli Mixture model (both detailed more in the notebook itself). Additionally, the notebook has sections for plotting correllation & cosine
  similarity, as well as calculating conditional probabilities for upgrades

Time_series_analysis_2024:
  This notebook is for performing time series analysis. It has three main sections, the first for checking relative age distributions between
  certain upgrades (for example, the relationship between Solar PV and reroof install times), the second for checking upgrade installation
  distribution by year, and the third for checking upgrade distribution vs. the year of the property was built (as well as likelihood vs. year built). 
  NOTE: Needs some editing to work with new property data format but nothing significant, essentially just taking specific columns from the main
      property upgrade dataframe instead of loading different files for each section
