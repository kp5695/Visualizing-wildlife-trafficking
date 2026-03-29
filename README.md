# Wildlife Trafficking Visualizations

This project contains interactive D3.js visualizations to explore wildlife trafficking incidents and trends from 2015-2023.

## Visualizations

### 1. Choropleth Map (`choropleth_map.html`)

An interactive map of the world showing wildlife trafficking incidents by country with year-based filtering.

**Features:**
- Color-coded countries representing incident intensity (darker red = more incidents)
- Year selector dropdown to filter data by year
- Interactive tooltips displaying incident details when hovering over countries
- Quantile-based color scale for effective data representation

**How to Use:**
1. Open `choropleth_map.html` in your web browser
2. Use the "Select Year" dropdown to view trafficking data for different years
3. Hover over countries to see detailed incident information

**Data Source:**
- [world_countries.json](data/world_countries.json) - World map topology
- [wildlife_trafficking.csv](data/wildlife_trafficking.csv) - Incident data by country and year

---

### 2. Top Trafficked Species Bar Chart (`trafficking_viz_d3.html`)

An interactive bar chart displaying the top 5 most trafficked wildlife species from 2015-2023.

**Features:**
- Horizontal bar chart with 5 color-coded species categories
- Clear visualization of trafficking incident counts per species
- Professional styling with labeled axes

**How to Use:**
1. Open `trafficking_viz_d3.html` in your web browser
2. View the top 5 most trafficked species ranked by incident count

**Data Source:**
- [species_data.csv](species_data.csv) - Trafficking counts aggregated by species

---

## Setup & Getting Started

### Requirements
- A modern web browser (Chrome, Firefox, Safari, Edge)
- Local web server for proper data loading (required due to CORS restrictions)

### Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd Visualizing-wildlife-trafficking
   ```

2. Start a local web server from the project directory:
   ```bash
   # Using Python 3
   python -m http.server 8000
   
   # Using Python 2
   python -m SimpleHTTPServer 8000
   
   # Using Node.js (http-server)
   npx http-server
   ```

3. Open your browser and navigate to:
   - Choropleth Map: `http://localhost:8000/choropleth_map.html`
   - Species Bar Chart: `http://localhost:8000/trafficking_viz_d3.html`

---

## File Structure

```
Visualizing-wildlife-trafficking/
├── choropleth_map.html          # Interactive world map visualization
├── trafficking_viz_d3.html      # Top species bar chart visualization
├── species_data.csv             # Aggregated species trafficking data
├── data/
│   ├── wildlife_trafficking.csv # Country-level trafficking incidents
│   └── world_countries.json     # World map topology data
└── README.md                    # This file
```

---

## Dependencies

Both visualizations use the following D3.js libraries (loaded from CDN or local lib folder):
- **D3.js v5** - Core visualization library
- **TopoJSON v2** - For geographic data handling
- **D3-Legend** - For color legend rendering
- **D3-Tip** - For interactive tooltips
- **D3-Geo-Projection** - For map projections

---

## Data Description

### wildlife_trafficking.csv
Contains wildlife trafficking incidents aggregated by country and year:
- **Year** - Year of incident (2015-2023)
- **Country of Incident** - Country where trafficking occurred
- **Number_of_Incidents** - Count of trafficking incidents
- **Average_Fine** - Average fine imposed
- **Average_Imprisonment** - Average imprisonment duration

### species_data.csv
Aggregated trafficking data by species:
- **species** - Wildlife species name
- **count** - Total number of trafficking incidents

### world_countries.json
TopoJSON format containing world country boundaries and geographic data for map rendering.

---

## Insights

- **Elephants** are the most trafficked species with 3,164 incidents
- **Pangolins** rank second with 856 incidents
- Wildlife trafficking incidents vary significantly by country and year
- Key hotspots can be identified through the choropleth map visualization

---

## Author

Created as part of CSE6242 coursework - Data Visualization

---
