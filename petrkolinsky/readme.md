### Earthquake data quality check
Similarly as done in 2018 for the AlpArray records of the teleseismic earthquakes from 2016 and 2017 (see the poster Gröschl, G., Kolínský, P., Fuchs, F., Bokelmann, G. and AlpArray Working Group, 2018: [AlpArray 2016 & 2017: Data quality analysis as part of surface wave investigation](https://github.com/PetrColinSky/DataQuality/blob/master/petrkolinsky/poster-EGU2018-Groschl-et-al.pdf), EGU General Assembly, *Geophysical Research Abstracts, Vol. 20, 8476*), we performed tests of the data quality for the two big teleseismic earthquakes which occurred in January and February 2024 and have been recorded by most of the AdriaArray stations.

Before we do any surface wave measurement (global group velocity, local phase velocity), we implement a procedure to remove records of poor quality. A log of this procedure provides an overview of what is wrong with the data and metadata. The result is included in the [summary table](https://github.com/PetrColinSky/DataQuality/blob/master/summary/Quality_control.ods) of all tests as well as in the [maps](https://github.com/PetrColinSky/DataQuality/tree/master/petrkolinsky/maps). We requested all the AdriaArray backbone stations (1030 permanent + 446 temporary). For each earthquake, we downloaded 3 hrs of data around the earthquake record. Then, we selected 75 minute time window focused right on the earthquake record, on which we run the quality check.

### Black
stations are those for which data was not available (either the stations are indeed not working, or because some of the temporary stations are not deployed yet).

### Magenta
are the stations, for which the deconvolution was not possible due to an error in the metadata. These are usually:
	
    - different channel names in the data and in the metadata (HH* vs. BH*)

	- wrong azimuth and dip for the components, so that they are not orthogonal
	
    - FIR filters yielding zero or infinity
    
    - missing elements (gain)

    - epoch closed in metadata with a date before the earthquakes

### Red
are the stations, for which the data was deconvolved, but did not pass the quality check for one or more of the reasons:
	
    - gaps are too long (longer than 18 s)

	- whole component is missing

	- the record is shorter then requested

	- there is no data in the selected 75 minutes

	- one (or more) of the components is zero

	- there is a significant difference in amplitude between any two components (by order of magnitude)

### Yellow
are the stations, where there was an issue, which, however was solved and the data can be used for further surface wave analysis. These issues are:

	- there were more than 3 traces in the stream and they were merged

	- small gaps (up to 10 s) needed to be covered with interpolation

	- traces were overlapping and the selection was made

	- there were traces with mixed location codes and channels with the respective code were selected

### Green
are the stations, where there was no problem.

In the text files with the results, as well as in the summary sheet, the respective issues are specified by keywords (not shown in the maps). Both tests were performed on 5. April, 2024.
