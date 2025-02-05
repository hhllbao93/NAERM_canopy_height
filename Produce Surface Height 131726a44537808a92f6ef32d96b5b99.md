# Produce Surface Height

1. Get 3DEP Lidar data (Also check Lidar Region: [https://apps.nationalmap.gov/lidar-explorer/#/](https://apps.nationalmap.gov/lidar-explorer/#/))
    1. Web: [https://apps.nationalmap.gov/downloader/](https://apps.nationalmap.gov/downloader/)
    2. Upload the polygon to clip region
    3. Select appropriate region to download laz files
    4. Check the CRS from [https://www.sciencebase.gov/catalog/item/6435e050d34ee8d4addb3320](https://www.sciencebase.gov/catalog/item/6435e050d34ee8d4addb3320) (Metadata)
    5. Search projcsn: <projcsn>NAD_1983_StatePlane_Pennsylvania_South_FIPS_3702_Feet</projcsn>

1. Process DTM in QGIS (Need to use QGIS 3.38)
    1. [https://www.youtube.com/watch?v=yJpm6sBq8Sk](https://www.youtube.com/watch?v=yJpm6sBq8Sk)
    2. Classification = 2
    3. Need to export to tif
2. Process DSM
    1. (ReturnNumber = 1) AND (Classification != 7 OR Classification != 18)
    2. Need to export to tif
3. Process CHM
    1. CHM = DSM-DTM