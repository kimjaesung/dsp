[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

>>  
```
soln = np.random.random(1000)
soln_pmf = thinkstats2.Pmf(soln)
thinkplot.Pmf(soln_pmf, linewidth=0.1)
thinkplot.Config(xlabel='1000 random numbers', ylabel='PMF')
```

```
soln_cdf = thinkstats2.Cdf(soln)
thinkplot.Cdf(soln_cdf)
thinkplot.Config(xlabel='1000 random numbers', ylabel='CDF')
```


