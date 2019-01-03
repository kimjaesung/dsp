[Think Stats Chapter 8 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2009.html#toc77) (scoring)

>> 

```
n = 10
iters = 1000

est = [] 

for _ in range(iters):
  s = np.random.exponential(1.0/2.0, n)
  est.append(1.0 / np.mean(s))

std_err = RMSE(est, 2.0) 
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

![chap8_2](https://github.com/kimjaesung/dsp/blob/master/img/stats8_2.png "")


```
def stats82(n):
    iters = 1000
    est = [] 

    for _ in range(iters):
      s = np.random.exponential(1.0/2.0, n)
      est.append(1.0 / np.mean(s))

    return RMSE(est, 2.0) 


std_errs = []
low_n = 10
hi_n = 200
for n in range(low_n,hi_n):
    std_errs.append(stats82(n))

thinkplot.plot(obj=range(low_n,hi_n), ys=std_errs)
```

![chap8_2](https://github.com/kimjaesung/dsp/blob/master/img/stats8_2b.png "")
