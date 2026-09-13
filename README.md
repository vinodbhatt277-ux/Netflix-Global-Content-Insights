# Netflix Global Content Insights Dashboard

## Project Overview

This project is a Power BI dashboard built to analyze Netflix content using a Netflix titles dataset containing **8,807 records and 12 columns**.

The dashboard provides an interactive view of Netflix content across content type, year added, country, genre, duration, and rating.

## Dashboard

![Netflix Global Content Insights Dashboard](Dashboard..png)

### Key KPIs
- Total Titles
- Total Movies
- Total TV Shows
- Country Count

### Interactive Analysis
The dashboard includes:
- Titles Added by Year
- Titles Added by Genre
- Titles Added by Country
- Total Titles by Type
- Titles Added by Duration
- Titles Added by Rating

### Filters
Users can interact with the dashboard using:
- Type — Movie / TV Show
- Year Added
- Country

The filters cross-filter the dashboard visuals to support focused analysis.

## Dataset

**Source file:** `netflix_titles(3).csv`

The dataset contains:

`show_id`, `type`, `title`, `director`, `cast`, `country`, `date_added`, `release_year`, `rating`, `duration`, `listed_in`, `description`

### Data Quality

The source dataset contains missing values in several descriptive fields, including director, cast, country, date added, rating, and duration. These are retained where appropriate rather than inventing values.

The dataset was also checked for duplicate records and duplicate `show_id` values.

During Power Query ingestion, quoted line breaks in CSV records required CSV quote-aware parsing so that records were loaded correctly.

## Tools & Technologies

- Microsoft Power BI Desktop
- Power Query
- DAX
- CSV
- Kaggle Netflix titles dataset

## Power BI Concepts Demonstrated

- Data import and transformation
- Data type management
- Handling missing values
- CSV parsing and data-quality validation
- DAX measures
- KPI cards
- Slicers and interactive filtering
- Cross-filtering between visuals
- Line charts
- Bar charts
- Column charts
- Donut chart
- Map visualization
- Dashboard formatting and layout

## Business Questions

The project is aligned with the Netflix analysis objectives supplied with the project, including:

1. Count the number of Movies vs TV Shows.
2. Find the most common rating for movies and TV shows.
3. List movies released in a specific year.
4. Find the top countries with the most Netflix content.
5. Identify the longest movie.
6. Find content added in the last five years.
7. Find movies/TV shows by a specified director.
8. List TV shows with more than five seasons.
9. Count content items by genre.
10. Analyze yearly average content releases in India.
11. Identify documentary movies.
12. Find content without a director.
13. Analyze appearances by a specified actor.
14. Find actors with the highest number of appearances in Indian-produced movies.
15. Categorize content based on the presence of the keywords `kill` and `violence` in descriptions.

The current Power BI dashboard focuses on the visual analysis areas represented by its KPIs, charts, map, and slicers.

## Key Dashboard State

With no filters selected, the dashboard displays approximately:

- **9K Total Titles**
- **6K Movies**
- **3K TV Shows**
- **749 Country Count**

The dashboard was also validated using filtered scenarios, including Movie, TV Show, and TV Show + India selections.

## Project Structure

```text
Netflix Global Content Insights/
│
├── Netflix_Global_Content_Insights_Dashboard.pbix
├── netflix_titles(3).csv
├── README.md
└── dashboard-preview.png
```

## How to Use

1. Download or clone the project.
2. Open `Netflix_Global_Content_Insights_Dashboard.pbix` in Power BI Desktop.
3. If Power BI asks for the source file location, select `netflix_titles(3).csv`.
4. Use the Type, Year Added, and Country filters to explore the dashboard.

## Notes

The `country` field can contain multiple country names in a single source record. Therefore, the dashboard's **Country Count** represents distinct values/entries in the source field rather than a normalized count of individual countries.

This project is intended as a portfolio demonstration of practical Power BI data analysis and dashboard development.
