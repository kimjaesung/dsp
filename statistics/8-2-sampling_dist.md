[Think Stats Chapter 8 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2009.html#toc77) (scoring)

>> 

```
n = 10
iters = 1000

est = [] 

for _ in range(iters):
  s = np.random.exponential(1.0/2.0, n)
  est.append(1.0 / np.mean(s))

std_err = RMSE(est, L) 
cdf = thinkstats2.Cdf(est)
con_int = cdf.Percentile(5), cdf.Percentile(95)
thinkplot.Cdf(cdf)
thinkplot.Config(xlabel='estimate', ylabel='cdf', title='sample dist')
print('std. error:', std_err)
print('con. interval:', con_int)
```

```
std. error: 0.782724624248741
con. interval: (1.2803919094553737, 3.5850023190341047)
```

![chap8_2](https://github.com/kimjaesung/dsp/blob/master/img/stat8_2.png "")

