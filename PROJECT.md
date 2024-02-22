# Galactic Vacations

Our project will be for a fictional space fairing company that provides space cruises to exotic planets.



Legend:

PK = Primary key
FK = Foreign key
Comp = Composite attibute

## Potential Database structure

### Starship Table

ID (name, serial number) PK

name (comp of ID)

Serial number (comp of ID)

min crew 

max passenger capacity

last service date

next service date

### Pilots Table
 
ID num. PK

Name

DoB 

home planet

graduated from

years of service

total number of flights


### Passengers Tables:

Passenger_ID_num PK 

name

DoB 

Trip_number

Dependant of (null if adult)

### Locations Table

location_ID (name, starsystem) PK

name (Comp of trip_ID)

Star system (Comp of trip_ID)

average review

climate type


### Trip Table

trip_num PK

Starship FK (ID from Starships table)

Pilot FK (ID_num from Pilots table)

Destination FK (location_ID from Locations Table)

Passengers FK (Passenger_ID_num form Passengers Table)

Departure date

