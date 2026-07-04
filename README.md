# E-Commerce Data Pipeline & Performance Optimization

## 📊 Project Overview
This project demonstrates an end-to-end data engineering and analytics pipeline built using Pandas. The pipeline processes a digital sales dataset containing 100,000 transaction logs, optimizes its memory consumption for production deployment, and extracts temporal moving-average revenue trends.

## What I did step-by-step:
* **Smart Data Loading:** Used `usecols` to load only the columns I actually needed, dropping useless system codes right from the start to save memory.
* **Data Cleaning & Splitting:** Cleared out hidden spaces, fixed the lowercase formatting, and split the messy product strings into clean 'Category' and 'Sub_Category' columns.
* **Memory Optimization:** Downcasted large 64-bit numbers to smaller types like `int8` and `float32`. I also changed repeating text columns into the `category` data type. This dropped the dataset's memory usage drastically!
* **Time-Series Analysis:** Changed the date strings into proper datetimes, set it as the index, and calculated a 3-day rolling moving average to see the revenue trends smoothly.
* **Data Visualization:** Used Matplotlib to plot a clean line graph. I overlaid a bold 3-day moving average trend line over the noisy raw daily sales to smooth out volatility and clearly show the business's revenue direction.

## Results
Even after adding new columns, the total memory size of the dataset dropped down significantly compared to the raw baseline. The final pipeline successfully calculated the moving averages while keeping the notebook incredibly fast and lightweight.
