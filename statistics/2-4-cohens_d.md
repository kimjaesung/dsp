[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

>> ```
resp = nsfg.ReadFemResp()
rich = resp[resp.totincr == 14]
notrich = resp[resp.totincr < 14]
CohenEffectSize(rich.parity, notrich.parity)

```

>> -0.12511855314660611
