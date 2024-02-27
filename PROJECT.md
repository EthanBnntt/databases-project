# Galactic Vacations

Our project will be for a fictional space fairing company that provides space cruises to exotic planets.



Legend:

PK = Primary key
FK = Foreign key
Comp = Composite attibute

## Potential Database structure

### Starship Table

| ID (name + serial number) | name | serial number | min crew | max passenger capacity | last service date | next service date |
| - | - | - | - | - | - | - |
| PK, NN, UQ | NN | NN | NN | NN | NN | NN |

### Pilots Table

| ID | name | dob | home planet | graduated from | years of service | flight count |
| - | - | - | - | - | - | - |
| PK, NN, UQ | NN | NN | Planet FK, NN | NN | NN | NN |

### Passengers Table:

| ID | name | dob | dependent_of |
| - | - | - | - | 
| PK, NN, UQ | NN | NN | Passenger FK |

### Planets Table

| ID (planet name + star system name) | planet name | star system name | average review | climate type |
| - | - | - | - | - |
| PK, NN, UQ | NN | NN | NN | NN |

### Trip Table

| ID | starship | pilot | source | destination | departure date |
| - | - | - | - | - | - | 
| PK, NN, UQ | Starship FK, NN | Pilot FK, NN | Planet FK | Planet FK | NN |

### Trip_Participation Relationship Table

| ID | passenger | trip |
| - | - | - |
| PK, NN, UQ | Passenger FK, NN, UQ | Trip FK, NN, UQ |
