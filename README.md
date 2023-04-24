# Urban CIs Resilience to Flood Hazards
This repository contains code, data, and documentation for analysing and visualising the resilience to flood hazards on urban Critical Infrastructure (CI) nodes in the Bangkok Metropolitan Region (BMR). This is an analysis part of my master's thesis titled "Assessing Urban Critical Infrastructure Resilience to Flood Hazards for Bangkok Metropolitan Region, Thailand". This thesis is a partial fulfillment of the requirements for the degree of 
Master of Science in Disaster Preparedness, Mitigation, and Management, Asian Institute of Technology 


## Project Overview ##

The goal of this project is to analyse and visualise the effects of flooding on urban CI nodes in the BMR, focusing on how urban CIs are impacted. The analysis takes into account the spatial and network, interdependencies, and flood extent layers to understand the resilience of urban CI nodes during flood events.

## Dataset ##

The data for this project includes:
* Point layers representing urban CI nodes (Rail Station, Electric Power Supply, Water Supply, Healthcare Service, Educational Service, Civic Protection, Sanitation)
* Line layer representing the road network (RD)
* Flood extent layers for 2011, 2030, and 2050
* Population grid layer (1km resolution)
* Interdependencies Topology of Urban CIs

## Analysis Workflow ##

**Spatial Analysis**
* Load and add layers
* Calculate service areas using Kernel Density
* Calculate shortest paths and accessibility between population centroids and urban CI nodes
* Modify the road network by removing edges located in flood extent layers
* Recalculate shortest paths and accessibility using the modified road network
* Export the shortest path results to CSV files
* Visualise the accessibility of urban CI nodes as Iso-Areas

**Network Analysis**
* Install and import required libraries
* Load and add layers that containing urban CI nodes and their dependencies
* Create a NetworkX directed graph (G) from the CSV dat
* Compute the degree of each node and visualize the graph in Pyviz (using the HoloViews library)
* Define a function compute_impacts to analyze the primary, secondary, and tertiary impacts based on flood data
* Define a function calculate_resilience_performance to calculate the resilience performance for each scenario
* Plot a line graph showing resilience performance degradation during flood events for different scenarios and create a table summarising the impacts

## Visualisation ##
The project uses QGIS and Python libraries for visualising the urban CI nodes, road network, service areas, and accessibility Iso-Areas. The impact of floods on urban CI nodes is shown in maps, graphs, and tables.

## Results ##

The analysis results include:

* Distribution of urban CI nodes by service provision radius
* Shortest paths and accessibility between population centroids and urban CI nodes
* Impact of floods on urban CI nodes in terms of Provision, Accessibility, and Reachablity
* Visualisations of service areas, accessibility Iso-Areas, and impacted nodes
* Urban CI inventory and their interdependencies map
* Resilience performance degradation during flood events for different scenarios
