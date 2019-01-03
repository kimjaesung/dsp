[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

>>  
```
import scipy.stats
hd = scipy.stats.norm(loc=178, scale=7.7)
print(100*(str(hd.cdf(185.42) - hd.cdf(177.8))))
```

'34.274683763147365'


