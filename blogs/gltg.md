---
description: Personal notes for my work at GLTG
icon: display-code
hidden: true
---

## Meeting with Laura and Jong-  October 11, 2021

Questions:

Replacing the dashboard here with the thematic maps means we have to change the dashboard also? Else users will be confused.

- Temporarily remove the conservation practices dashboard
- Lisa suggested remove news section, Jong suggested a whats new section
- They want to change intro backgroun to banner, text will go below this banner


- November 20 to deploy GLTG homepage changes now


## Breaking down the new wirefreames for GLTG

My initial thoughts are these designs are clunky and feel like a lot of work for a placeholder but onwards we go. Here are a breakdown of the tasks that will be needed to implement the new wireframes.

- Changing the contact us, it should direct to Laura
-  We will need to create a prop compoent that explains the different dashboards, it would be two columns one with the photo and the other for a dynamic description with tabs for different topics("I envision the user clicks on the dashboards and get taken to those dashboards separately, the same way the navigation currently functions on GLTG. The dashboards on the homepage are not interactive, and the actual dashboards will have more information available in the narrative sections/tabs. Clicking the tab would replace the current narrative box with whatever narrative corresponds with the selected tab.")
- Changing copyright year


## Creating the shapefile for watersheds

The process for generating new watersheds for the GLTG dashboard has been simplified thanks to the scripts in the repo `gltg_scripts`. There is no need to use QGIS to generate the shapefile.

Here is the process given the format of the data provided remains the same. 

- Step 1 - Download the folder of shapefiles from google drive. Then run the script `watershed_creator.py`, the script use geopandas to go through the folder and create a new geojson with all the watersheds. 

- Step 2 - Suppose you have to combine multiple watershed files, use the script `watershed_combiner.py`. This script will combine all the watersheds into one file.

- Step 3 - Run the script `watershed_corrector.py`. This script will need the station geojsons in a single directory. The script will use the station geojsons to update the properties of the watershed geojson.
