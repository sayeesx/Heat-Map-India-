# India Crime Density Heatmap

This project visualizes the **crime distribution across India** using a spatial heatmap built from city level crime data.

![Heatmap Example](./null)

---

## Objective

- Visualize crime-prone areas across Indian geography.
- Help authorities identify regional hotspots.
- Build a reusable pipeline for other datasets/scenarios.

---

##Data Sources

- **Crime Data**: `india_event_data.csv` — includes city names and crime events.
- **Boundaries**: `gadm41_IND_1.json` — GeoJSON file of Indian state borders.

---

##  How It Works

1. **City Geocoding**  
   Converts city names into latitude/longitude using OpenStreetMap (Nominatim API).

2. **GeoDataFrame Conversion**  
   Transforms data into geographic coordinates and reprojects for spatial math.

3. **Clipping & Gridding**  
   A 50km x 50km grid is generated to bin events by location.

4. **Heatmap Visualization**  
   Uses matplotlib to generate a PNG with crime intensity and overlays state borders.

---

## Technologies Used

- `Python`, `pandas`, `geopandas`
- `matplotlib`, `numpy`, `shapely`
- `geopy` for geocoding cities

---

## Output

- High-resolution PNG image (`india_crime_heatmap.png`)
- Highlights crime hotspots with color intensity

---

## Reusability

### You can reuse this project for:

- Other countries: Replace the boundary file (GADM link below)
- Other data: Replace the crime CSV with pollution, health, etc.
- Custom visualizations: Change title, grid size, or colormaps.

🔗 Download boundaries: [https://gadm.org/download_country.html](https://gadm.org/download_country.html)
🔗 Download Indian Crimes Dataset: https://www.kaggle.com/datasets/sudhanvahg/indian-crimes-dataset
🔗 Download Indian city database or any other country's : https://simplemaps.com/data/in-cities

---

## Future Ideas

- Add year or month filtering
- Add type-specific crimes (e.g., theft vs assault)
- Make it interactive (e.g., with Plotly or Folium)
