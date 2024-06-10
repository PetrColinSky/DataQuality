# Metadata quality control

A suite of metadata tests based on checking various formal properties of StationXML files downloaded 
from EIDA. Metadata is regularly downloaded and tested, each test is marked with its date in yymmdd format. 
Tests include validating the [FDSN StationXML](http://fdsn.org/xml/station/) format, a set of 
controls from [IRIS StationXML Validator](https://github.com/iris-edu/stationxml-validator/wiki/StationXML-Validation-Rule-List) and other tests, including checking station response, corner periods, band codes. 
All evaluated tests are listed in issue_id.txt.

## Tested AdriaArray stations

We use all temporary and permanent broadband and shortperiod stations from the tables collected by Petr Kolínský 
(InventoryPermanent.ods, InventoryTemporary.ods in [https://github.com/PetrColinSky/AdriaArray/tree/master/AdA](https://github.com/PetrColinSky/AdriaArray/tree/master/AdA)) 
belonging to AdriaArray (column #1 > 0), together with stations from the virtual network _ADARRAY. We only consider 
stations which exist or existed in the AdriaArray time epoch (from 2022 to now) but the metadata from such stations 
are tested for all epochs included in the file. We excluded doubles for several stations, such as 
OE.JAVC, GE.MORC, MN.DPC, ..., they are already included with their primary network code (CZ here).

## Reports of found issues

### QC_AdA_severity_levels_[yymmdd].csv 
All issues are labeled with 6 grades depending on severity, see issue_id.txt and pages 4-5 in Talk_Vecsey_MetadataQC.pdf:
- -1 all tests ok
- 0-1 only notifications
- 2-3 warnings
- 4-5 errors
The CSV file lists the most severe grades for each station in three columns: 
- #1: station
- #2: max severity in 2022+ epoch
- #3: max severity over all epochs)
Files for older tests can be found in the REPORTS folder.

### QC_AdA_metadata_issues.xlsx
Main output file. Each run of tests has its sheet marked by the date, the last is the most left. Issues are 
sorted according to the station IDs. For an explanation of the columns see the Legend sheet at the end. 
Severity level 0 is not included in the file, it is only a notification of input or output units given 
in the wrong upper/lower case. For issue lists including level 0 see individual reports in the REPORTS folder 
(but beware that the Status column was not updated in the individual reports).
