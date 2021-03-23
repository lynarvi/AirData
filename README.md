# AirData

## Access AirData

https://aqs.epa.gov/aqsweb/airdata/download_files.html

https://aqs.epa.gov/aqsweb/airdata/download_files.html#eighthour

    install.packages("readr")
    library("readr")
    download.file("https://aqs.epa.gov/aqsweb/airdata/annual_conc_by_monitor_2014.zip",destfile="Air.zip")
    con = unz("Air.zip", filename = "annual_conc_by_monitor_2014.csv")
    con2 = gzcon(con)
    AirData = read_csv(con2)
    
     install.packages("readr")
    library("readr")
    download.file("https://aqs.epa.gov/aqsweb/airdata/8hour_44201_2014.zip",destfile="Air.zip")
    con = unz("Air.zip", filename = "8hour_44201_2014.csv")
    con2 = gzcon(con)
    AirData = read_csv(con2)
    
    > library("tidyr")
    > library("stringr")
    > names(AirData) = str_replace_all(names(AirData), c(" " = "." , "," = ""))
    > View(AirData)

