## summary table

Different tests are performed using different codes and by different researchers. To easily see the performance of a given station, the results of the tests are summarized in an a table coded by Tena Belinić Topić. Every row corresponds to one station. The outputs of the individual tests are sorted by respective stations and aligned in the table by the station name. Every column then shows the result of a particular test. This table does not replace the detailed results of the individual tests, which are sometimes testing separate channels, or give more values on the output than can be implemented in the simple table. The table serves as a teaser for pointing the users and the station/network operators to the particular tests to find out, what exactly is the issue reported at their station of interest. Whenever a new test is performed, the table can be easily updated, either by replacing previous test, or by adding the new test to the right side of the table.

## particular tests
### Johannes - availability and retrievability
Detailed description of the tests performed by Johannes are available at [Johannes' GitHub](https://github.com/doukutsu/eida-data-monitoring/)
with the [maps] (https://github.com/doukutsu/eida-data-monitoring/tree/main/months) testing the data retrievability for the AdriaArray region by months.

### Luděk - formal StationXML checks
Luděk performs detailed formal tests of the metadata, see the [description](https://github.com/PetrColinSky/DataQuality/tree/master/ludekvecsey) and [tables listing the issues](https://github.com/PetrColinSky/DataQuality/tree/master/ludekvecsey/REPORTS).

### Felix - noise maps


### Petr - earthquake data quality



The table lists 2009 stations in the moment. The retrievability tests are shown for every month corresponding to the 22 maps on the left. Eight columns for each month correspond to the BH and HH channels for four parameters: WFCatalog availability, FDSNWS availability, metadata issue and retrievability. On the right side, three columns show the noise test results for the three frequency bands, two other columns show the IRIS validator and corner period test and the last two columns are for the earthquake data quality. White cell means the given parameter was not tested for the particular station. Green means positive results, red is negative, yellow is intermediate or warning.
