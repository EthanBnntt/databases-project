# Galactic Vacations

Our project will be for a fictional space fairing company that provides space cruises to exotic planets.



Legend:

PK = Primary key
FK = Foreign key
Comp = Composite attibute

## Potential Database structure

### Database structure

Each starship will have a name and a serial number. A starship will be **identified** by a combination of their name and serial number.
Each starship will have a minimum crew required to operate.
The maximum passenger capacity of a starship will also be tracked in a attribute. 
The last service date and next service date will also be tracked in a attribute.

A pilot will be **identified** by an incrementing, unique ID attribute.
Each pilot will have name, date of birth, and flight count attributes.
The pilot's number of years in service and flight count will also be stored in simple attributes.
(TODO: Home Planet)

A passenger will be **identified** by an incrementing, unique ID attribute.
Each passenger will also have name and date of birth attributes.
(TODO: Dependent of)

Each planet will be **identified** by a combination of its name and its star system name.
Each planet will have a climate type attribute.

(TODO: Trip Table)
(TODO: Trip_Participation)

### Starship Table

| ID (name + serial number) | name | serial number | min crew | max passenger capacity | last service date | next service date |
| - | - | - | - | - | - | - |
| PK, NN, UQ | NN | NN | NN | NN | NN | NN |

### Pilots Table

| ID | name | dob | home planet | years of service | flight count |
| - | - | - | - | - | - | 
| PK, NN, UQ | NN | NN | Planet FK, NN | NN | NN |

### Passengers Table:

| ID | name | dob | dependent_of |
| - | - | - | - | 
| PK, NN, UQ | NN | NN | Passenger FK |

### Planets Table

| ID (planet name + star system name) | planet name | star system name | climate type |
| - | - | - | - |
| PK, NN, UQ | NN | NN | NN |

### Trip Table

| ID | starship | pilot | source | destination | departure date |
| - | - | - | - | - | - | 
| PK, NN, UQ | Starship FK, NN | Pilot FK, NN | Planet FK | Planet FK | NN |

### Trip_Participation Relationship Table

| ID | passenger | trip |
| - | - | - |
| PK, NN, UQ | Passenger FK, NN, UQ | Trip FK, NN, UQ |
