### DATA

##### Metadata about air quality

[http://airviro.klab.ee/] (Eesti välisõhu kvaliteet)

| Attr  | example value | unit    | Description                 |
| ----- | ------------- | ------- | --------------------------- |
| SO2   | 0,23          | µg/m³ | Vääveldioksiid            |
| NO2   | 0,02          | µg/m³ | Lämmastikdioksiid          |
| CO    | 0,24          | mg/m³  | Süsinikoksiid              |
| O3    | 70,05         | µg/m³ | Osoon                       |
| PM10  | 8,55          | µg/m³ | Peened osakesed             |
| PM2.5 | 4,72          | µg/m³ | Eriti peened osakesed       |
| TEMP  | 9,72          | C       | Temperatuur                 |
| WD10  | 204,40        | deg     | Tuule suund 10 m kõrgusel  |
| WS10  | 1,56          | m/s     | Tuule kiirus 10 m kõrgusel |

Process:

* Using python script extract data from [http://airviro.klab.ee] (fetch_air.ipynb)
* Using Openrefine transform columns into correct format (use data_tranform_air.json)
* Use Openrefine export to SQL.

### Metadata about electricity:

Downloaded from https://e.elering.ee/#/, need to log in and can only be accessed by the contract owner.

| Attr  | example value | unit  | Description                 |
|-------|---------------|-------| --------------------------- |
| Elec  | 2,42          | kWh   | tunnis kulunud elekter            |
| Price | 70,03         | €/MWh | Börsi hetke hind          |

* Nord Pool hourly data from [https://www.nordpoolgroup.com/en/Market-data1/Dayahead/Area-Prices/EE/Hourly/?view=table]
* Downloaded file to be fixed with Openrefine (use data_transform_el.json)
* Use Openrefine export to SQL.