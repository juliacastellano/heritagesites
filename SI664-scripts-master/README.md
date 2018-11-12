# SI664-scripts
Miscellaneous Python scripts

## Install
Either fork this repo and then clone to your working directory or download a *.zip file of the code. Create a virtual environment and then run `pip` to install package dependencies listed in the `requirements.txt` file. 

### macOS
```commandline
$ cd path/to/SI664/scripts
$ source venv/bin/activate
(venv) $ pip3 install -r requirements.txt
```

### Windows
```commandline
> cd path/to/SI664/scripts
> venv\Scripts\activate
(venv) > pip install -r requirements.txt
```

### UNSD/UNESCO data sets column inspector
Run `inspect_un_data_sets.py` to "inspect" two UN data sets included in the project `/input` directory:

* un_area_country_codes-m49.csv
* unesco_heritage_sites.csv

The script utilizes the [Pandas](https://pandas.pydata.org/) library to peruse the data sets, 
generating a set of column-based *.csv files that contain distinct column values (duplicate 
values and NaN values are filtered out) sorted in ascending order.  The files are stored in the 
project `/output` directory.

#### macOS
```commandline
(venv) $ python3 inspect_un_data_sets.py
```

##### Output

```commandline
INFO: Source file read /absolute/path/to/input/un_area_country_codes-m49.csv
INFO: UNSD M49 regions written to file /absolute/path/to/output/unsd_region.csv
INFO: UNSD M49 sub-regions written to file /absolute/path/to/output/unsd_sub_region.csv
INFO: UNSD M49 intermediate regions written to file /absolute/path/to/output/unsd_intermed_region.csv
INFO: UNSD M49 countries and areas written to file /absolute/path/to/output/unsd_country_area.csv
INFO: UNSD M49 development status written to file /absolute/path/to/output/unsd_dev_status.csv
INFO: Source file read /absolute/path/to/input/unesco_heritage_sites.csv
INFO: UNESCO heritage site countries/areas written to file /absolute/path/to/output/unesco_heritage_site_country_area.csv
INFO: UNESCO heritage site categories written to file /absolute/path/to/output/unesco_heritage_site_category.csv
INFO: UNESCO heritage site regions written to file /absolute/path/to/output/unesco_heritage_site_region.csv
INFO: UNESCO heritage site transboundary values written to file /absolute/path/to/output/unesco_heritage_site_transboundary.csv
```

#### Windows 10
```commandline
(venv) > python inspect_un_data_sets.py
```

##### Output

```commandline
INFO: Source file read C:\path\to\input\un_area_country_codes-m49.csv
INFO: UNSD M49 regions written to file C:\path\to\output\unsd_region.csv
INFO: UNSD M49 sub-regions written to file C:\path\to\output\unsd_sub_region.csv
INFO: UNSD M49 intermediate regions written to file C:\path\to\output\unsd_intermed_region.csv
INFO: UNSD M49 countries and areas written to file C:\path\to\output\unsd_country_area.csv
INFO: UNSD M49 development status written to file C:\path\to\output\unsd_dev_status.csv
INFO: Source file read C:\path\to\input\unesco_heritage_sites.csv
INFO: UNESCO heritage site countries/areas written to file C:\path\to\output\unesco_heritage_site_country_area.csv
INFO: UNESCO heritage site categories written to file C:\path\to\output\unesco_heritage_site_category.csv
INFO: UNESCO heritage site regions written to file C:\path\to\output\unesco_heritage_site_region.csv
INFO: UNESCO heritage site transboundary values written to file C:\path\to\output\unesco_heritage_site_transboundary.csv
```
