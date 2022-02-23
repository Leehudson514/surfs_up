# surfs_up
## Overview
* starting a surf/ice cream shop in hawii , looking for investors but they require more information on the weather trends to determine if it will be a good investment or not.

## Results

## Summary
* Additonal queries:
* Determine total number of stations to asses data relevance and accuracy:
```
session.query(func.count(Station.station)).all()
```
* Determine annual percipitation:
```
prev_year = dt.date(2017, 8, 23) - dt.timedelta(days=365)
results = session.query(Measurement.date, Measurement.prcp).filter(Measurement.date >= prev_year).all()
df_results = pd.DataFrame(results, columns=['date','precipitation'])
```
