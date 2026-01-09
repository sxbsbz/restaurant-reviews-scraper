# Google Places Reviews Scraper

This is a Python-based scraper that collects **restaurant reviews** from the **Google Places API (v1)** using a grid-based search and exports the results in a CSV format using pandas.  

---

## Features

- Grid-based geographic scanning
- Uses Google's Places API (new)
- Extracts:
  - Place ID & name
  - Latitude & longitude
  - Review text
  - Google Maps links
- Exports clean, UTF-8 encoded CSV
- Configurable API limits and delays

---

## Dataset Output

The script generates a CSV file with the following columns:

| Column Name | Description |
|------------|------------|
| `place_id` | Google Place unique ID |
| `place_name` | Restaurant name |
| `latitude` | Latitude |
| `longitude` | Longitude |
| `review_text` | Review content |
| `google_maps_uri` | Google Maps place link |
| `reviews_uri` | Google Maps reviews link |

Each **row corresponds to a single review**.

---

## Configuration

All main parameters are defined at the top of the script:

```python
OUTPUT_CSV = "db_restaurant_reviews.csv"
MAX_API_CALLS = 800 
SLEEP_SECONDS = 0.2
SEARCH_RADIUS_METERS = 600
GRID_STEP_METERS = 450
LANGUAGE_CODE = "fr"
REGION_CODE = "FR"
