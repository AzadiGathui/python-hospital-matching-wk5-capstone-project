# Kenyan Licensed Hospitals Map
Visualizing all licensed hospitals in Kenya on a map.

## Problem Statement
Accessing accurate, up-to-date information about licensed hospitals in Kenya is often difficult.
While the Kenya Medical Practitioners and Dentists Council (KMPDC) maintains a searchable list of licensed facilities, the data is not easily accessible in a visual format.
This project aims to bridge that gap by integrating KMPDC data with the Google Maps API to automatically geocode and visualize all licensed hospitals on a map.

## Objectives
- Extract hospital data from the official KMPDC licensed health facilities list.
- Identify geographic coordinates for each facility.
- Match and validate hospital names from KMPDC data with Google Maps search results.
- Create a map showing all licensed hospitals across Kenya.

## Dataset Description
### Source
- Kenya Medical Practitioners and Dentists Council (KMPDC) (https://kmpdc.go.ke/Registers/HealthFacilities)
- Google My Maps (Used for geocoding and place verification.)

### Features
Typical attributes include:
- Facility Name
- Facility Type (e.g., hospital, clinic, dispensary)
- Level (e.g. Level 2A, Level 6)
- County
- License Status (active/inactive)
- Latitude, Longitude (added via API)

### Size
Approximately 14,000+ licensed health facilities (as per the latest KMPDC list).

## Tools & Tech to be used
| Tool / Library                 | Purpose                                 |
| ------------------------------ | --------------------------------------- |
| **Python 3.x**                 | Core programming language               |
| **Google My Maps**             | Creatign a custom map                   |
| **Requests**                   | API calls to Google Maps                |
| **Jupyter Notebook / VS Code** | Development environment                 |

## Methodology
1. Create and activate a virtual environment.
2. Install and import the following resources:
    1. `requests` module  [link to docs](https://requests.readthedocs.io/en/latest/)
    2. `BeautifulSoup` class from `bs4` module    [link to docs](https://www.crummy.com/software/BeautifulSoup/bs4/doc/#)
    3. `csv` module
3. Download the KMPDC dataset of licensed facilities and store it in a csv.
4. Standardize facility names and create a geocoding search term by combining facility name, address, facility type and county, and adding 'Kenya' at the end.
5. Save all the information into a csv.
6. Upload the csv onto Google My Maps for geocoding.
7. Group by facility type and update the markers/icons to match the facility type.

## Expected Outcomes
- A verified dataset of all licensed hospitals in Kenya.
- A Python-based workflow that automates data scraping and cleaning.
- A map view displaying all verified hospitals and details of each facility.
