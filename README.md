# Comprehensive Urban Analysis Toolkit

## Overview

The Comprehensive Urban Analysis Toolkit is an integrated educational project designed to analyze urban environments through a combination of raster and vector data processing, spatial analysis techniques, and OpenStreetMap (OSM) data. This toolkit encompasses three main components that work together to provide a thorough assessment of territorial conditions.

### Component 1: Raster Image Classification

This method focuses on classifying raster images using K-nearest neighbors (KNN) and vector data. Key steps include:

- **Loading Raster and Vector Data**: The toolkit reads raster images (e.g., TIFF files) and vector data (e.g., GeoJSON files) to extract relevant features.
- **Feature Extraction**: It extracts pixel values from the raster data based on the geometries defined in the vector data.
- **Classification**: A KNN classifier is trained on the extracted features to classify the raster pixels into different categories.
- **Visualization**: The results are visualized by overlaying the classified raster data with the vector geometries.

![Digitized map of functional zoning from regulatory documentation for Vasilevsky Island PZZ](img/021.png)


### Component 2: Image Processing and Text Recognition

This method expands the analysis capabilities by processing a bitmap image for vectorization and text recognition using EasyOCR. This method is used to digitize functional zoning maps from the regulatory documentation of the Rules of Land Use and Development. The main steps include:

- **Image Segmentation**: The toolkit applies KMeans clustering to segment the image into different regions based on color.
- **GeoTIFF Creation**: It generates a GeoTIFF file from the segmented image, preserving geographical information.
- **Text Recognition**: Using EasyOCR, the toolkit extracts text from the processed images and converts it into geospatial data points.
- **Land Use Assignment**: The recognized text is categorized into predefined land use types, enriching the dataset for further analysis.

![](img/5469847474198935614.png)

![](img/Vasikevskiy.png)

### Component 3: Method for determining the functional zoning of a territory and classifying zones according to the degree of urbanization

This method is based on data from the OSM to determine the functional purpose of the territory and classify zones according to the degree of urbanization. If the data is missing or unreliable, it can be supplemented using the methods described above. Key features include:

- **OSM Data Extraction**: The toolkit fetches building and land-use data from OpenStreetMap.
- **Building Classification**: It classifies buildings into residential and non-residential categories based on OSM tags.
- **Land Use Processing**: The toolkit filters out water bodies and digitizes functional zoning maps.
- **Grid Generation**: It creates polytonal grids for undefined areas and assigns land use categories to grid cells.
- **Urbanization Analysis**: The toolkit measures urban intensity and identifies spatial patterns, providing insights into urban development.

![](img/010.png)

![](img/09.png)

![](img/011-копия.png)

![](img/015.png)

![](img/016.png)

![](img/019.png)

![](img/18.png)
  
### Libraries Used in Each Code File

#### 1. Raster Image Classification Code
- **Libraries Used**:
  - **GeoPandas**: For managing vector data and performing spatial analyses.
  - **Rasterio**: For reading and writing geospatial raster data.
  - **Scikit-learn**: For implementing the KNN classifier.
  - **NumPy**: For numerical computing, providing support for large multi-dimensional arrays and matrices, along with mathematical functions to operate on these arrays.
  
- **Installation Command**:
```bash
  pip install geopandas rasterio scikit-learn numpy
```

### Image Processing and Text Recognition Code
- **Libraries Used**:
  - **OpenCV**: For image segmentation and processing.
  - **EasyOCR**: For optical character recognition to extract text from images.
  - **GDAL**: For creating GeoTIFF files and handling raster data.
  - **Shapely**: For manipulation and analysis of planar geometric objects, allowing for the creation and manipulation of geometric shapes such as points, lines, and polygons.
- **Installation Command**:
```bash
pip install opencv-python easyocr gdal geopandas sklearn shapely
```
### Method for determining the functional zoning of a territory and classifying zones according to the degree of urbanization
- **Libraries Used**:
  - **OSMnx**: For retrieving, modeling, analyzing, and visualizing street networks from OpenStreetMap, enabling the analysis of urban infrastructure.
  - **Pandas**: For data manipulation and analysis, providing data structures like DataFrames for handling structured data efficiently.
- **Installation Command**:
```bash
pip install geopandas shapely pandas osmnx numpy
```

### Author
- **Egor Andreevich Chichkov, a graduate student at the Institute of Design and Urban Studies at ITMO University**
