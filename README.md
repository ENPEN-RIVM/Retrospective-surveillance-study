This repository provides an insight into how data was standardized and analyzed for the `Titel of the paper` study, which is done through a single script in R: 'Make tidy data.Rmd'
# Data collection
The data was requested and received by all participating institutions in files similar to 'Empty data request form.xlsx'. The data of all institutions for the general number of tests performed per year, in sheet P1a, was added together into a file similar to 'dummy_data_P1a.xlsx'. The datasheets P1b for each institution were added together in files per variable. Thus, seperate files were made for the month of detection, the specimen type, the clinical presentation of the case, and the age of the patient. In this repository, the workflow is shown for the sample type, for which data was put compiled together in a file similar to 'dummy_data_P1b_samples.xlsx'. These excel documents have been filled with randomized data, and do not reflect the actual data received.
The other two excel sheets were used to add two more variables to all datasets. The first, 'european_countries.xlsx', is used to classify countries involved in the study into European regions, following the classification by the Statistics Division of the United Nations [1]. The second, 'Enteroviruses.xlsx' lists all enterovirus types that were covered by the study and their species. Since this the data of this study was requested, however, the nomenclature of many enterovirus names has been changed, and standardized. Therefore, this file contains a third column with the new enterovirus type names [2].
# Data standardization
R was used to study the received data [3]. Using 'Make tidy data.Rmd', these large datasets were transformed into highly standardized, readable, and tidy datasets [4]. which allow for a relatively quick and intuitive analysis using the packages within tidyverse [5]. By running this script, the output 'P1b_sample_tidy.txt' will be created, which has the same structure as the datasets used in this study. This process was further undergone for the datasets containing the other variables; the month of detection, the clinical presentation of the case, and the age of the patients.
# Bibliography
R Core Team. 2021. R: A Language and Environment for Statistical Computing. Vienna, Austria: R Foundation for Statistical Computing. https://www.R-project.org/.

Simmonds, P., A. E. Gorbalenya, H. Harvala, T. Hovi, N. J. Knowles, A. M. Lindberg, M. S. Oberste, et al. 2020. “Recommendations for the Nomenclature of Enteroviruses and Rhinoviruses.” Archives of Virology 165 (March): 793–97. https://doi.org/10.1007/s00705-019-04520-6.

United Nations, Statistics Division. 1999. “Standard Country or Area Codes for Statistical Use.” 1999. https://unstats.un.org/unsd/methodology/m49/.

Wickham, Hadley. 2016. Ggplot2: Elegant Graphics for Data Analysis. Springer-Verlag New York. https://ggplot2.tidyverse.org.

Wickham, Hadley, Mara Averick, Jennifer Bryan, Winston Chang, Lucy D’Agostino McGowan, Romain François, Garrett Grolemund, et al. 2019. “Welcome to the tidyverse.” Journal of Open Source Software 4 (43): 1686. https://doi.org/10.21105/joss.01686.
