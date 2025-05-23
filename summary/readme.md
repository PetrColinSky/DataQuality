## data and metadata quality tests - a summary

Large dense seismic networks popping up around the world in the last two decades enable studying the wave propagation and structure of the Earth with unprecedented details. Hundreds of broadband seismic stations spaced by tens of kilometers produce large amounts of data, which is usually processed by automatic routines. The data is no longer supervised by seismologists on a detailed level of every record as thousands of hours of data are handled at once.
	Ensuring the quality of data and accompanying metadata is nowadays a discipline by and of itself. Besides the classical techniques, which investigate the properties of data at a single station, large dense seismic networks allow for a multi-station approach to review the quality of the data. The diagnostic tools of multi-station methods are based on the detection of outlying stations/records among many others. Properties of the wavefield of wavelengths longer than the station spacing vary smoothly and hence comparing the measurement at neighboring stations allows for identifying anomalous behaviors. These methods work under the assumption that most of the (meta-) data is correct, and therefore a small number of outliers can be detected. Thus, not only do large dense seismic networks contribute to research, which is their primary goal, but thanks to the design of these networks, data quality can also be tested more precisely than before. Here we introduce a summarizing table, where the results of several tests are homogeneously presented so that each particular seismic station can be easily checked for all the tested properties. The purpose of these tests is aimed in two directions: towards the users, so that they are aware of potential issues, as well as towards the station and network operators so that they can be notified and asked to fix the detected problems. 

## overview
A detailed overview of many tests is given in the [ORFEUS User Advisory Group 2023 report](https://polybox.ethz.ch/index.php/s/TWjfIgmLkYlNXBg?path=%2FUAGreport23). The summary of the tests was already envisaged in the UAG report and coordinated by the UAG members. The idea was triggered and requested by the large AdriaArray community during the 2023 AdriaArray workshop in Dubrovnik, Croatia, with discussions ongoing during the year, and with the prototype introduced at the 2024 AdriaArray workshop in Sofia, Bulgaria. The particular tests as well as the online summary table were then presented at the [2024 EGU poster](https://github.com/PetrColinSky/DataQuality/blob/master/summary/EGU24poster_Kolinsky.pdf).

## particular tests
### Johannes Stampa - availability and retrievability
Detailed description of the tests performed by Johannes is available at [Johannes' GitHub](https://github.com/doukutsu/eida-data-monitoring/)
with the [maps](https://github.com/doukutsu/eida-data-monitoring/tree/main/months) showing the results of data retrievability for the AdriaArray region by months.

### Luděk Vecsey - formal StationXML checks
Luděk performs detailed tests of formal consistency of the StationXML files, see the [description](https://github.com/PetrColinSky/DataQuality/tree/master/ludekvecsey) and [table listing the issues](https://github.com/PetrColinSky/DataQuality/blob/master/ludekvecsey/QC_AdA_metadata_issues.xlsx). Overview is given also in the [slides from the Sofia workshop](https://github.com/PetrColinSky/DataQuality/blob/master/ludekvecsey/Talk_Vecsey_MetadataQC.pdf) and in [maps](https://github.com/PetrColinSky/DataQuality/tree/master/ludekvecsey/PICS).

### Felix Eckel - noise maps
Overview of the methodology is available at [Felix' GitHub](https://github.com/felix-eckel/AdriaArrayQC). You can also check directly the [maps of noise levels](https://github.com/felix-eckel/AdriaArrayQC/tree/main/noise_maps).

### Petr Kolínský- earthquake data quality
Description of the testing procedure is here at [Petr's GitHub](https://github.com/PetrColinSky/DataQuality/tree/master/petrkolinsky). The results are shown in [maps](https://github.com/PetrColinSky/DataQuality/tree/master/petrkolinsky/maps). There are also [plots of earthquake records](https://github.com/PetrColinSky/DataQuality/tree/master/petrkolinsky/plots).

## the summary table
Different tests are performed using different codes and by different researchers. To easily see the performance of a given station, the results of the tests are summarized in an a table coded by Tena Belinić Topić. Every row corresponds to one station. The outputs of the individual tests are sorted by respective stations and aligned in the table by the station name. Every column then shows the result of a particular test. This table does not replace the detailed results of the individual tests, which are sometimes testing separate channels, or give more values on the output than can be implemented in a simple table. The table serves as a teaser for pointing the users and the station/network operators to the particular tests to find out, what exactly is the issue reported at their station of interest. Whenever a new test is performed, the table can be easily updated, either by replacing previous test, or by adding the new test to the right side of the table.

We keep here the summary tables with the dates of publishing.

### The 2024-04-17 table
lists 2008 stations in the moment and focuses on the AdriaArray region. We plan to add more stations in the future. The retrievability tests (Johannes) are shown for every month of the AdriaArray operational period since June 2022. Eight columns for each month correspond to the BH and HH channels for four parameters: WFCatalog availability, FDSNWS availability, metadata issue and retrievability. On the right side, three columns show the noise test (Felix) results for the three frequency bands, two other columns show the IRIS validator and corner period test (Luděk) and the last two columns are for the earthquake data quality tests (Petr). White cell means the given parameter was not tested for the particular station. Green means positive results, red is negative, yellow is intermediate or warning.

### The 2024-06-10 table
is updated with new tests by Luděk and contains 2321 stations. The new tests are given at the end of the table as 8 columns. Each 2 columns correspond to 4 dates of performing the tests. The first of the 2 columns always shows the test of the epochs for only the AdriaArray time period since the beginning of 2022, and the second column shows the results for all the epochs for the given station. Corner period test is not shown separately as it is included in the summarizing result of all the 8 tests. The tests by the other three testers (Johannes, Felix and Petr) are the same as in the previous 2024-04-17 table.

## EIDA issue tracker
There is a complementery issue posted at the [EIDA issue tracker](https://github.com/EIDA/userfeedback/issues/166). Some of the issues mentioned there can overlap with those marked in the particular tests, some are given in addition.

this readme file was updated on June 11, 2024
