# Probability and Statistics for Data Science

Coursework from my Probability and Statistics courses: one simulation project on random networks, and lab notebooks on time series and data handling in Python.

## Project: percolation on Boolean networks — `PERCOLATION_ON_BOOLEAN_NETWORKS.ipynb`

**Question:** in a random network, how does the size of the largest connected cluster change as the network gets denser?

**Method**
- Scattered points at random (a Poisson process with density λ) on a large square, and drew a disc of radius 1 around each point. Two points are connected when their discs overlap.
- Built the network with a KD-tree (SciPy) and NetworkX, and found the largest cluster with depth-first search.
- Ran 30 simulations on a 100 × 100 square for each of 25 values of λ between 0.1 and 1, and averaged the size of the largest cluster.
- The assignment text (Probability for Data Science, MSc in Data Science) is in `Project_P_DS_Boolean_RG.pdf`.

**Result:** below the critical density λc ≈ 4.512 / 4π the network breaks into many small, separate clusters. Above it, one large cluster suddenly appears and connects most of the points. The simulations show this sharp change (the percolation threshold) clearly.

## Lab notebooks

| Notebook | Topics |
|---|---|
| `Statistical_Models_For_Data_Science_ToDo.ipynb` | NumPy and pandas refresher: arrays, reshaping, structured data, DataFrames, merging |
| `Lesson2_21_11_2023_ToDo.ipynb` | Dates and times in pandas, reading tabular data, selection, sorting, pivot tables, resampling; exercises on temperature, earthquake and global temperature data |
| `Lesson3_27_11_2023_ToDo.ipynb` | Time series charts: heatmaps, box and violin plots, lag plots, autocorrelation, white noise; exercises on CO₂, brain activity, Google stock prices and energy use |

My weekly order forecasting project (ARIMA) is in my [Business Intelligence repository](https://github.com/Amirhatamian/Bussines-Intelligence-Project). The data files for the labs are in `csv-part2.zip` and `csv-part3.zip`.

## How to run

```bash
git clone https://github.com/Amirhatamian/Probability-and-Statistics-Analysis.git
cd Probability-and-Statistics-Analysis
unzip csv-part2.zip && unzip csv-part3.zip
pip install numpy pandas matplotlib seaborn scipy networkx statsmodels jupyter
jupyter notebook
```

## Tools

Python, NumPy, pandas, SciPy, NetworkX, Matplotlib, Seaborn
