
# Flight Data Processing and Analysis with Apache Spark

This project leverages Apache Spark to process and analyze flight data from JSON files. Using Jupyter Notebook, we load, clean, transform, and analyze the data to compute key performance indicators (KPIs) for flights and airports.

## Project Structure

```
├── adsb.json                # JSON file containing ADS-B flight data
├── oag.json                 # JSON file containing OAG flight data
├── Flight_Data_Analysis.ipynb # Jupyter Notebook for data processing and analysis
└── README.md                # Project documentation
```

## Datasets

- **`adsb.json`**: Contains ADS-B data with flight information like `AircraftId`, `Latitude`, `Longitude`, `Speed`, `Altitude`, etc.
- **`oag.json`**: Contains OAG data with nested fields detailing scheduled departure and arrival times, delays, and flight status.

## Requirements

- Apache Spark
- Python 3.x
- Jupyter Notebook
- JSON files (`adsb.json` and `oag.json`)

## Setup

1. **Install Apache Spark**: Follow [this guide](https://spark.apache.org/downloads.html) to set up Apache Spark.
2. **Install required Python packages**:

   ```bash
   pip install pyspark notebook
   ```

3. **Launch Jupyter Notebook**:

   ```bash
   jupyter notebook
   ```

4. **Open `Flight_Data_Analysis.ipynb`** and follow the steps inside the notebook to execute the data processing and analysis.

## Project Workflow

The notebook performs the following tasks:

1. **Data Loading**: Load `adsb.json` and `oag.json` data into Spark DataFrames.
2. **Data Cleaning**: Remove null values and ensure consistent data types across columns.
3. **Data Transformation**: Flatten nested data, convert types as necessary, and apply aggregations.
4. **Analysis**: Calculate key metrics like average speed per airport, delayed flights, and the latest flight entry per flight ID.

## Results

The notebook produces tables and charts that summarize:
- **Average Speed** per airport
- **Total Delayed Flights**, categorized into arrival and departure delays
- **Latest Flight Information** for each flight ID

## Notes

- The notebook contains code comments explaining each step in detail.
- Ensure that the JSON files (`adsb.json` and `oag.json`) are in the same directory as the notebook.
