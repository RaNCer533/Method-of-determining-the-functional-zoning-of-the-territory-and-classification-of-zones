Comprehensive Territorial Assessment Toolkit
An educational project for analyzing urban environments using OpenStreetMap (OSM) data and spatial analysis techniques.

Overview
This project demonstrates a methodology for assessing territorial conditions by:

Classifying buildings and land use zones
Processing geospatial data
Creating supplemental grids for undefined areas
Evaluating urbanization levels
WorkFlow Diagram

Features
OSM Data Extraction: Fetch building/land-use data from OpenStreetMap
Building Classification:
Residential vs non-residential categorization
Object validation checks
Land Use Processing:
Water feature exclusion
Functional zoning map digitization
Grid Generation:
Polytonal grid creation for undefined territories
Urbanization Analysis:
Urban intensity measurement
Spatial pattern identification
Methodology
1. Data Collection
Extract OSM data for target territory
Classify buildings using tags:
building: residential
building: commercial
building: industrial
2. Data Processing
1. Land Use Classification:
   - Filter water bodies (natural=water)
   - Categorize zones using OSM landuse tags

2. Undefined Area Handling:
   - Create polytonal grid overlay
   - Digitize official zoning maps
   - Assign landuse categories to grid cells
Structure
Examples directory: Jupyter Notebook file with source code with full pipeline
Data directory: directory with main information sources for calculations
Installation
pip install -r requirements.txt

Usage
Install requirements from requirements.txt
Open Jupyter Notebook file in Examples directory
Follow the pipeline in Jupyter Notebook file
Contributors
Chichkov Egor Andreevich, IDU ITMO @RaNCer533 — methodology design, core implementation, initial codebase.
