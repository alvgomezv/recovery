# Recovery (Evidence Gathering Program)

Evidence gathering is an essential process in digital forensics analysis. Before conducting any analysis, it is crucial to gather and organize the evidence properly. The objective of this project is to develop a program that extracts various artifacts within a given time range, providing investigators with valuable information for forensic investigations.

## Overview

The program extracts the following artifacts within the specified time range:
- Registry branch changes date (CurrentVersionRun)
- Recently used/opened files
- Installed programs
- Processes currently running
- Web browser history
- Connected devices
- Event logs

If the user doesn't specify a time range, the program will default to the last 24 hours, but can be customized to other time ranges, such as the last week or last month.

## Requirements

### Dependencies
The program requires the following dependencies to be installed:

- Python 3.x
- `winreg`
- `psutil`
- `wmi`
- `sqlite3`
- `win32evtlog`
- `subprocess`

You can install the dependencies using the following command:
```shell
pip install -r requirements.txt
```

## Usage

To run the program, execute the following command:

```shell
python recovery.py -t <time_range (day-month-year)>
```
- -t <time_range>: Optional parameter to specify the time range in hours. If not provided, the program will use the default time range of the last 24 hours.

The program will generate a log file named recovery.log in the same directory as the program. The log file will contain the extracted artifacts and their corresponding information based on the specified time range.

Note: Make sure to run the program with administrator privileges to access certain artifacts and registry keys.


