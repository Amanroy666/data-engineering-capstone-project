## Fact Table schema:
 |-- airline: string (nullable = true) - Airline used to arrive in U. S.
 |-- arrivalPortId: long (nullable = true) - FK for arrival port dimension table
 |-- cicid: integer (nullable = true) - ID that uniquely identify one record in the dataset
 |-- countryId: long (nullable = true) - FK for country dimension table
 |-- departureDate: date (nullable = true) -  Departure date
 |-- flightNumber: string (nullable = true) - Flight number of Airline used to arrive in U.S.
 |-- ident: string (nullable = true) - FK for airport dimension table
 |-- mode: integer (nullable = true) - Mode of transportation (1 = Air; 2 = Sea; 3 = Land; 9 = Not reported)
 |-- personId: long (nullable = true) - FK for person dimension table
 |-- stateCode: string (nullable = true) - FK for US state dimension table
 |-- statusFlagId: long (nullable = true) - FK for Status flag dimension table
 |-- time: date (nullable = true) - FK for time dimension table
 |-- visa: integer (nullable = true) - Visa codes collapsed into three categories: (1 = Business; 2 = Pleasure; 3 = Student)
 |-- visaType: string (nullable = true) - Class of admission legally admitting the non-immigrant to temporarily stay in U.S.
 
 
## Dimension Tables

### Demographics data schema:

 |-- stateCode: string (nullable = true) - Primary Key
 |-- state: string (nullable = true) - US state of the city
 |-- medianAge: double (nullable = true) - The mean of median of the age of the population of the state
 |-- totalPopulation: double (nullable = true) - Number of the total population
 |-- malePopulation: double (nullable = true) - Number of the male population
 |-- femalePopulation: double (nullable = true) - Number of the female population
 |-- numberOfVeterans: double (nullable = true) - Number of veterans living
 |-- foreignBorn: double (nullable = true) Number of residents of the state that were not born in the state
 |-- averageHouseholdSize: double (nullable = true) - Average size of the houses

 ### Airport data schema:

 |-- ident: string (nullable = true) - Primary Key
 |-- type: string (nullable = true) - Type of the airport
 |-- name: string (nullable = true) - Airport Name
 |-- isoRegion: string (nullable = true) -  ISO code for the region of the airport
 |-- municipality: string (nullable = true) - City where the airport is located
 |-- gps_code: string (nullable = true) - GPS code of the airport
 |-- iata_code: string (nullable = true) - IATA code of the airport
 |-- iso_country: string (nullable = true) -ISO code of the country of the airport
 |-- coordinates: string (nullable = true) - GPS coordinates of the airport
 
  ### Status Flag data schema:

 |-- arrivalFlag: string (nullable = true) - Arrival Flag. Whether admitted or paroled into the US
 |-- departureFlag: string (nullable = true) - Departure Flag. Whether departed, lost visa, or deceased
 |-- updateFlag: string (nullable = true) - Update Flag. Update of visa, either apprehended, overstayed, or updated to PR
 |-- matchFlag: string (nullable = true) - Match flag
 |-- statusFlagId: long (nullable = false) - Primary Key
 
### Arrival Port data schema:

 |-- arrivalPort: string (nullable = true) - Port addmitted through
 |-- numArrivalAddress: long (nullable = false) - Number of different address in the port
 |-- arrivalPortId: long (nullable = false) - Primary key
 
### Visa data schema:

 |-- visa: integer (nullable = true)
 |-- visaType: string (nullable = true)
 |-- visaId: long (nullable = false)
 
### Country data schema:

 |-- country: integer (nullable = true) - 3 digit code of source city for immigration
 |-- countryId: long (nullable = false) - Primary Key

### Person data schema:

 |-- birthYear: integer (nullable = true) - 4 digit year of birth
 |-- gender: string (nullable = true) - Gender
 |-- personId: long (nullable = false) - Primary key
 
### Time data schema:

 |-- time: date (nullable = true) - Primary key
 |-- day: integer (nullable = true) - Day
 |-- month: integer (nullable = true) - Month
 |-- year: integer (nullable = true) - year
 |-- week: integer (nullable = true) - Week
 |-- weekday: integer (nullable = true) - Weekday
 
 
 
 
 