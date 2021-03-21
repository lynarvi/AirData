# AirData

## Access AirData

    download.file("https://aqs.epa.gov/aqsweb/airdata/annual_conc_by_monitor_2014.zip",destfile="Air.zip")
    con = unz("Air.zip", filename = "annual_conc_by_monitor_2014.csv")
    con2 = gzcon(con)
    AirData = read_csv(con2)
