[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

>> 
```
pmf = thinkstats2.Pmf(resp.numkdhh, label='numkdhh')
thinkplot.Pmf(pmf)
thinkplot.Config(xlabel='Num children', ylabel='PMF')
```

![chap3_1a](https://github.com/kimjaesung/dsp/blob/master/img/stats3_1.png "")

```
bias = BiasPmf(pmf, label='bias')
thinkplot.PrePlot(2)
thinkplot.Pmfs([pmf, bias])
thinkplot.Config(xlabel='Num children', ylabel='PMF')
```

![chap3_1b](https://github.com/kimjaesung/dsp/blob/master/img/stats3_1b.png "")
