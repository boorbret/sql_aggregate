# SQL Lesson 4
## Aggregate Functions

1. What was the hottest day? Where was that?

```
SELECT
    zip,
    date,
    MAX(maxtemperaturef) as max_temp
FROM
    weather
GROUP BY zip, date
ORDER BY max_temp DESC
```
Ideally this would skinny down the list some. But because we're showing date, there's not many repeated values for the grouping to remove is my guess. So ordering by max_temp is the simpler way to see the max temp. 

2. How many trips started at each station?

```
SELECT
    start_station,
    COUNT(*) AS trip_count
FROM
    trips
GROUP BY 1
```
