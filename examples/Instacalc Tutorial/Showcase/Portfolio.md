```ic
holdings = [{fund: "VTI", shares: 40, price: 262}, {fund: "VXUS", shares: 90, price: 63}, {fund: "BND", shares: 60, price: 73}] @sheet @cols(Fund, Shares, Price) @sort(shares desc)
value = sum(map(holdings, h => h.shares * h.price))
biggest = max(map(holdings, h => h.shares * h.price))
```
