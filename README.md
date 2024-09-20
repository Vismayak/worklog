---
description: Daily Work Updates on what I have done
icon: display-code
---

# Visu's Worklog

## September 19
# HDC
- Running Object Detection Notebook sucessfully on NCSA GPU (Small changes such as loading data locally with curl instead of bucket download needed to be done)
- Running Detectron 2 on NCSA GPU VM
  Notes:
  - Needed to install g++ , [used](https://stackoverflow.com/a/69485927) `conda install -c conda-forge cxx-compiler`


## September 17 
## GLTG 
* Draft of Sidebar is done

## HDC
* Learning to use Ray Core and Ray Train
* Get to setting up Ray Cluster soon



## Aug 27, 2024 - Aug 28, 2024

## GLTG 
* Trends Dashboard Sidebar
  * Trends Table - The table now is available for all parameters, the only thing left is the interaction between map and table. 

* Geostreams
 * Hash and store the API keys for user. Still need to provide username
 * Debugging geostream scripts with Max


## HDC
* Screen recorded the Segment Anything extractor 

## Reading
  * Reading on Kubernetes 

## Misc
* Complete Cybersecurity work


## Aug 26, 2024

### GLTG
* Trends Dashboard Sidebar
  * Trends Table - Dynamically loads the GeoJson files, a hack I had to use was to use the fetch API to get the geojson data, the webpack config currently was loading them as URLS which was needed for the vector layer creation on the map

### Geostreams3 
  * The authentication app now has another API to generate API keys for logged in users, it was done using the secrets library of python, it is currently stored plainly in the database but will spend time to encrypt and store it if possible, the encryption key can be stored in settings

## Aug 21, 2024 - Aug 22, 2024

### HDC
* Segment Anything Extractor
  * Bug in Image annotator was caught, image coordinates were in SVG space, needed to be converted to image
  * Bug was fixed and minor changes to extractor, the segment anything extractor is working perfectly

### GLTG
* Basic layout of Trend Tables created


## Aug 20, 2024

### Geostreams3
* Since there was no radiant available, I put all my focus on Geostreams3, corrected the basic front end UI to login, signup and  get the token using React Contexts
* Taking a slight detour to see if I can use keycloak, one last time. 
* Keycloak method is bearing fruition, I am able to login and validate through Django. For the purpose of sign up, I think my plan is to use the keycloak frontend to create users. 


## Aug 15, 2024

### GLTG 
* Productive meeting with Max to discuss future steps with GLTG
* Making progress with issue [#108](https://github.com/geostreams/gltg/issues/108), this issue needs to be fixed in order to imrove efficiency and avoid rewriting code for new trend dashboard



## Aug 14, 2024

### HDC

* Segment Anything Extractor
  * Fixed bug regarding reading parameters
  * Clowder broke, needed to rebuild
  * Fixed mistake with extractor-info.json that caused extractor to run on all files
  * Clowder broke again before I can check the annotation tool

### GLTG

* Cleaned up `gltg_scripts` repo with small documentation for easier use

## Aug 13, 2024

### GLTG

* [PR](https://github.com/geostreams/gltg/pull/105) that modifies data to relfect new units for Load and conditional rendering of graph for improved UI

