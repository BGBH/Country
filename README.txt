# Plotting Country's Publications and Collaborative Patterns 

## Overview
This repository provides a Jupyter Notebook for preprocessing and visualizing geospatial bibliometric data. The workflow demonstrates how to create intuitive plots, such as publication density maps and collaboration visualizations, that are highly relevant for bibliometric analysis.

## Features
- Data Preprocessing: Utilize pandas for efficient data manipulation. 
- Geospatial Visualization: Leverage geopandas and matplotlib to create high-quality geospatial visualizations. 
- Comprehensive Analysis: Combine publication data and country collaboration data into a single visual representation. 
- Customizable Arrows: Plot directional arrows with varying widths and colors to indicate collaboration frequency between countries. 

## Datasets and Variables
Input Datasets
    1. country_of_author
        ◦ Source: Corresponding author countries dataset 
        ◦ Columns: 
            ▪ Country: Name of the country (renamed to NAME during processing). 
            ▪ Publications: Total number of publications from the country. 
    2. country_of_colab
        ◦ Source: Country collaboration dataset 
        ◦ Columns: 
            ▪ From: Source country in the collaboration. 
            ▪ To: Destination country in the collaboration. 
            ▪ Frequency: Number of collaborations between the source and destination. 
    3. world
        ◦ Source: Geospatial shapefile dataset 
        ◦ Details: Geospatial data of countries. 
        ◦ Extracted Columns: 
            ▪ NAME: Country name. 
            ▪ geometry: Geospatial boundaries of the country. 
            ▪ SOV_A3: Sovereignty code.

Processed Variables
    1. full_dataset
        ◦ A merged dataset combining the world, country_of_author, and country_of_colab datasets. 
    
    2. coords
        ◦ Coordinates prepared for plotting collaboration arrows. 
        ◦ Columns: 
            ▪ lats_from, lons_from: Latitude and longitude of the source country. 
            ▪ lats_to, lons_to: Latitude and longitude of the destination country. 
            ▪ counts: Frequency of collaboration. 

## Requirements
    • Python Version: 3.12.7 or higher. 
    • Required Libraries: 
        ◦ pandas 
        ◦ geopandas 
        ◦ matplotlib 
        ◦ numpy 

## Special Notes
    1. Data Accessibility:
Ensure that the source files for country_of_author, country_of_colab, and the world shapefile are accessible via the provided URLs. If the URLs are unavailable, download the files manually and update the paths in the script.
    2. Column Renaming:
Rename columns as follows to ensure seamless merging:
        ◦ Country → NAME 
    3. Custom Datasets:
You can use your own dataset instead of the provided sources. Verify that your dataset follows a compatible structure.
    4. Geospatial Matching:
For accurate results, confirm that the countries in the datasets match those in the shapefile. If discrepancies occur, inspect and resolve them during preprocessing.
    5. Debugging Unmatched Data:
If there are missing or unmatched countries, check the logs for detailed debugging information.

## Summary
This notebook simplifies the visualization of bibliometric data by combining publication frequency and collaboration patterns into a single, clear geospatial map. It enables researchers to uncover meaningful patterns and insights efficiently while providing customization options to suit diverse research objectives.

