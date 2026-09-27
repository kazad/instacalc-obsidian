---
sleep_hours: 7.5
steps: 8200
---

# Totals across the vault

![Demo: Totals across the vault](https://raw.githubusercontent.com/kazad/instacalc-obsidian/main/media/lessons/06-totals-across-the-vault.gif)

The properties above are variables in this note, so a daily note computes from  
its own header:

sleep_debt = 8 - sleep_hours  
steps_to_goal = 10000 - steps

## Adding up a folder

A reference reads one number from one note. To total many, name a folder and a  
property:

spend = vaultsum("Instacalc Tutorial/Tutorial Expenses/**", amount)  
receipts = vaultcount("Instacalc Tutorial/Tutorial Expenses/**", amount)  
typical = vaultavg("Instacalc Tutorial/Tutorial Expenses/**", amount)

`*` matches inside one folder, `**` matches below it too, and the `.md` is  
optional because you think in note names.

A query that matches nothing is an **error**, not a zero — a folder typo that  
silently reported `0` would look exactly like a real answer:

oops = vaultsum("Instacalc Tutorial/Tutorial Expensez/**", amount)

Next: *07 - Tables of data*.
