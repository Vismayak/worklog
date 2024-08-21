---
description: Daily Work Updates on what I have done
icon: display-code
---

# Visu's Worklog

## Aug 16, 2024

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

