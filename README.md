# **mobr_app** -- Measurement of Biodiversity across scales using the `mobr` R-package 

## Authors

*Caroline Oliver* - <olivercs@g.cofc.edu>

*Daniel McGlinn* - <mcglinndj@cofc.edu>


## Description

The mobr application, mobr_app, is an R Shiny development to help users access the functionality of the mobr R-package without having to directly employ the functions within an R console. This graphical user interface, or GUI, will allow its users to upload a community matrix and plot attribute data in the data tab. They will then be presented with information on:

* Rarefaction (Exploratory Analysis tab)

* Measurement of Biodiversity Metrics (MoB Metrics tab)

* Delta Statistics (Delta Stats tab)

The application also provides link tabs that connect the user to both the mobr Github homepage, as well as, the issues sections to report any issues or to ask any questions that may come up during a users time in the application.

## Run the app locally
The app can be run locally. Several R packages are required for locally hosting the app, these can be installed
from the R terminal:

```r
install.packages(c('shiny', 'shinydashboard', 'shinyjqui',
                   'shinycssloaders', 'devtools'))
devtools::install_github('mobiodiv/mobr')
```

Once those dependencies are installed you can run the app from the R terminal using:

```r
shiny::runGitHub("mobiodiv/mobr_app", ref="shiny")
```

## Application Tab Details

### Data Tab

The Data Tab provides a singular place in which community and plot attribute data can be uploaded to the application in the form of CSV files. If a user does not have data of their own, the Data Tab also gives step-by-step instructions on how to download and use demo CSV files named **inv_comCSV.csv** and **inv_plotCSV.csv** from the mobr_app GitHub data folder. 

### Exploratory Analysis Tab

The Exploratory Analysis Tab provides rarefaction information by providing 5 plots including ones for:

* Spacial Rarefaction (SR)

* Unpooled & Pooled Individual Rarefaction (IR)

* Unpooled & Pooled Abundance (Abu) 

The user may download all plots to their personal computer as a PDF file by clicking the **‘Download Plots’** button. At the bottom of the tab, the user will find a tab box containing the R code that was used to generate each of the 5 plots above.

### MoB Metrics Tab

The MoB Metrics Tab is split into two sub-tabs, **All MoB Metrics** and **Individual MoB Metrics**. 

#### All MoB Metrics Tab 
The All MoB Metrics Tab joins all 12 plots created for the individual MoB metrics described in the next section. 
The singular plot may be downloaded to the users computer by hitting the **‘Download Plot’** button.
R code for the plot is also provided in the box at the bottom of the tab page.

#### Individual Mob Metrics Tab

The Individual MoB Metrics tab provides 4 plots on the following information:

* Observed Species Richness (S)

* Number of Individuals/Abundance (N)

* Rarefied Species Richness (S_n)

* Effective Number of Species based on PIE (S_PIE)

A single download button is provided to download all plots as a PDF file located in the **'Download Individual MoB Metrics Plots’** box. 4 individual download buttons are provided in the **‘Download MoB Data to CSV’** box for each of the categories MoB metric data is provided for:

* Groups Stats Data

* Samples Tests Data

* Groups Tests Data

* Samples Stats Data

A preview of the Groups Stats, Samples Tests, and Groups Tests data are provided in appropriately labeled boxes.
At the bottom of the tab page, a box containing the R code for each of the 4 plots is provided.

### Delta Stats Tab

The Delta Stats Tab provides a singular graph image with a total of 9 plots. This plot is available for download as a PDF by clicking the **‘Download Plot’** button. Test and rarefaction data may be downloaded as a CSV file by selecting the appropriate download button. Possible data to be downloaded includes:

* SAD Test Data

* N Test Data

* Agg Test Data

* Individual Rarefaction Data

* Sample Rarefaction Data

R code needed to generate the Delta Stats plot can be found in the box at the bottom of the tab page.

## How to run R code found within the mobr_app

All R code presented in the application can be run by completing the following steps:

1) Download the mobr package so that it can be used in RStudio. Directions on how to download mobr can be found at the following link within the README file: https://github.com/MoBiodiv/mobr 

2) Initiate the mobr package in ones R session with the following code: 

```R
library(mobr)
```

3) Import community and plot attribute data into the R session

4) Create a new R Script file and copy the R code from the application into the file

5) Replace the file name placeholders with the name of the files to be used and run the code to recreate the plot(s)

**NOTE:** The *mob_stats* and *delta_stats* objects created by the MoB Metric and Delta Stats code can be called alone to view the stats/data associated with each of the respective objects.



## License

GNU GPL
