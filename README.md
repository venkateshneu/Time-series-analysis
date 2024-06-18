# Time-series-analysis
Loading and Initial Exploration:

The data is loaded from a CSV file and basic information like data types and null values are checked.
Date column is converted to datetime format and set as index.
Time Series Operations:

Added new columns for month, day name, and quarter using index.month_name(), index.day_name(), and index.quarter.
Filtered data for specific dates, and plotted closing prices over the years.
Visualization and Analysis:

Plotted closing prices over time using plot() and subsets of multiple columns using plot(subplots=True, layout=(2,2), figsize=(20,10), sharex=False).
Grouped data by month and plotted the average closing prices using groupby("month")["Close"].mean().plot(kind="bar").
Resampling and Interpolation:

Downsampled the data to weekly frequency using resample("W").mean() and interpolated the data for every 6 hours using resample("6h").interpolate(method="linear").
Calculated rolling average and shift in opening prices using rolling(window=3).mean() and shift(1).
Future and Index:

Made the various groupby, table