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
- Google Maps API (Used for geocoding and place verification.)

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
| **Google Maps API**            | Location search and geocoding           |
| **Requests**                   | API calls to Google Maps                |
| **Jupyter Notebook / VS Code** | Development environment                 |

## Proposed Methodology
1. Download the KMPDC dataset of licensed facilities.
2. Standardize facility names and format locations.
3. Connect to the Google Maps API and fetch the latitude and longitude for each hospital name.
4. Match each KMPDC facility name to the closest Google Maps result based on name similarity and location metadata.
5. Represent each facility on a map of all matched facilities, with each marker showing the facility name and details.

## Expected Outcomes
- A verified dataset of all licensed hospitals in Kenya.
- A Python-based workflow that automates data cleaning, matching, and mapping.
- A map view displaying all verified hospitals and details of each facility.
