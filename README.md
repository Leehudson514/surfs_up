# surfs_up
## Overview
* The purpose of this analysis was to analyze trends in weather in Hawaii to determine if starting a surf/ice cream shop in Hawaii, would be a good investment.

## Results
* The analysis shows that **weather temperature is consistent year round** with temperature being slightly warmer during the summer months.
* The average temperature from June was 74C while december was 71C.
* The minimum temperature for december was 56C while the max was 83C

* **June Temperature:**

![goals](https://github.com/Leehudson514/surfs_up/blob/main/images/june_describe.png)


* **December Temperature:**

![goals](https://github.com/Leehudson514/surfs_up/blob/main/images/dec_describe.png)


## Summary
* Having consistent warm weather will be key for the success of the shop, surfers and ice cream consumers will be able to benefit from the store year round.
* Additional quereies will be needed to be able to fully conclude if this will be a sound investment or not. Gathering information on the the number of stations and the accuracy of the data itself will be important. Additionally, measurements of percipitation to determine the average amount of rainfall there is.
* **Example of Additional queries:**
* Determine total number of stations to asses data relevance and accuracy: (9)
```
session.query(func.count(Station.station)).all()
```
* Determine annual percipitation:
```
prev_year = dt.date(2017, 8, 23) - dt.timedelta(days=365)
results = session.query(Measurement.date, Measurement.prcp).filter(Measurement.date >= prev_year).all()
df_results = pd.DataFrame(results, columns=['date','precipitation'])
```

![goals](https://github.com/Leehudson514/surfs_up/blob/main/images/precipation_results.png)
