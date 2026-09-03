# 🏠 Tokyo Airbnb Market Analytics

> 🚧 **Project Status: In Progress**
>
> This project is currently under development. Each stage of the analysis will be completed, reviewed, and committed to the repository progressively as the project evolves.

## Overview

This project analyzes Tokyo's Airbnb short-term rental market using publicly available data from Inside Airbnb.

Tokyo's short-term rental market operates under a distinctive regulatory framework, including the 2018 **Private Lodging Business Act (Minpaku)**, which introduced a framework for registered private lodging businesses, including a general annual limit of 180 operating days, alongside the **Hotels and Inns Business Act**, which applies to more traditional accommodation businesses.

This makes Tokyo a useful case study for exploring how **market structure, hosting patterns, pricing, and regulatory status** appear in platform-level data.

The analysis focuses on **market structure, neighborhood distribution, pricing, host concentration, regulatory status, availability, seasonality, and review activity** to understand how Airbnb listings vary across Tokyo.

The project follows an end-to-end data analytics workflow:

**Data Collection → Data Understanding → Data Cleaning → Exploratory Data Analysis → SQL Analysis → Power BI → Business Insights**

As the project progresses, each stage will be documented and added to the repository through individual commits, allowing the development process and analytical workflow to be tracked over time.

---

## Business Objective

The objective of this project is to understand the structure and dynamics of Tokyo's Airbnb market and identify patterns that may be relevant to hosts, hospitality businesses, market analysts, and other stakeholders.

### Main Business Question

> **Is Tokyo's Airbnb market dominated by casual home-sharing or by professional, multi-listing operators — and how does this vary across the city?**

---

## Business Questions

The analysis is structured around the following questions:

### Market Overview

1. **How large is Tokyo's Airbnb market?**

### Pricing & Neighborhoods

2. **Which neighborhoods have the highest and lowest median prices?**
3. **What characteristics are associated with higher listing prices?**
4. **How are listings distributed across room types and neighborhoods?**

### Host Structure & Market Concentration

5. **What percentage of listings are operated by multi-listing hosts?**
6. **How concentrated is Tokyo's Airbnb market among the largest hosts?**
7. **Which neighborhoods have the highest concentration of multi-listing hosts?**

### Regulatory Status

8. **What proportion of Tokyo listings operate under Hotels and Inns Business Act licenses versus Minpaku registration, and how does this vary by neighborhood?**

### Availability & Seasonality

9. **How do price and availability vary throughout the year?**
10. **How does seasonality differ across neighborhoods and room types?**

### Market Activity

11. **How has Airbnb review activity evolved over time?**

---

## Data Source

The dataset was obtained from **Inside Airbnb**, an independent project that provides publicly available Airbnb data for cities around the world.

The Tokyo dataset used in this project was published on **June 30, 2026** and includes detailed listings, calendar, reviews, and neighborhood data.

**Source:** [Inside Airbnb — Tokyo Data](https://insideairbnb.com/get-the-data/)

### Datasets

The analysis uses the following datasets:

* `listings.csv` — Detailed information about Airbnb listings and hosts
* `calendar.csv` — Daily availability and pricing information
* `reviews.csv` — Historical review activity by listing
* `neighbourhoods.csv` — Tokyo neighborhood reference data

---

## Data Limitations

Several limitations should be considered when interpreting the results.

* The dataset represents a **snapshot of listings available on the Airbnb platform at a specific point in time**.
* Airbnb's calendar does not distinguish between **booked nights and nights blocked by hosts**, so availability should not be interpreted as direct occupancy.
* Listing locations are anonymized by Airbnb and may differ from the actual property location by up to approximately 150 meters.
* Neighborhood assignments are derived from geographic coordinates rather than relying directly on Airbnb's neighborhood labels.
* Review activity is used as an indicator of market activity, but reviews do not represent all bookings.
* The analysis does not estimate actual listing revenue because the dataset does not provide observed booking revenue.
* License field values may be incomplete, missing, or inconsistently formatted. Regulatory status findings should therefore be interpreted as **indicative rather than exhaustive**.

---

## Tools & Technologies

* **Python**

  * Pandas
  * NumPy
  * Matplotlib
  * Seaborn

* **SQL**

  * MySQL
  * DBeaver

* **Data Visualization**

  * Microsoft Power BI

* **Version Control**

  * Git
  * GitHub

---

## Project Structure

```text
tokyo-airbnb-analytics/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── notebooks/
│   ├── 01_data_understanding.ipynb
│   ├── 02_data_cleaning.ipynb
│   └── 03_exploratory_analysis.ipynb
│
├── sql/
│   ├── 01_schema.sql
│   └── 02_business_analysis.sql
│
├── dashboard/
│   └── Tokyo_Airbnb_Analytics.pbix
│
├── images/
│
├── README.md
├── README.PT-BR.md
├── README.JP.md
└── requirements.txt
```

> **Note:** The repository structure will be updated as new stages of the project are completed.

---

## Analytical Workflow

### 1. Data Understanding

The first stage evaluates the structure and quality of the source datasets, including:

* Dataset dimensions
* Data types
* Missing values
* Duplicate records
* Unique values
* Distribution of key variables
* Potential data quality and encoding issues

### 2. Data Cleaning

The raw datasets are processed using Python.

The cleaning process includes:

* Handling missing values
* Standardizing data types
* Parsing dates
* Removing duplicates where appropriate
* Investigating inconsistent values
* Investigating character encoding issues in Japanese-language fields, particularly the `license` column
* Standardizing and classifying regulatory information where supported by the source data
* Creating analytical variables
* Preparing datasets for SQL analysis

### 3. Exploratory Data Analysis

Exploratory analysis will be conducted to identify patterns, distributions, relationships, and potential anomalies in the data.

The analysis will focus on areas such as:

* Listing distribution
* Pricing
* Neighborhood patterns
* Room types
* Host activity
* Market concentration
* Availability
* Seasonality
* Review activity

### 4. SQL Analysis

The processed data is loaded into MySQL and analyzed using SQL.

Business questions are translated into queries using:

* Aggregations
* JOINs
* CTEs
* Window functions
* Ranking
* Percentiles
* Time-based analysis

### 5. Power BI Dashboard

The analytical results are presented through an interactive Power BI dashboard focused on:

* Market overview
* Neighborhood and room-type distribution
* Pricing
* Host concentration
* Regulatory status
* Availability
* Seasonality
* Review activity

### 6. Business Insights

The final stage translates the analytical findings into business-oriented insights.

Rather than simply reporting descriptive statistics, the project will focus on identifying **meaningful patterns, differences, and potential implications for the Tokyo Airbnb market**.

---

## How to Reproduce

> **Project status:** Reproduction instructions will be finalized as the analytical workflow is completed.

Once the project is complete:

1. Download the raw data from Inside Airbnb (see **Data Source**).
2. Place the downloaded files in `data/raw/`.
3. Install the required Python dependencies:

```bash
pip install -r requirements.txt
```

4. Run the notebooks in `notebooks/` in numerical order.
5. Load the processed data into MySQL using `sql/01_schema.sql`.
6. Run the business analysis queries in `sql/02_business_analysis.sql`.
7. Open `dashboard/Tokyo_Airbnb_Analytics.pbix` in Power BI.

---

## Dashboard

The Power BI dashboard will be added to the repository after the visualization stage is completed.

### Market Overview

*Dashboard screenshot to be added.*

### Pricing & Market Structure

*Dashboard screenshot to be added.*

### Seasonality & Market Activity

*Dashboard screenshot to be added.*

---

## Key Findings

> **This section will be completed after the analysis is finalized.**

The final findings will focus on the most relevant business insights discovered during the analysis, rather than simply reporting descriptive statistics.

Potential areas include:

* Tokyo's overall Airbnb market structure
* Neighborhood price differences
* Factors associated with higher listing prices
* Host concentration
* Differences between single- and multi-listing hosts
* Regulatory status across neighborhoods
* Seasonal price and availability patterns
* Differences across room types and neighborhoods
* Long-term trends in review activity

---

## Conclusion

This project aims to provide a data-driven view of Tokyo's Airbnb market by combining **Python, SQL, and Power BI** to move from raw marketplace data to actionable business insights.

The analysis emphasizes not only what is happening in the market, but also **where the strongest patterns occur and what they may mean from a business and regulatory perspective**.

The repository will be progressively updated as each stage of the project is completed, providing a transparent view of the analytical process from raw data to final insights.

---

## License & Data Attribution

This project is for educational and portfolio purposes.

**Data source:** Inside Airbnb

The source data is not included in this repository. To reproduce the analysis, please obtain the datasets directly from the official Inside Airbnb data portal and review the applicable data policies.
