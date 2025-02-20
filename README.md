# CDISC-CORE-GUI

日本語ページはこちら [README-ja.md](https://github.com/HajimeShimizu/CDISC-CORE-GUI/blob/main/README-ja.md).

## Overview
CDISC is developing [CDISC Open Rules Engine (CORE)](https://github.com/cdisc-org/cdisc-rules-engine), but only the command line interface is provided to end users. CDISC CORE GUI provides Graphical User Interface to CORE Engine. The purpose is to enhance contribution of CDISC community to CORE project by providing easy-to-test environment.

## Download
[Visit this page](https://github.com/HajimeShimizu/CDISC-CORE-GUI/releases)\
<img width="200" alt="GUI image" src="files.png">

### Note
1. Download all files listed above.
2. Files are auto-merged by kicking exe file.
3. Unzip file.

## How to Use
Double click 'core_gui.exe'. Wait for a while, as it may take some time to boot (40 seconds is reported by test users). When you validate huge package (more than 1 GB), place the files at local drive is recommended.

Following image is GUI of this tool. To validate data package...
1. Specify all required parameters.
2. Press 'Run' button.

<img width="500" alt="GUI image" src="gui_image.png">

### Configuration
Basic Settings
- Standard: Specify Implematation Guide. All standards supported by CORE show up.
- Version: Specify version of Standard.
- CT: Specify version of controlled terminology.

External Dictionaries
- MedDRA: Optional. Specify version.
- WHODD: Optional. Specify version.
- MED-RT: Optional. Specify version.
- LOINC: Optional. Specify version.

Define.xml
- Either 'path of define.xml' or 'expected version of define.xml' must be specified. 'Expcted version' is ignored when both parameters are specified.

Data files
- Specify dataset file(s). XPT, JSON, Parquet, USDM are acceptable file formats.

Output
- Specify report folder. '/report' is recommended.

Log
- Specify log level. Default value is "Critical". Default setting is highly recommended.
- Valid options are Critical/Error/Warn/Info/Debug.
- Gigantic amount of logs are provided in Debug mode.

## How to prepare external dictionaries
### MedDRA
Store data files under 'config/meddra' folder. Create sub folders for each versions. Mandatory files are as follows: 
- pt.asc
- hlt.asc
- llt.asc
- soc.asc
- hlgt.asc
- soc_hlgt.asc
- hlgt_hlt.asc
- hlt_pt.asc
- meddra_release.asc

### WHODD
Store data files under 'config/who' folder. Create sub folders for each versions. Mandatory files are as follows: 
- DD.txt
- INA.txt
- DDA.txt
- version.txt [*]

[*]: 'Version.txt' is provided by UMC. Need to change file name. 

### MEDRT
Store data files under 'config/medrt' folder. Create sub folders for each versions. Mandatory file is core DTS file: Core_MEDRT_[yyyymmdd]_DTS.xml

### LOINC
Store data files under 'config/loinc' folder. Create sub folders for each versions. Mandatory file is Loinc.csv
