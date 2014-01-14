# Library [NMEA](http://www.maartenlamers.com/nmea/)

## Sommaire

* [gprmc_status](https://github.com/Sryther/RCCar/wiki/GPS#gprmc_status)
* [gprmc_utc](https://github.com/Sryther/RCCar/wiki/GPS#gprmc_utc)
* [gprmc_latitude](https://github.com/Sryther/RCCar/wiki/GPS#gprmc_latitude)
* [gprmc_longitude](https://github.com/Sryther/RCCar/wiki/GPS#gprmc_longitude)
* [gprmc_speed](https://github.com/Sryther/RCCar/wiki/GPS#gprmc_speed)
* [gprmc_course](https://github.com/Sryther/RCCar/wiki/GPS#gprmc_course)

## Methodes

### gprmc_status

**Description**

Returns status character of the last GPRMC sentence received. The status character can be 'A' (for Active) or 'V' (for Void), and signals whether the GPS was active when the positioning was made. If it is void, the GPS could not make a good positioning and you should ignore it, which usually occurs when the GPS is still searching for satellites.

**Syntax**

gps.gprmc_status()

**Returns**

char

### gprmc_utc

**Description**

Returns UTC time of the last GPS positioning. Coordinated Universal Time (UTC) is independent of time-zones and daylight saving adjustments. It is commonly referred to as 'Greenwich Mean Time' (GMT) or 'Zulu' time. A floating-point value is returned which contains the hour, minutes, seconds and milliseconds. For example a value of 235219.281 indicates that the measurement was made at 23h52, 19 seconds and 281 milliseconds UTC.

**Syntax**

gps.gprmc_utc()

**Returns**

float

### gprmc_latitude

**Description**

Returns latitude of GPS position. The latitude is returned as decimal degrees. A positive value indicates the Northern hemisphere, a negative value indicates the Southern hemisphere. For example, Sydney (Australia) is located around -33.853312 decimal degrees latitude, which is 33.853312 degrees latitude on the Southern hemisphere.

**Syntax**

gps.gprmc_latitude()

**Returns**

float

### gprmc_longitude

**Description**

Returns longitude of GPS position. The longitude is returned as decimal degrees. A positive value indicates East of Greenwich (UK), a negative value indicates West of Greenwich. For example, Sydney (Australia) is located around 151.209472 decimal degrees longitude, which is 151.209472 degrees East of Greenwich.

**Syntax**

gps.gprmc_longitude()

**Returns**

float

### gprmc_speed

**Description**

Returns speed-over-ground of GPS. To get the speed in kilometers-per-hour, use gprmc_speed(KMPH). Possible units of speed are KMPH for kilometers-per-hour, MPS for meters-per-second, MPH for miles-per-hour, and KTS for Knots.

**Syntax**

gps.gprmc_speed(unit)

**Parameters**

unit : KMPH, MPS, MPH, or KTS

**Returns**

float

### gprmc_course

**Description**

Returns direction of movement in degrees. North is 0o, East is 90o, South is 180o, West is 270o. For example, if gprmc_course() returns 227.13, then you are moving roughly in South-West direction.

**Syntax**

gps.gprmc_course()

**Returns**

float