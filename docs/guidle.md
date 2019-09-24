# Guidle event Data
## Introduction
Guidle is a provider of event data in Switzerland. This data contain basic information such as the exact location and the date. It is further enriched by descriptive information, contact data and hierarchical categorization.  
We provide you a prepared set of events which take place within the next two weeks.
## Scope
The prepared data contains all guidle events which take place between September 27th and October 11th, 2019.
## Files and format
We provide you with the following 3 json files.
### event.json
array containing 18.556 events
#### Example
```
[
    {
        "event_id" : 2014423,
        "date" : "2019-09-27",
        "start_time" : "19:00:00.0",
        "end_time" : null,
        "title_de" : " Supermoto Ried Muotathal SZ",
        "title_en" : " Supermoto Ried Muotathal SZ",
        "title_fr" : " Supermoto Ried Muotathal SZ",
        "title_it" : " Supermoto Ried Muotathal SZ",
        "short_description_de" : "Die noch ausstehende Bewilligung des Kantons ist eingetroffen, so dass das Supermoto Ried Muotathal nun definitiv stattfinden kann. ",
        "short_description_en" : "The still outstanding permit of the canton has arrived, so that the Supermoto Ried Muotathal can now definitely take place. ",
        "short_description_fr" : "Die noch ausstehende Bewilligung des Kantons ist eingetroffen, so dass das Supermoto Ried Muotathal nun definitiv stattfinden kann. ",
        "short_description_it" : "Die noch ausstehende Bewilligung des Kantons ist eingetroffen, so dass das Supermoto Ried Muotathal nun definitiv stattfinden kann. ",
        "long_description_de" : "Wie angekündigt, hat sich die SAM-Sportkommission nach der Absage des Supermoto Ramsen an die Arbeit gemacht, um eine Ersatzveranstaltung auf die Beine zu stellen. Dem Sport-Vizepräsidenten Sandro Micheletto und seinem Team ist es gelungen, in Ried Muotathal ein geeignetes Gelände zu finden. Die Landbesitzer und Mieter, sowie die Behörden von Gemeinde und Kanton konnten überzeugt werden, dem Anlass die Bewilligung zu erteilen. ",
        "long_description_en" : "As announced, following the cancellation of the Supermoto Ramsen, the SAM Sports Commission set to work to set up an alternative event. Sport Vice-President Sandro Micheletto and his team succeeded in finding a suitable site in Ried Muotathal. The landowners and tenants, as well as the authorities of the municipality and canton were convinced to grant permission for the event. ",
        "long_description_fr" : "Wie angekündigt, hat sich die SAM-Sportkommission nach der Absage des Supermoto Ramsen an die Arbeit gemacht, um eine Ersatzveranstaltung auf die Beine zu stellen. Dem Sport-Vizepräsidenten Sandro Micheletto und seinem Team ist es gelungen, in Ried Muotathal ein geeignetes Gelände zu finden. Die Landbesitzer und Mieter, sowie die Behörden von Gemeinde und Kanton konnten überzeugt werden, dem Anlass die Bewilligung zu erteilen. ",
        "long_description_it" : "Wie angekündigt, hat sich die SAM-Sportkommission nach der Absage des Supermoto Ramsen an die Arbeit gemacht, um eine Ersatzveranstaltung auf die Beine zu stellen. Dem Sport-Vizepräsidenten Sandro Micheletto und seinem Team ist es gelungen, in Ried Muotathal ein geeignetes Gelände zu finden. Die Landbesitzer und Mieter, sowie die Behörden von Gemeinde und Kanton konnten überzeugt werden, dem Anlass die Bewilligung zu erteilen. ",
        "homepage" : "https://www.s-a-m.ch/Termine/EventsDetails/EID/5285/ModuleID/1442?Title=Supermoto+Ried+Muotathal+SZ",
        "price_information" : "Saturday:\r\nAdults CHF 15.00\r\nChildren up to 14 free of charge\r\n\r\nSunday:\r\nAdults CHF 20.00\r\nChildren up to 14 free of charge",
        "thumbnail_url" : "https://d37dhr5745n0y2.cloudfront.net/c/00/b1/c00b1ea5fea11022394709b8ff574f209d30f95f.jpg",
        "address_street" : "Bacheggli",
        "address_address_line" : "Micheletto Sandro",
        "address_zip" : "6434",
        "address_city" : "Illgau",
        "address_country" : "Schweiz",
        "address_venue_name" : "Stoos-Muotatal Tourismus GmbH",
        "address_latitude" : 46.9872623,
        "address_longitude" : 8.7277275
    },
    ...
]
```
### category.json
Categories are hierarchacly structured. They are stored as a flat array. The Hierarchy is obtained by optional parent references.
#### Example
```
[
    ... 
    {
        "category_id" : 11,
        "title_de" : "Ausstellungen",
        "title_en" : "Exhibitions",
        "title_fr" : "Expositions",
        "title_it" : "Esposizioni",
        "parent_category_id" : null
    }, {
        "category_id" : 43,
        "title_de" : "Archäologie / Ur- / Frühgeschichte",
        "title_en" : "Archaeology / prehistoric history",
        "title_fr" : "Archéologie / histoire préhistorique",
        "title_it" : "Archeologia / stoira preistorica",
        "parent_category_id" : 11
    }
    ...
]
```
### event_category.json
This json document contains a many to many mapping between events and categories.
#### Example
```
[
    {
        "event_id" : 1376065,
        "category_id" : 1147
    }, {
        "event_id" : 1376065,
        "category_id" : 2443
    }, {
        "event_id" : 1376077,
        "category_id" : 1147
    }, {
        "event_id" : 1376077,
        "category_id" : 2443
    },
...
]
```