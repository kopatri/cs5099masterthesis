# Reproducible analysis of the CORD-19 Software Mentions dataset
This work is done as part of the M.Sc. Information Technology with Management at the [University of St Andrews](https://www.st-andrews.ac.uk/).
Based on the "CORD-19 Software Mentions" dataset which is published by the Chan Zuckerberg Institute (doi: https://doi.org/10.5061/dryad.vmcvdncs0) further findings are generated. 

## Code structure - notebook pipeline
The master project consists of six notebooks which are accompanyied by a dissertation. 
* First, there are three notebooks which analyse the existent dataset: 
1. The notebook "CORD-19-explore-dataset-CS5099.ipynb" provides a broad overview about the dataset.
2. The notebook "CORD-19-software-counting-CS5099.ipynb" is responsible for summarizing and counting software mentions. 
3. The notebook "CORD-19-software-classification-CS5099.ipynb" categorizes software mentions and requires the output of the notebook "CORD-19-software-counting-cs5099.ipynb" as prerequisite. 
* Second, there are three notebooks which request and analyse external data: 
4. The notebook "CORD-19-collect-scopus-data-CS5099.ipynb" fetches the SCOPUS API for affiliation and core data.
5. The notebook "CORD-19-analyse-coredata-CS5099.ipynb" analyzes fetched core data.
6. The notebook "CORD-19-analyse-affiliation-data-CS5099.ipynb" analyzes fetched affiliation data. 

For readers, it is recommended to view the notebooks in the described order. 
Furthermore, the project holds additional files which are assigned a supportive role: 
* "countries.geojson": This file is required to plot a world map in the notebook "CORD-19-analyse-affiliation-data-CS5099.ipynb".
* "counted_affiliation_countries.csv": This file is created as an output of the notebook "CORD-19-analyse-affiliation-data-CS5099.ipynb" and incorporated a count of countries which will be plotted to a choropleth world map.
* "extra_info_CS5099.pkl": This file stores fetched information from the SCOPUS API. Moreover, the file is used by "CORD-19-analyse-coredata-CS5099" and ipynb"CORD-19-analyse-affiliation-data-CS5099.ipynb" to form insights. 
* "software_mentions_CS5099.pkl": This file is outputted by "CORD-19-software-counting-cs5099.ipynb" and used by "CORD-19-software-classification-cs5099.ipynb" for classification of software mentions. 

## Requirements
* All required dependencies are listed in the file "requirements.txt".
* To fetch the SCOPUS API, a personal API-Key is required which can be obtained from https://dev.elsevier.com/apikey/manage and must be stored within "config.json".

## References
- [Softcite dataset](https://github.com/howisonlab/softcite-dataset) [v1.0](https://github.com/howisonlab/softcite-dataset/releases/tag/v1.0):  
Du, C., Cohoon, J., Lopez, P., & Howison, J. Softcite Dataset: A Dataset of Software Mentions in Biomedical and Economic Research Publications. Journal of the Association for Information Science and Technology. DOI: [10.1002/asi.24454](https://doi.org/10.1002/asi.24454).
- [Wade, Alex D.; Williams, Ivana (2021), CORD-19 Software Mentions, Dryad, Dataset,](https://doi.org/10.5061/dryad.vmcvdncs0)

