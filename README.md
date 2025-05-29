SQL Analysis: Billboard Top 100 Year-End Charts

This repository contains a collection of SQL queries designed to explore and analyze historical Billboard Top 100 Year-End chart data. The dataset spans multiple decades and offers insights into music trends, artist performance, and ranking patterns.

 Dataset Overview

Table: `tutorial.billboard_top_100_year_end`

Key Indicators

* `year`: The chart year
* `year_rank`: Position of the song in the year-end chart (1–100)
* `song_name`: Title of the song
* `group_name`: Primary performer or group
* `artist`: Featured or contributing artist(s)

Areas of Focus

The queries in this repository address:

* Ranking trends across different years and decades
* Filtering songs or artists by name or pattern
* Identifying top-performing songs and artists
* Comparing results across specific timeframes
* Excluding or isolating results based on custom conditions
* Ordering and slicing data for clearer presentation

Sample of Queries

-- Songs by Macklemore or Timberlake in 2013
SELECT *
FROM tutorial.billboard_top_100_year_end
WHERE year = 2013
  AND (group_name ILIKE '%macklemore%' OR group_name ILIKE '%timberlake%');


-- Songs ranked in the Top 3, ordered by year and rank
SELECT *
FROM tutorial.billboard_top_100_year_end
WHERE year_rank <= 3
ORDER BY year DESC, year_rank;

-- Songs containing 'California' in the title from the 70s and 90s
SELECT *
FROM tutorial.billboard_top_100_year_end
WHERE (year BETWEEN 1970 AND 1979 OR year BETWEEN 1990 AND 1999)
  AND song_name ILIKE '%california%';


Objective

This project serves as a structured exercise in writing and optimizing SQL queries using real-world data. It demonstrates how chart-based cultural datasets can be queried to uncover patterns and support exploratory analysis.




