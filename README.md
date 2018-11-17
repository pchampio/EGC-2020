# EGC_2020
EGC 2020 Challenge: 20 years of history for which future?

The goal of this challenge is to take stock at the evolution of the EGC community over the past 20
years and try to predict the future. The principle is to apply techniques of knowledge discovery and
data mining to explain the structure and evolution.

## Dataset

The data set consists of 1200 titles and abstracts from the articles published at the EGC conference between 2004 and 2018.  
Fields:
  - years
  - title
  - abstract
  - authors


## Pipeline

- filter_extreme
- tf-idf
- LDA (Coherence Score)
- K-Means (Silhouette scores)

## Cluster (Topics) evolution / Time

<p align="center">
  <a href="#">
    <img alt="ScreenShot" src="https://raw.githubusercontent.com/Drakirus/EGC_2020/master/plots/distribution.png">
  </a>
</p>

Our system deducted a sharp increase in articles related to the social network analysis over the past years 20 (Label 1).  
On the other hand, rule-based algorithms seem to have declined drastically (Label 6).

## Evaluation (Hyper-parameters defined in the [Jupiter-notebook](./EGC.ipynb))
The pipeline used in this project doesn't seem to find a lot of structure for one cluster (Label 9), sadly this cluster represents ~30% of our training data (Silhouette plot below).
<details>
<summary>Silhouette plot for 10 clusters</summary>
<p align="center">
  <a href="#">
    <img alt="ScreenShot" src="https://raw.githubusercontent.com/Drakirus/EGC_2020/master/plots/silhouette.png">
  </a>
</p>
</details>

#### There is still room for improvement. 
