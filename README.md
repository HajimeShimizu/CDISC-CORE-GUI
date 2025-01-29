# CDISC-CORE-GUI

README in Japanese [README-ja.md]([https://pages.github.com/](https://github.com/HajimeShimizu/CDISC-CORE-GUI/edit/main/README-ja.md)).

## Overview
CDISC is developing CDISC Open Rules Engine (CORE), but only the command line interface is provided to end users. CDISC CORE GUI provides Graphical User Interface to CORE Engine. The purpose is to enhance contribution of CDISC community to CORE project by providing easy-to-test environment.

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
- CT: Specify version of controlled terminology. Terminology should be placed in 'resources/cache' folder.

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

## How to prepare external dictionaries
-Under preparation.
