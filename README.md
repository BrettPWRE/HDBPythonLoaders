# Python Based HDB Data Loaders

# Overview

This repository contains two python based data loaders for HDB: xl2hdb.py and wrcc2hdb.py. A brief description of each is below, with more detailed documentation available in separate .md files for each loader.

## xl2hdb

The xl2hdb.py Python data loader is designed for loading data from Excel spreadsheets to the HDB R tables. Data is written to the r_base table with an 'O' in the overwrite_flag field by default, with metadata values defined in the source data spreadsheets. It relies on the generic lib/hdb.py class, which provides database connection and access to HDB SQL packages like ts_xfer for writing arrays of real data.

[Full xl2hdb documentation](xl2hdb.md)

## wrcc2hdb

The wrcc2hdb.py Python data loader is designed to load monthly precipitation and average temperature from the Western Regional Climate Center (WRCC) to the HDB R tables. WRCC data is used to compute Upper Colorado consumptive use and loss (CUL) data, but could also be used for other purposes by mapping the loader to different time series. By default, data written by the loader includes an 'O' in the r_base.overwrite_flag field. Wrcc2hdb.py relies on the generic lib/hdb.py class, which provides database connection and access to HDB SQL packages like ts_xfer for writing arrays of real data.

[Full wrcc2hdb documentation](wrcc2hdb.md)