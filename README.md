# Petalaris Data Pipeline

## Installation & Setup

1. Clone this repository:
   ```bash
   git clone <repo-url>
   cd petalaris-data
   ```

2. Create and activate the Conda environment from `environment.yml`:
   ```bash
   conda env create -f environment.yml
   conda activate petalaris-env
   ```

3. Install Python requirements (optional, for pip-based setup or updates):
   ```bash
   pip install -r requirements.txt
   ```

## Data Structure
- All processed and raw data are in the `data/` folder.
- Notebooks are in the `notebooks/` folder.

## Usage
- Run Jupyter notebooks for data processing and analysis.

## Notes
- Make sure Conda is installed before setup.
- The environment name is `petalaris-env`.

## Project Overview
This project is a spatial data processing pipeline that aggregates various data sources into grid-based features for Malang city.

### Pipeline Workflow
1. **OSM Data Processing** (`01`-`02`): Extracts raw Points of Interest (POIs) such as schools, markets, and parks from OpenStreetMap and aggregates them into spatial grids.
2. **Crowd & Popular Time Forecasting** (`03`, `06`): Analyzes venue popular times to forecast crowd patterns and maps these crowd densities to the grids.
3. **Map Visualization** (`04`): Generates map-based visualizations of the spatial data (e.g., `venue_coverage_map.html`).
4. **Venue to Grid Mapping** (`05`): Correlates physical venue locations with predefined spatial grids.
5. **Weather Integration** (`08`): Integrates historical weather data into the pipeline.
6. **Master Feature Generation** (`07`): Consolidates POI density, venue data, crowd patterns, and weather into a final comprehensive dataset (`master_features_malang.csv`) for downstream analysis or modeling.
