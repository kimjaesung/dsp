[Think Stats Chapter 6 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2007.html#toc60) (household income)

>> assuming hinc and hinc2

```
df = hinc.ReadData()
log_is = InterpolateSample(df, 6.0)
fs = np.power(10, log_is)
print('mean: ' + str(Mean(fs)))
print('median: ' + str(Median(fs)))
print('skewness: ' + str(Skewness(fs)))
print('pearsons skewness: ' + str(PearsonMedianSkewness(fs)))
print('% below mean: ' + str(cdf.Prob(Mean(fs))*100))
```

```
mean: 2929881.9121865327
median: 51226.45447894046
skewness: 17.53971121043337
pearsons skewness: 0.2285274006190828
% below mean: 100.0
```

assumed upper bound is likely higher than 1mm. could drastically increase skew (positively)

