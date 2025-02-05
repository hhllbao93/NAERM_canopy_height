# Identify trees

1. NDVI>0.3
    
    ```bash
    ("NDVI@1" > 0.1) * 1
    ```
    
2. Surface height > 5
    
    ```bash
    ("CHM@1" > 5) * 1
    ```
    
3. Merge all small rasters to a big raster tif file
4. Identify tree 
    
    ```bash
    ("Vegetation_Mask@1" = 1) AND ("Height_Mask@1" = 1)
    ```