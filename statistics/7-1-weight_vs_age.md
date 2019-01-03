[Think Stats Chapter 7 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2008.html#toc70) (weight vs. age)

>> 
```
live = live.dropna(subset=['agepreg','totalwgt_lb'])
ages = live['agepreg']
wgts = live['totalwgt_lb']
print('correlation: ', ages.corr(wgts))
print('spearman corr: ', ages.corr(wgts, method='spearman'))
```

```
correlation:  0.0688339703541091
spearman corr:  0.09461004109658226
```

low level of correlation implies minimal or weak relationship
