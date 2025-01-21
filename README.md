# A Comparison of Distance Metrics: Exploring Temporal Music Collaboration Networks

## Overview
This paper analyzes collaboration patterns in global popular music using network science methods. Using data from Spotify's Weekly Top Songs Global chart during 2017, the study examines how musical collaboration networks evolve over time by comparing three distance metrics: Jaccard distance, polynomial dissimilarity, and eigenvector centrality-based distance.

## Methodology
The study considers three complementary approaches to measure network evolution:
- **Jaccard Distance**: Measures structural changes at the individual edge level
- **Polynomial Dissimilarity**: Captures mesoscale network changes while accounting for edge weights
- **Eigenvector Centrality-based Distance**: Analyzes changes in artist influence and prominence

## Data
The analysis uses data originally collected by Oliveira et al. for their paper "Detecting Collaboration Profiles in Success-Based Music Genre Networks" presented at ISMIR 2020. The dataset includes:
- 366 unique artists
- 44 distinct music genres
- 50 weeks of collaboration data from 2017
- Weekly snapshots of Spotify's global top songs chart

## Key Findings
- The largest connected component of collaborating artists grew from 81 nodes in January to 101 nodes by December 2017
- Artists in pop-rap and Latin music genres showed higher-than-average collaboration rates
- Analysis suggests increasing integration of niche artists into mainstream collaborations, particularly from genres like reggaeton, K-pop, and Brazilian funk
- Major shifts in network structure were observed after week 38 (late September)

