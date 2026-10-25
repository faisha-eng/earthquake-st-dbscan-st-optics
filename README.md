# Earthquake Clustering in Indonesia: ST-DBSCAN vs ST-OPTICS

An individual project for the Big Data course at Universitas Tarumanagara. It compares two clustering algorithms, ST-DBSCAN and ST-OPTICS, on earthquake data from BMKG (2021-2023) to find earthquake-prone zones in Indonesia.

## Data
31,615 earthquake events from January 2021 to December 2023. Source: [sumber]

## Method
- Checked the data for missing values and duplicates, and converted time into days.
- Tested 27 parameter combinations for each algorithm on a random sample of 2,000 records, and picked the best one by Silhouette Score.
- Compared the two algorithms with Silhouette Score and Davies-Bouldin Index, and plotted the results on maps and charts.

## Results
ST-DBSCAN did better than ST-OPTICS.

ST-DBSCAN (eps1=0.5, eps2=7, min_samples=5) found 7 clusters, with a Silhouette Score of 0.990 and a Davies-Bouldin Index of 0.013.

ST-OPTICS (xi=0.5, eps2=7, min_samples=5) found 11 clusters, with a Silhouette Score of 0.943 and a Davies-Bouldin Index of 0.076.

Note: the scores only count the points that were put into clusters. Most points (98% for ST-DBSCAN, 96% for ST-OPTICS) were left out as noise.

## Tech
Python, Google Colab, pandas, scikit-learn, st-dbscan, st-optics, geopandas, matplotlib

## How to run
1. Upload `gempa_2021_2023.csv` to your Google Drive (the main "My Drive" folder).
2. Open `earthquake_clustering.ipynb` in Google Colab.
3. Run all cells.

## Author
Faisha Devian Az-Zam Zamiah, Information Systems, Universitas Tarumanagara.
