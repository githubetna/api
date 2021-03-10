# MCH API 0.1

## Usage

All responses will have the form

```json
{
    "Field1": Field in the table ...,
    "Field1": Field in the table ...
    "..."
}
```

### stations

**Definition**

`GET /API/stations`

**Response**

- `200 OK` on success

```json
[
    {
        "Station": "01AECLIF",
        "StationName": "Eclipse Falls",
        "StationName2": "",
        "TimeZone": "GUY",
        "Longitude": 0,
        "Latitude": 0,
        "Altitude": 69.0,
        "Longitude2": -60.0632,
        "Latitude2": 7.6349,
        "DMSlongitude": "060\u00b003'48''",
        "DMSLatitude": "07\u00b038'06''",
        "Statee": "R1\r",
        "RegManagmt": null,
        "Catchment": null,
        "Subcatchment": null,
        "OperatnlRegion": null,
        "HydroReg": null,
        "RH(2)": null,
        "Municipality": null,
        "CodeB": null,
        "CodeG": null,
        "CodeCB": null,
        "CodePB": null,
        "CodeE": null,
        "CodeCL": null,
        "CodeHG": null,
        "CodePG": null,
        "CodeNw": null,
        "Code1": null,
        "Code2": null,
        "Code3": null,
        "MaxOrdStrgLvl": null,
        "MaxOrdStrgVol": null,
        "MaxExtStrgLvl": null,
        "MaxExtStrgVol": null,
        "SpillwayLevel": null,
        "SpillwayStorage": null,
        "FreeSpillwayLevel": null,
        "FreeSpillwayStorage": null,
        "DeadStrgLevel": null,
        "DeadStrgCapac": null,
        "UsableStorageCapLev": null,
        "UsableStorage": null,
        "HoldingStorage": null,
        "Key1fil": null,
        "Key2fil": null,
        "Key3fil": null,
        "CritLevelSta": null,
        "MinLevelSta": null,
        "MaxLevelSta": null,
        "CritFlow": null,
        "MinDischarge": null,
        "MaxDischarge": null,
        "Stream": null,
        "Distance": null,
        "Infrastructure": null,
        "Type": null,
        "Usee": null
    },
    {
        "Station": "01ARAKAK",
        "StationName": "ARAKAKA",
        "StationName2": "ARAKAKA",
        "TimeZone": "GUY",
        "Longitude": 0,
        "Latitude": 0,
        "Altitude": 241.0,
        "Longitude2": 0.0,
        "Latitude2": 7.495278,
        "DMSlongitude": "",
        "DMSLatitude": "07\u00b029'43''",
        "Statee": "R1\r",
        "RegManagmt": null,
        "Catchment": null,
        "Subcatchment": null,
        "OperatnlRegion": null,
        "HydroReg": null,
        "RH(2)": null,
        "Municipality": null,
        "CodeB": null,
        "CodeG": null,
        "CodeCB": null,
        "CodePB": null,
        "CodeE": null,
        "CodeCL": null,
        "CodeHG": null,
        "CodePG": null,
        "CodeNw": null,
        "Code1": null,
        "Code2": null,
        "Code3": null,
        "MaxOrdStrgLvl": null,
        "MaxOrdStrgVol": null,
        "MaxExtStrgLvl": null,
        "MaxExtStrgVol": null,
        "SpillwayLevel": null,
        "SpillwayStorage": null,
        "FreeSpillwayLevel": null,
        "FreeSpillwayStorage": null,
        "DeadStrgLevel": null,
        "DeadStrgCapac": null,
        "UsableStorageCapLev": null,
        "UsableStorage": null,
        "HoldingStorage": null,
        "Key1fil": null,
        "Key2fil": null,
        "Key3fil": null,
        "CritLevelSta": null,
        "MinLevelSta": null,
        "MaxLevelSta": null,
        "CritFlow": null,
        "MinDischarge": null,
        "MaxDischarge": null,
        "Stream": null,
        "Distance": null,
        "Infrastructure": null,
        "Type": null,
        "Usee": null
    }, ...
]
```

### Query a station

**Definition**

`GET /API/stations/qry_station`

**Arguments**

- `"stn_id":string` a globally unique identifier for this station

**Response**

- `404 Not Found` if the station does not exist
- `200 OK` on success

```json
[
    {
        "Station": "01MATTRG",
        "StationName": "MATTHEWS RIDGE",
        "StationName2": "",
        "TimeZone": "GUY",
        "Longitude": 0,
        "Latitude": 0,
        "Altitude": 0.0,
        "Longitude2": 0.0,
        "Latitude2": 0.0,
        "DMSlongitude": "",
        "DMSLatitude": "",
        "Statee": "R1\r",
        "RegManagmt": null,
        "Catchment": null,
        "Subcatchment": null,
        "OperatnlRegion": null,
        "HydroReg": null,
        "RH(2)": null,
        "Municipality": null,
        "CodeB": null,
        "CodeG": null,
        "CodeCB": null,
        "CodePB": null,
        "CodeE": null,
        "CodeCL": null,
        "CodeHG": null,
        "CodePG": null,
        "CodeNw": null,
        "Code1": null,
        "Code2": null,
        "Code3": null,
        "MaxOrdStrgLvl": null,
        "MaxOrdStrgVol": null,
        "MaxExtStrgLvl": null,
        "MaxExtStrgVol": null,
        "SpillwayLevel": null,
        "SpillwayStorage": null,
        "FreeSpillwayLevel": null,
        "FreeSpillwayStorage": null,
        "DeadStrgLevel": null,
        "DeadStrgCapac": null,
        "UsableStorageCapLev": null,
        "UsableStorage": null,
        "HoldingStorage": null,
        "Key1fil": null,
        "Key2fil": null,
        "Key3fil": null,
        "CritLevelSta": null,
        "MinLevelSta": null,
        "MaxLevelSta": null,
        "CritFlow": null,
        "MinDischarge": null,
        "MaxDischarge": null,
        "Stream": null,
        "Distance": null,
        "Infrastructure": null,
        "Type": null,
        "Usee": null
    }
]
```

## Station groups

`GET /API/stngroups`

**Response**

- `200 OK` on success

```json
[
    {
        "Stngroup": "Guyana"
    },
    {
        "Stngroup": "Hydros"
    },
    {
        "Stngroup": "Myanmar"
    }
]
```

## Query an station group

**Definition**

`GET /API/stngroups/qry_stngroup`

**Arguments**

- `"stngp_id":string` a globally unique identifier for this station group

**Response**

- `404 Not Found` if the station group does not exist
- `200 OK` on success

```json
[
    {
        "Stngroup": "Guyana",
        "Secuen": 10,
        "Station": "Aishalton"
    },
    {
        "Stngroup": "Guyana",
        "Secuen": 20,
        "Station": "Albion"
    },
    {
        "Stngroup": "Guyana",
        "Secuen": 30,
        "Station": "AnnaRegina"
    }
]
```
## Variables

`GET /API/variables`

**Response**

- `200 OK` on success

```json
[
    {
        "Variable": "AirTemp"
    },
    {
        "Variable": "BaromPresMax"
    },
    {
        "Variable": "BaromPresMin"
    },
    {
        "Variable": "BaromPressure"
    }
]
```

## Query an variable

**Definition**

`GET /API/variables/qry_variable`

**Arguments**

- `"var_id":string` a globally unique identifier for this variable

**Response**

- `404 Not Found` if the variable does not exist
- `200 OK` on success

```json
[
    {
        "Variable": "Precipitation",
        "VariabAbbrev": "PR",
        "VariabDescrn": "Precipitaci\u00f3n",
        "TableName": "precipitation",
        "Unit": "mm",
        "TypeDDorDE": "DD",
        "CumulType": "CUMU",
        "NbrDecimal": 2,
        "CalcbyGrp": "MEAN",
        "CalcDTaD": "CUMULAT"
    }
]
```

### Query daily data

**Definition**

`GET /API/data/dailydata`

**Arguments**

- `"stn_id":string` a globally unique identifier for this station
- `"var_id":string` a globally unique identifier for this variable
- `"date_ini":date` the period start date YYYY/MM/DD
- `"date_end":date` the period end date YYYY/MM/DD
- `"datee":date` the date for a single day

A query can be made for a date or a period depending on which parameters are entered.

**Response**

- `404 Not Found` if the variable does not exist or there is no data for the query
- `200 OK` on success

```json
[
    {
        "Station": "01MATTRG",
        "Date": "2013-11-01T00:00:00Z",
        "Value": 7.8
    },
    {
        "Station": "01MATTRG",
        "Date": "2013-11-02T00:00:00Z",
        "Value": 12.2
    },
    {
        "Station": "01MATTRG",
        "Date": "2013-11-03T00:00:00Z",
        "Value": 10.5
    },
    {
        "Station": "01MATTRG",
        "Date": "2013-11-04T00:00:00Z",
        "Value": 0.0
    },
    {
        "Station": "01MATTRG",
        "Date": "2013-11-05T00:00:00Z",
        "Value": 0.0
    },
    {
        "Station": "01MATTRG",
        "Date": "2013-11-06T00:00:00Z",
        "Value": 8.8
    },
    {
        "Station": "01MATTRG",
        "Date": "2013-11-07T00:00:00Z",
        "Value": 9.0
    }
]
```
### Query daily data

**Definition**

`GET /API/data/dailydata`

**Arguments**

- `"stn_id":string` a globally unique identifier for this station
- `"var_id":string` a globally unique identifier for this variable
- `"date_ini":date` the period start date YYYY/MM/DD
- `"date_end":date` the period end date YYYY/MM/DD
- `"datee":date` the date for a single day

A query can be made for a date or a period depending on which parameters are entered.

**Response**

- `404 Not Found` if the variable does not exist or there is no data for the query
- `200 OK` on success

```json
[
    {
        "Station": "01MATTRG",
        "Date": "2013-11-01T00:00:00Z",
        "Value": 7.8
    },
    {
        "Station": "01MATTRG",
        "Date": "2013-11-02T00:00:00Z",
        "Value": 12.2
    },
    {
        "Station": "01MATTRG",
        "Date": "2013-11-03T00:00:00Z",
        "Value": 10.5
    },
    {
        "Station": "01MATTRG",
        "Date": "2013-11-04T00:00:00Z",
        "Value": 0.0
    },
    {
        "Station": "01MATTRG",
        "Date": "2013-11-05T00:00:00Z",
        "Value": 0.0
    },
    {
        "Station": "01MATTRG",
        "Date": "2013-11-06T00:00:00Z",
        "Value": 8.8
    },
    {
        "Station": "01MATTRG",
        "Date": "2013-11-07T00:00:00Z",
        "Value": 9.0
    }
]
```

### Query detail data

**Definition**

`GET /API/data/detaildata`

**Arguments**

- `"stn_id":string` a globally unique identifier for this station
- `"var_id":string` a globally unique identifier for this variable
- `"date_ini":date` the period start date YYYY/MM/DD HH:MM:SS
- `"date_end":date` the period end date YYYY/MM/DD HH:MM:SS
- `"datee":date` the date for a single day YYYY/MM/DD HH:MM:SS

A query can be made for a date or a period depending on which parameters are entered.

**Response**

- `404 Not Found` if the variable does not exist or there is no data for the query
- `200 OK` on success

```json
[
    {
        "Station": "2060",
        "Date": "2019-04-01T00:00:00Z",
        "Value": 0.0
    },
    {
        "Station": "2060",
        "Date": "2019-04-01T00:30:00Z",
        "Value": 0.0
    },
    {
        "Station": "2060",
        "Date": "2019-04-01T01:00:00Z",
        "Value": 0.0
    },
    {
        "Station": "2060",
        "Date": "2019-04-01T01:30:00Z",
        "Value": 0.0
    }
]
```

