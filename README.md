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
