[Think Stats Chapter 8 Exercise 3](http://greenteapress.com/thinkstats2/html/thinkstats2009.html#toc77)

---

>> 
```
def sim_game(lam):
    ng, t = 0, 0
    while t<1:
        g_time = random.expovariate(lam)
        t += g_time
        if t<1: ng += 1
    return ng

def many_games(lam=2, n):
    g_est = []

    for i in range(n):
        g_est.append(sim_game(lam))

    print('rmse: ', RMSE(g_est, lam))
    print('mean err: ', MeanError(g_est, lam))
    
    pmf = thinkstats2.Pmf(g_est)
    thinkplot.Hist(pmf)
    thinkplot.Config(xlabel='goals', ylabel='pmf')
    
#many_games(1000)
#many_games(5000)
many_games(10000)
```

```
rmse:  1.399392725434858
mean err: -0.0025
```

![chap8_3](https://github.com/kimjaesung/dsp/blob/master/img/stats8_3.png "")

mean err is relatively small and decreases as n increases, so likely not biased


---
