# US-Gun-Violence
Building a comprehensive dataset to analyze US gun violence trends using Google Maps' Geocoding API and BeautifulSoup

Project data: 

1. Gun violence data from Kaggle: `gun-violence.csv` 

* incident_id
* date: Date of crime
* stateL State of crime
* city_or_county: City/ County of crime
* address: Address of the location of the crime
* n_killed: Number of people killed
* n_injured: Number of people injured
* incident_url: URL regarding the incident
* source_url: Reference to the reporting source
* incident_url_fields_missing: TRUE if the incident_url is present, FALSE otherwise
* congressional_district: Congressional district id
* gun_stolen: Status of guns involved in the crime (i.e. Unknown, Stolen, etc...)
* gun_type: Typification of guns used in the crime
* incident_characteristics: Characteristics of the incidence
* latitude: Location of the incident
* location_description
* longitude: Location of the incident
* n_guns_involved: Number of guns involved in incident
* notes: Additional information of the crime
* participant_age: Age of participant(s) at the time of crime
* participant_age_group: Age group of participant(s) at the time crime
* participant_gender: Gender of participant(s)
* participant_name: Name of participant(s) involved in crime
* participant_relationship: Relationship of participant to other participant(s)
* participant_status: Extent of harm done to the participant
* participant_type: Type of participant
* sources: Participants source
* state_house_district: Voting house district
* state_senate_district: Territorial district from which a senator to a state legislature is elected.
________________________________

2. Shooting locations - integrated with lat and long data pulled from Google API: `guns_location.csv`

* address: address of the shooting
* formatted address: address in the format that Google API can read and pass
* latitude: coordinates of the address
* longitude: coordinates of the address
* number of result: 1 if only 1 point is found on the map, to make sure that we don't get 2 points have the same address. 
* status: OK if the loop successfully geocode the address 
* zipcode: zip code of the incident
________________________________

3. Gun violence data merged with lat and long data from API: `geodata.csv`

* location: newly created column that combines address with state and city/county 
* latitude: coordinates of the address
* longitude: coordinates of the address
* date: Date of crime
* state: State of crime
* city_or_county: City/ County of crime
* address: Address of the location of the crime
* n_killed: Number of people killed
* n_injured: Number of people injured
* incident_url: URL regarding the incident
* source_url: Reference to the reporting source
* incident_url_fields_missing: TRUE if the incident_url is present, FALSE otherwise
* congressional_district: Congressional district id
* gun_stolen: Status of guns involved in the crime (i.e. Unknown, Stolen, etc...)
* gun_type: Typification of guns used in the crime
* incident_characteristics: Characteristics of the incidence
* latitude: Location of the incident
* location_description
* longitude: Location of the incident
* n_guns_involved: Number of guns involved in incident
* notes: Additional information of the crime
* participant_age: Age of participant(s) at the time of crime
* participant_age_group: Age group of participant(s) at the time crime
* participant_gender: Gender of participant(s)
* participant_name: Name of participant(s) involved in crime
* participant_relationship: Relationship of participant to other participant(s)
* participant_status: Extent of harm done to the participant
* participant_type: Type of participant
* sources: Participants source
* state_house_district: Voting house district
* state_senate_district: Territorial district from which a senator to a state legislature is elected.
_______________________________

4. Crime data scraped from Wikipedia: `crime_data.csv`
state

* city
* population
* vc_total: total number of violence crimes 
* vc_murder: total number of murders
* vc_rape: total number of rapes
* vc_robbery: total number of robberies
* vc_aggravatedAssault: total number of aggrevated assauls
* pc_total: total number of property crime
* pc_burglary: total number of burglars
* pc_larcenyTheft: total number of larceny thefts
* pc_motorVehicleTheft: total number of motor vehicle thefts 
* pc_arson: total number of arson 
_______________________________

5. Income data scraped from Wikipedia: `income_data.csv`
rank

* county
* state
* per capita: income per capita
* median household income
* median family income
* population: city/county population 
* number of households 
_______________________________

6. Final dataset: `final_data.csv`

* location: newly created column that combines address with state and city/county 
* latitude: coordinates of the address
* longitude: coordinates of the address
* date: Date of crime
* state: State of crime
* city_or_county: City/ County of crime
* address: Address of the location of the crime
* n_killed: Number of people killed
* n_injured: Number of people injured
* incident_url: URL regarding the incident
* source_url: Reference to the reporting source
* incident_url_fields_missing: TRUE if the incident_url is present, FALSE otherwise
* congressional_district: Congressional district id
* gun_stolen: Status of guns involved in the crime (i.e. Unknown, Stolen, etc...)
* gun_type: Typification of guns used in the crime
* incident_characteristics: Characteristics of the incidence
* latitude: Location of the incident
* location_description
* longitude: Location of the incident
* n_guns_involved: Number of guns involved in incident
* notes: Additional information of the crime
* participant_age: Age of participant(s) at the time of crime
* participant_age_group: Age group of participant(s) at the time crime
* participant_gender: Gender of participant(s)
* participant_name: Name of participant(s) involved in crime
* participant_relationship: Relationship of participant to other participant(s)
* participant_status: Extent of harm done to the participant
* participant_type: Type of participant
* sources: Participants source
* state_house_district: Voting house district
* state_senate_district: Territorial district from which a senator to a state legislature is elected
* population
* vc_total: total number of violence crimes 
* vc_murder: total number of murders
* vc_rape: total number of rapes
* vc_robbery: total number of robberies
* vc_aggravatedAssault: total number of aggrevated assauls
* pc_total: total number of property crime
* pc_burglary: total number of burglars
* pc_larcenyTheft: total number of larceny thefts
* pc_motorVehicleTheft: total number of motor vehicle thefts 
* pc_arson: total number of arson 
* rank
* per capita: income per capita
* median household income
* median family income
* population: city/county population 
* number of households 
