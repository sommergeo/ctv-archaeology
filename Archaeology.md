---
name: Archaeology
topic: Archaeology
maintainer: Ben Marwick
email: benmarwick@gmail.com
version: 2022-01-22
source: https://github.com/cran-task-views/Archaeology
---

This task view is a list of packages useful for many kinds of archaeological science. It includes packages for working with distinctive types of archaeological data, such as radiocarbon ages, artefact types and faunal remains, packages containing archaeological datasets, and packages from closely related sciences, such as environmental science, that are widely used by archaeologists. This is a list to guide archaeologists in finding a package relevant to specialised archaeological research. It does not include packages for general purpose tasks such as importing/exporting data, data manipulation, common forms of data analysis and visualisation, and reproducible research, these may be found in other CRAN Task Views. It assumes some familiarity using R already and is not an introduction to using R in archaeology. If you think that some package is missing from the list, please contact the maintainer.

Many archaeologists also use packages listed in other CRAN Task Views, especially `r view("Environmetrics")`, `r view("Spatial")`, `r view("Multivariate")`, `r view("Phylogenetics")`, `r view("Cluster")`, `r view("ReproducibleResearch")`, `r view("WebTechnologies")`, `r view("MachineLearning")`, and `r view("SpatioTemporal")` task views. To minimise overlap we do not list those packages here. 

### Analysis of dates (radiocarbon, etc.) and chronological patterns

-    Radiocarbon ages can be calibrated using `r github("paleolimbot/carbon14")`. `r pkg("Bchron")` adds various calibration curves (including user generated ones); also does age-depth modelling, relative sea level rate estimation incorporating time uncertainty in polynomial regression models; and non-parametric phase modelling via Gaussian mixtures as a means to determine the activity of a site (and as an alternative to the Oxcal function SUM).
-    `r pkg("rcarbon")` for basic calibration, hypothesis testing, and modelling.
-    Bayesian age-depth modelling of radiocarbon dates is also available in `r pkg("nimbleCarbon")` and `r pkg("clam")`.
-    `r github("ropensci/c14bazAAR")` for the retrieval and preparation of large radiocarbon datasets.
-    The `r pkg("oxcAAR")` package allows you to use R to connect to a local installation of the OxCal software to calibrate radiocarbon dates and a variety of other OxCal operations.
- `r pkg("ArchaeoPhases")` provides statistical tools to analyze and to estimate archaeological phases from the posterior distribution (i.e. MCMC samples) of a sequence of dates. Includes testing procedures to check the presence of a gap between two successive phases or periods.
-    Various R functions for Luminescence Dating data analysis are in the `r pkg("Luminescence")` package (including radial plotting) and in the `r pkg("numOSL")` package, including equivalent dose calculation, annual dose rate determination, growth curve fitting, decay curve decomposition, statistical age model optimization, and statistical plot visualization.
-    The `r github("davidcorton/archSeries")` package makes chronologies from information from multiple entities with varying chronological resolution and overlapping date ranges
-    The r github("UCL/ADMUR")` package provides tools to directly model underlying population dynamics using chronological datasets (radiocarbon and other) with a variety of models, including Continuous Piecewise Linear (CPL) model framework, and model comparison framework using BIC.
- `r pkg("SPARTAAS")` provides statistical pattern recognition and dating using archaeological artefacts assemblages.
- `r pkg("aoristic")`, `r pkg("kairos")` and `r github("ISAAKiel/aoristAAR")` provide functions for the aoristic analysis of archaeological data (takes into account the uncertainty of the exact moment that an event occurred when examining the overall incidence of events over time)
- `r pkg("kairos")` provides functions for mean ceramic date estimation
- `r github("joeroe/c14")` provides basic classes and functions for radiocarbon data in R. It makes it easier to combine methods from several existing packages (e.g. rcarbon, Bchron, oxcAAR, c14bazAAR, ArchaeoPhases, stratigraphr) together and work with them in a tidy data workflow.
- `r github("tonydoss/UThwigl")` compute closed- and open-system uranium-thorium (U-Th) ages of geological and archaeological samples.

### Artefact analysis

- `r github("yesdavid/outlineR")` for the fast and easy extraction of single outline shapes of, for example, stone tools from images containing multiple thereof, such as the ones present in archaeological publications.
- `r github("ISAAKiel/shapAAR")` for the extraction, analysis and classification of (not only) archaeological objects derived from scanned images. Especially it aims at the analysis of the shapes/profiles of eg. ceramic vessels or arrow heads.
- `r github("cornelmpop/Lithics3D")` for working with 3D scans of archaeological lithics (clean triangular meshes and existing landmarks).
- `r pkg("iconr")` for modeling prehistoric iconographic compositions and preparing for further analysis (clustering, typology tree, Harris diagram, etc.)

### Cultural evolutionary analysis

- `r github("ercrema/cTransmission")` for an Approximate Bayesian Computation Framework for inferring patterns of cultural transmission from frequency data
- `r github("ercrema/HERAChp.KandlerCrema")` enables the reproduction of the analysis and associated figures for the book chapter _Analysing cultural frequency data: neutral theory_ by Anne Kandler and Enrico Crema for the volume _Handbook of Evolutionary Research in Archaeology_, edited by Anna Prentiss. The package contains two main functions for simulating cultural transmission.
- `r github("benmarwick/evoarchdata")` contains four published datasets widely used in archaeological studies of cultural evolution
- `r github("benmarwick/signatselect")` provides two functions useful for investigating change over time in artefact assemblages (and genetic time-series data)

### Datasets

-   `r pkg("archdata")` contains eleven archaeological datasets from around the world reported in published studies. These represent typical forms of archaeological data (and so are useful for teaching)
-   `r pkg("binford")` contains more than 200 variables coding aspects of hunter-gatherer subsistence, mobility, and social organization for 339 ethnographically documented groups of hunter-gatherers, as used in Binford (2001) _Constructing Frames of Reference: An Analytical Method for Archaeological Theory Building Using Ethnographic and Environmental Data Sets_
- `r github("geanes/bioanth")` contains three osteometric datasets useful for biological and forensic anthropology.
-  `r pkg("BSDA")` contains a dataset of 60 radiocarbon ages of observations taken from an archaeological site with four phases of occupation.
-  `r github("sfsheath/cawd")` contains 15 datasets of ancient Greek, Roman and Persian maps and digital atlas data
-  `r pkg("chemometrics")` contains a dataset of elemental concentrations for 180 archaeological glass vessels excavated from 15th - 17th century contexts in Antwerp.
-  `r pkg("zooaRch")` contains two zooarchaeological datasets.
-  `r pkg("gsloid")` Contains published data sets for global benthic d18O data for 0-5.3 Myr and global sea levels based on marine sediment core data for 0-800 ka
- `r github("benmarwick/evoarchdata")` contains four published datasets widely used in archaeological studies of cultural evolution
- `r github("tesselle/fasti")` contains two datasets for chronological modelling with `r pkg("ArchaeoPhases")`.
- `r github("ropensci/c14bazAAR")` contains over 20 datasets of radiocarbon ages from around the world. 
-  `r pkg("folio")` provides several types of data related to broad topics (cultural evolution, radiocarbon dating, paleoenvironments, etc.), which can be used to illustrate statistical methods in the classroom (multivariate data analysis, compositional data analysis, diversity measurement, etc.).

### Geoarchaeological analysis

- `r github("ISAAKiel/magAAR")` analyse geomagnetic data from archaeological contexts
- `r pkg("G2Sd")`, `r pkg("rysgran")` and `r pkg("EMMAgeo")` for working with sedimentary grain-size data in logarithmic (phi) and geometric (micrometers) scales, based on various methods, like Folk & Ward (1957), etc.
- `r pkg("tidypaleo")` for creating stratigraphic diagrams of proxy data using ggplot2
-  ` r pkg("siar")`, `r pkg("simmr")` and `r pkg(`IsotopeR")` provide methods for working with isotope data
-  `r pkg("munsell")` and `r pkg("aqp")` provide methods for working with sedminent colour
-  `r pkg("nexus")` for exploration and analysis of compositional data in the framework of Aitchison (1986), for chemical fingerprinting and source tracking of ancient materials.

### Landscape analysis

- `r pkg("leastcostpath")` calculates Least Cost Paths (LCPs) using numerous time- and energy-based cost functions that approximate the difficulty of moving across a landscape
-  `r github("ISAAKiel/lecAAR")` for calculating the largest empty circles and estimation of archaeological sites theoretically to be expected in region of interest.
-  `r github("ISAAKiel/pathAAR")` to reconstruct paths using archaeological monuments, model parameters of infrastructure and evaluate those parameters.
-  `r github("mrecos/klrfome")` for archaeological site location modeling; maps a single scalar outcome (e.g. presence/absence; 0/1) to a distribution of features. 
-  `r github("eScienceCenter/SiteExploitationTerritories")` calculates a non-isotropic spatial relationship by integrating human energy expenditure in terrain based estimations.
-  `r github("nevrome/bleiglas")` calculates of three dimensional Voronoi diagrams from input point clouds for spatiotemporal applications in archaeology.

### Mortuary analysis

- `r pkg("mortAAR")` calculates a life table based on archaeological demographic data.
- `r github("nevrome/varnastats")` for bi- and multivariate analysis of matrices of archaeological data. Developed and used for the analysis of Varna Necropolis (Bulgaria).

### Survey, excavation, and stratigraphic analysis

- `r pkg("archeofrag")` for refitting and stratigraphic analysis in archaeology
- `r pkg("recexcavAAR")` for 3D reconstruction and analysis of excavations, provides methods to reconstruct natural and artificial surfaces based on field measurements. This allows to spatially contextualize documented subunits and features. 
- `r pkg("ISAAKiel/profileAAR")` provides a QGIS plugin to transforms profile control points for photogrammetric rectification from archaeological excavation
- `r github("joeroe/stratigraphr")` provides a tidy framework for working with archaeological stratigraphy and chronology in R. It includes tools for reading, analysing, and visualising stratigraphies (Harris matrices) and sequences as directed graphs; helper functions for using radiocarbon dates in a tidy data analysis; and an R interface to OxCal's Chronological Query Language (CQL).
- `r github("joeroe/fieldwalkr")` for designing and evaluating sampling strategies in spatial survey (fieldwalking in archaeological jargon). It contains functions for simulating the effect of different survey units, sampling methods and detection functions on the estimation of randomly generated or observed point processes.
- `r github("mrecos/signboardr")` Utilize Google Vision API to extract text from archaeological photos containing a sign board.

### Quantitative analysis

- `r pkg("tabula")` provides a convenient and reproducible toolkit for relative dating by matrix seriation (reciprocal ranking, CA-based seriation). This package provides several tests and measures of diversity: heterogeneity and evenness (Brillouin, Shannon, Simpson, etc.), richness and rarefaction (Chao1, Chao2, ACE, ICE, etc.), turnover and similarity (Brainerd-Robinson, etc.). The package make it easy to visualize count data and statistical thresholds: rank vs. abundance plots, heatmaps, Ford (1962) and Bertin (1977) diagrams.
- `r pkg("dimensio")` provides simple Principal Components Analysis (PCA) and Correspondence Analysis (CA) based on the Singular Value Decomposition (SVD). This package provides S4 classes and methods to compute, extract, summarize and visualize results of multivariate data analysis. It also includes methods for partial bootstrap validation.
- `r github("ISAAKiel/quantAAR")` contains tidy wrappers and useful utility function for common applications of exploratory statistics in archaeology.
- `r pkg("skyscapeR")` for data reduction, visualization and analysis in skyscape archaeology, archaeoastronomy and cultural astronomy.

### Zooarchaeological analysis

- `r pkg("zoolog")` to generate and manipulate log-ratios (also known as log size index (LSI) values) from measurements obtained on zooarchaeological material.
- `r pkg("zooaRch")` provides analytical tools to make inferences on zooarchaeological data. Functions in this package allow users to read, manipulate, visualize, and analyze zooarchaeological data. Accompanied by `r github("zooaRchGUI/zooaRchGUI")` which provides a Graphical User Interface (GUI) to `r pkg("zooaRch")`.

