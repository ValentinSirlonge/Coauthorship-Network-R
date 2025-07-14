# Gender Dynamics in Scientific Co-authorship Networks

## Objective
This project investigates the collaboration patterns of marine science researchers based in California (USA), with a specific focus on gender-related structural differences in co-authorship networks.  
The main research question is:  
**How do gender dynamics influence the structure of academic co-authorship networks in California?**


## Methodology
- **Data**: Extracted from Web of Science – journal articles (“J”, containing “Article”) published between 2014 and 2018 in marine sciences.
- **Cleaning**: Standardized journal names, parsed names and affiliations, extracted countries and organization types (University, Research, Other), and predicted gender using the `gender` package in R.
- **Unique Author ID**: Combined last name, first name, country, and organization type to create unique identifiers and avoid duplicates.
- **Network Construction**: Edges represent co-authorship links from the same publication (same DOI). The network was filtered to include only authors located in California with identified gender (male or female).

## Network Analysis
Node-level centrality metrics computed:
- **Degree centrality** – direct collaborations
- **Betweenness centrality** – influence over indirect paths
- **Closeness centrality** – proximity to others
- **Eigenvector centrality** – influence via well-connected peers

Global metrics:
- **Network density**
- **Number of connected components**

## Visualizations

- **Static graph** (via `ggraph`) with gender-based coloring and labels for the top 10 authors by degree.
- **Interactive graph** (via `networkD3`) for detailed network exploration and gender grouping.

## Key Findings

- Male authors tend to occupy more central positions within the network.
- Female authors are more often located at the periphery or within tight, dense subgroups.
- Examples of **brokers** (e.g., McWilliams, Howard) and **hubs** (e.g., Stegen, Li) were identified.
