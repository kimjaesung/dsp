[Think Stats Chapter 9 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2010.html#toc90) (resampling)

>> REPLACE THIS TEXT WITH YOUR RESPONSE
```
def stats9_1(live, iters):
    n = len(live)
    first = live[live.birthord == 1]
    other = live[live.birthord != 1]
    
    data = first['prglngth'].values, other['prglngth'].values
    pval1 = DiffMeansPermute(data).PValue(iters)
    pval4 = PregLengthTest(data).PValue(iters)
    
    data = first['prglngth'].dropna().values, other['prglngth'].dropna().values
    pval2 = DiffMeansPermute(data).PValue(iters)
    
    live2 = live.dropna(subset=['agepreg', 'totalwgt_lb'])
    data = live2['agepreg'].values, live2['totalwgt_lb'].values
    pval3 = CorrelationPermute(data).PValue(iters)
    
    print('%d\t%0.2f\t%0.2f\t%0.2f\t%0.2f' % (n, pval1, pval2, pval3, pval4))

n = len(live)
for _ in range(7):
    sample = thinkstats2.SampleRows(live, n)
    stats9_1(sample, 1000)
    n //= 2
```

```
9148	0.17	0.17	0.00	0.00
4574	0.13	0.13	0.00	0.00
2287	0.12	0.12	0.00	0.00
1143	0.90	0.92	0.00	0.65
571	0.90	0.91	0.00	0.15
285	0.38	0.38	0.17	0.13
142	0.83	0.86	0.72	0.32
```

pvalues decrease as samples become smaller, but with some exceptions
