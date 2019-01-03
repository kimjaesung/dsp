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

assumed upper bound is likely higher than 1mm. could drastically increase skew (positively)

