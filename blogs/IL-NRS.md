---
description: Personal notes for my work at Illinois NRS Dashboard
icon: display-code
hidden: true
---


[Google Drive Link](https://drive.google.com/drive/u/0/folders/1bvuE5uNpSAmTLUHO_5O-dQbAwHixYaDl)


# Illinois NRS Dashboard

## Meeting with Trevor (October 4th 2024)
### Overview
- The project aims to visualize annual average loads for point sources in three categories: Major Municipal, Industrial, and Minor. 
- The focus is initially on aggregated data, with a goal to display individual point sources later.
- A basic site is expected to be ready by early 2025 for presentation to the committee, with potential interactive features added based on their feedback.

### Data
- **Data Availability**:
  - Data from point sources is available for the baseline year 2011, then 2017-2022.
  - Major Municipal data includes latitude and longitude, while data for minor facilities is still being finalized.
  - NonPOTW (non-publicly owned treatment works) data is relevant, with power plants excluded as they source water from nutrient-rich lakes.

- **Key Datasets**:
  - **MajorMunicipalTotalLoads2011-2022Huc8Huc12**: 
    - Focus on tabs for 2011-2022 TN (Total Nitrogen) and TP (Total Phosphorus).
    - Some facilities have closed, leading to zero load values, but historical data remains.
  
  - **Final 2022 Minor Municipal+Lagoons_Phosphorus Loads_dashboard**:
    - Contains data for minor facilities, with monthly load values (highlighted in yellow) that need to be aggregated to annual data.
    - Minor facilities typically show stable load patterns.

### Data Manipulation
- The data from the spreadsheets will be used to create spatial dashboards, focusing on visualizing annual average loads.
- Initial pages will be static, but there are plans to integrate interactive dashboards later. The recommendation is to consider using an interactive chart library from the outset.

### Current Steps
- Review and refine the mockup document; Trevor finds it a bit wordy, but Laura has provided useful wireframes that offer clarity.
- Await the finalization of wireframes to explore layout design.
- Explore dynamic infographic libraics
- Continue to get more comfortable with Gatsby for front-end development.


### Goals 
- Prepare to present chart prototypes at the next meeting.



## Point Source Vector Report Notes

**Introduction**

- A point source is any site of discharge into a waterway, such as a pipe. Point sources are often associated with publicly owned treatment works and industrial wastewater treatment plants.
- This sector is implementing strategies to reduce the nutrient loads.
- Phophorus loads are not as well handled as nitrate-nitrogen loads.
- The data is compiled by the Illinois Association of Wastewater Agencies. National Pollutant DischargeElimination System, NPDES, permit holders are also required to submit monthly discharge data to the Illinois Environmental Protection Agency, Illinois EPA.
-  Great improvements aready done, the goal was 25% reduction by 2025, and the sector has already achieved340% reduction in 2022

**Resource Measures**
- Only 11 out of 211 municpal facilities submitted resource and outreach data, therefore figures significantly underestimate staff, financial, and outreach measure
- The investment in operations, maintenace, and staff has increased

**Outreach measures** - Continues a lot with even online events during covid

**Progress Across Illinois** - Reducing nutrient losses from the point source sector requires two key strategies: upgrading and optimizing the systems used by wastewater treatment facilities, and utilizing a watershed approach


**TP Reductions**
-  Overestimation of the 2011 baseline loads for some facilities may also contribute to overall total phosphorus load reductions.
- 10 major municipal facilities contribute to 62% of the total phosphorus load
- Many of these facilities will remain in the top 10 simply due to the amount of treated wastewater that they discharge on an annual basis.


Nutrient Assessment Reduction Plans help identify phosphorus input reductions by point source discharges, non-point source discharges, and other measures that major municipal facilities can implement alongside a watershed workgroup. This helps meet watershed-wide criteria for dissolved oxygen, offensive aquatic algae, and offensive aquatic plants.

**Total Nitrogen Load Reductions**

- Illinois EPA incentivized point sources to adopt biological phosphorus removal. This is because the low dissolved-oxygen environment used with biological phosphorus removal would have the additional advantage of reducing a significant fraction of the nitrogen as well.

- The 2021 statewide total nitrogen load from all point sources was estimated to be 76.6 million pounds, which is a 12.2% decrease from the 2011 baseline load (Table 5.7). The 2022 total nitrogen load from all point sources was estimated to be 77.2 million pounds, which is an 11.6% decrease from the 2011 baseline load

**Future Stategic Actions**

Most municipal facilities required to develop a NARP. s wastewater facilities continue to invest in nutrient removal technology, total phosphorus loads — and in some cases, total nitrogen loads — are expected to continue to decrease.

# First Project Meeting

## Frontend
- I pushed for a couple of wireframes so we can get started with the layout of the dashboard and compare different navigation options.
- The design files might have some useful styling information that can be used for the dashboard.
- The project so far has 4 dashboards, but it is a tentative number and can be changed.

## Data
- A lot of the data in the report is statewide, but the dashboard might require us to focus by county, practices, and HUC.
- There are a number of spreadsheets from different sources which should be normalized to a single database, and this format is already being worked on by Joan.

## Data Manipulation
- A number of scripts would be required for conversions such as latitude/longitude to HUC, etc.

## Backend
- There are a lot of similarities to the old Green Infrastructure project, so going through the codebase could be helpful.

## Database
- Normalizing the spreadsheets to a single database format is in progress, led by Joan.

## Misc
- Joan showed us a timeline of the project and the different phases that are planned.
- Going to have a follow-up huddle with Laura to clarify some of the points and get started on the project.
