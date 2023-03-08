# extras

##### Check the 0.33  and 0.66 quantileof the data

```
quantile(df$GRMean,0.33) #GRMean is mean column name
quantile(df$GRMean,0.66) ##GRMean is mean column name
```
##### Consider you got 33rd Quantile = 7.74 and 66th Quantile= 8.11
##### segregate sample into high, low and moderate samples
```
df$GRgroup = with(df,
					ifelse(GRMean <= 7.74, 'Low',
					ifelse(GRMean > 7.74 & GRMean < 8.11, 'Moderate',
					ifelse(GRMean >= 8.11, 'High', 'unknown'))))
```
```
table(df$GRgroup) #check the number of groups
````
