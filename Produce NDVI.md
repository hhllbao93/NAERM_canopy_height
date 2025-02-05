# Produce NDVI

1. Download NAIP data 
    1. Check data from [https://naip-usdaonline.hub.arcgis.com/](https://naip-usdaonline.hub.arcgis.com/)
    2. Download data from [https://earthexplorer.usgs.gov/](https://earthexplorer.usgs.gov/),  choose NAIP, region (close to Penn State)
2. Calculate NDVI
    1. **Verify the Bands**:
        - **Band 1**: Red
        - **Band 2**: Green
        - **Band 3**: Blue
        - **Band 4**: Near-Infrared (NIR)
    2. **Enter the NDVI Expression**:
        - In the **Raster calculator expression** box, input the NDVI formula:
            
            ```less
            ([your_image]@4 - [your_image]@1) / ([your_image]@4 + [your_image]@1)
            ```
