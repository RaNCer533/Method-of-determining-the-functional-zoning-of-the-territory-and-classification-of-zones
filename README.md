# Comprehensive Urban Analysis Toolkit

## Overview

The Comprehensive Urban Analysis Toolkit is an integrated educational project designed to analyze urban environments through a combination of raster and vector data processing, spatial analysis techniques, and OpenStreetMap (OSM) data. This toolkit encompasses three main components that work together to provide a thorough assessment of territorial conditions.

### Component 1: Raster Image Classification

This component focuses on classifying raster images using K-nearest neighbors (KNN) and vector data. Key steps include:

- **Loading Raster and Vector Data**: The toolkit reads raster images (e.g., TIFF files) and vector data (e.g., GeoJSON files) to extract relevant features.
- **Feature Extraction**: It extracts pixel values from the raster data based on the geometries defined in the vector data.
- **Classification**: A KNN classifier is trained on the extracted features to classify the raster pixels into different categories.
- **Visualization**: The results are visualized by overlaying the classified raster data with the vector geometries.

### Component 2: Image Processing and Text Recognition

This component enhances the analysis by processing images and recognizing text using EasyOCR. The main steps include:

- **Image Segmentation**: The toolkit applies KMeans clustering to segment the image into different regions based on color.
- **GeoTIFF Creation**: It generates a GeoTIFF file from the segmented image, preserving geographical information.
- **Text Recognition**: Using EasyOCR, the toolkit extracts text from the processed images and converts it into geospatial data points.
- **Land Use Assignment**: The recognized text is categorized into predefined land use types, enriching the dataset for further analysis.

### Component 3: Comprehensive Territorial Assessment

This component utilizes the outputs from the first two components to perform a detailed territorial assessment using OSM data. Key features include:

- **OSM Data Extraction**: The toolkit fetches building and land-use data from OpenStreetMap.
- **Building Classification**: It classifies buildings into residential and non-residential categories based on OSM tags.
- **Land Use Processing**: The toolkit filters out water bodies and digitizes functional zoning maps.
- **Grid Generation**: It creates polytonal grids for undefined areas and assigns land use categories to grid cells.
- **Urbanization Analysis**: The toolkit measures urban intensity and identifies spatial patterns, providing insights into urban development.

## Installation

To set up the project, run the following command to install the necessary dependencies:

```bash
pip install -r requirements.txt
```

### Author
-**Egor Andreevich Chichkov, a graduate student at the Institute of Design and Urban Studies at ITMO University**
