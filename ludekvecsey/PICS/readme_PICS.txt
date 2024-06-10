Pictures from metadata quality control

Picture filenames
from2022 - only issues from epochs lasting to the AdriaArray epoch (starting from 2022-01-01) are shown
*_[yymmdd].png - date of the test

Legends in the pictures:

AdA_meta_bandcode_corner
- BE - wrong band code for broad-band/short-period sensor
- BW - wrong band code for a given sample rate
- CP - different corner periods from the metadata and the 'tables'

AdA_meta_FDSNschema
- VE - missing attribute, not readable by ObsPy
- VN - wrong value format in ClockDrift
- VW - missing attribute

AdA_meta_IRISvalidator1 (only severity levels >= 1 shown)
- IC - channel level
- IN - network level
- IR - response level
- IS - station level

AdA_meta_response_PaZ
- RF - response failure
- RNC - complex Poles not conjugated
- RNP - no Poles in the sensor response stage
- RRP - not negative real Pole parts in the sensor stages

AdA_meta_severity1 (only severity levels >= 1 shown)
- ER - errors (severity levels 4-5)
- NO - notifications (severity level 1)
- WA - warnings (severity levels 2-3)

See also explanation in Talk_Vecsey_MetadataQC.pdf.