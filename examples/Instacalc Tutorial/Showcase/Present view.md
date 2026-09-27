```ic present
price = 450000 // 200k..900k by 10k @label(Home price)
down = 20% // % 5..40 @label(Down payment)
rate = 6.25% // % 3..9 by 0.25 @label(Interest rate)
payment = pmt(rate/12, 360, -price*(1 - down)) // @hero @label(Monthly payment)
```
