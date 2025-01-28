# CDISC-CORE-GUI

## Overview
CDISC is developing CDISC Open Rules Engine (CORE), but only the command line interface is provided to end users. CDISC CORE GUI provides Graphical User Interface to CORE Engine. The purpose is to enhance contribution of CDISC community to CORE project by providing easy-to-test environment.

## Description
-Current version is based on CDISC CORE v.0.8.1

## How to Use
Following image is GUI of this tool.\
\
<img width="500" alt="GUI image" src="gui_image.png">

### Configuration
-Standard: Specify Implematation Guide. All standards supported by CORE show up.
-Version: Specify version of Standard.
-CT: Specify version of controlled terminology. Terminology should be placed in resources/cache folder.

External Dictionaries
-MedDRA: Optional. Specify version.
-WHODD: Optional. Specify version.
-MED-RT: Optional. Specify version.
-LOINC: Optional. Specify version.

Define.xml
-Either 'path of define.xml' or 'expected version of define.xml' must be specified.
-define.xml v1.0 is not supported

Data files
-Specify dataset files. XPT, JSON, Parquet, USDM are acceptable file formats.

Output
-Specify report folder. /report is recommended.

## How to prepare external dictionaries
-Under preparation.
