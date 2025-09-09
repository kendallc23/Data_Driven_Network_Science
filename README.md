# A Comparison of Distance Metrics: Exploring Temporal Music Collaboration Networks
## Overview
This project analyzes collaboration patterns in global popular music using network science methods. Using data from Spotify's Weekly Top Songs Global chart from 2017 (adapted from Oliveira et al. 2020), I examine how musical collaboration networks evolve over time by comparing three distance metrics: Jaccard distance, polynomial dissimilarity, and eigenvector centrality-based distance.

## Project Structure
- Final_code.ipynb: Main analysis notebook, including data processing, network construction, visualization, and distance metrics.
  - **Note:** I initially forgot to set up a random seed. This means that the exact visual configurations of the LCC graphs (e.g. graph shapes, or colors assigned to nodes) may look different from my figures, if you run the notebook. However, the essential characteristics of the graphs and the distance metric computations will be the same. 
- networks_data folder: 
  - spotify_artists.csv: Artist metadata (name, popularity, genres).
  - global_2017.csv: Collaboration data for charting songs in 2017 (collaborating artists: artist_1 and artist_2, number of collaborations: count, and song_ids).
- Figures:Images folder: Contains generated figures for analysis.
- Networks_Summative.pdf: Report outlining context, project methods and findings in detail
- README.md: You're here!

## Research Questions
How did the number of artist collaborations on Spotify’s Weekly Top Songs Global chart change throughout 2017? And were there changes in the specific (types/genres of) artists that tended to collaborate more often?

## Key Concepts
- **Temporal Networks:** Allow for the study of changing network structures over time. Temporal networks may be represented as continuous timelines reflecting the specific periods in which two nodes are connected (time-ordered graphs) or as a series of graphs, illustrating network structure at different points in time (time-aggregated graphs).
- **Network Distance Metrics:** Operationalize dissimilarities between graphical representations of the same system, often used to measure change over time. The selection of distance metrics is generally based on the scale of the problem/research question.
    - **Structural Metrics:**  Focus on the local structure of the graph surrounding each node and are often used to explore instances in which small changes can lead to larger consequences for the network system.
    - **Spectral Metrics:** Reflect global changes in the organization of a graph, without focus on specific node identities, interactions, or associations.
    - **Mesoscale Metrics:** Examine both local and global changes in a network. 
   
## Data and Methodology
- The analysis uses data originally collected by Oliveira et al. for their paper "Detecting Collaboration Profiles in Success-Based Music Genre Networks" presented at ISMIR 2020. The dataset includes:
  - 366 unique artists
  - 44 distinct music genres
  - 52 weeks of Spotify Chart data from 2017, including songs featuring artist collaborations
- The notebook contains code for cleaning the data and constructing graphs. I conduct exploratory analysis, focusing on the largest connected components (LCCs) of three graphs at the 1, 25, and 50 week marks.
- I then examine changes in the system using three distance metrics:
  - **Jaccard Distance:** A structural metric that measures the amount of edge rewiring (node-level connectivity changes) in a network over time, with respect to a starting graph.
  - **Polynomial Dissimilarity:** This metric reflects how local changes have impact different areas of the network to varying extents.
  - **Eigenvector Centrality-Based Distance:** The eigenvector centrality of a given node assumes that its centrality or prestige in the network is proportional to the sum of the centrality of its neighbors. This metric captures aggregate changes in the eigen vector centrality of the nodes in the system over time.

##  Main Findings
- The largest connected component of collaborating artists grew from 81 nodes in January to 101 nodes by December 2017, suggesting increasing integration of niche artists into mainstream collaborations.
- Artists in pop-rap and Latin music genres showed higher-than-average collaboration rates throughout the year.
- Major shifts in network structure were observed after week 38 (late September).



