
# esp32-sml-reader-Che

## TL;DR
Code for letting an ESP32 read sml data from a smart meter via its IR
interface.

## Values
You may define which fields/values you want to read from the smartmeter. I'm
reading
- 1.8.0 : energy in kWh from grid so far
- 2.8.0 : energy in kWh to grid so far, from PV unit
- 16.7.0 : current power in W passing the smartmeter (may be different in my experience -> Leon)
You may want to read others. Find a list of OBIS identifiers at https://de.wikipedia.org/wiki/OBIS-Kennzahlen
.

## Targets
The first version supports three backends as target:
- Influx tineseries DB, e.g. at corlysis.com or at own site. You may use Grafana to visualize the data later.
- Volkszähler.org instance, presumably on a raspberry at home. Find more info at https://www.volkszaehler.org/
- Plain web server, in my case just to have the values in the web servers error log, for debugging purposes. Of course you may use this with an own PHP or Python script to write the data to a database.

