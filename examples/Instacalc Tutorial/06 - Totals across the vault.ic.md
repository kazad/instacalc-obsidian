---
sleep_hours: 7.5
steps: 8200
---

# Totals across the vault

![Demo: Totals across the vault](https://raw.githubusercontent.com/kazad/instacalc-obsidian/main/media/lessons/06-totals-across-the-vault.gif)

The properties above are values in this note, so a daily note can compute from its own header:

sleep_debt = 8 - sleep_hours  
steps_to_goal = 10000 - steps

## Adding up a folder

To total many notes, name a folder and a property:

spend = vaultsum("Instacalc Tutorial/Tutorial Expenses/**", amount)  
receipts = vaultcount("Instacalc Tutorial/Tutorial Expenses/**", amount)  
typical = vaultavg("Instacalc Tutorial/Tutorial Expenses/**", amount)

`*` matches one folder, `**` includes its subfolders, and `.md` is optional.

A folder that matches nothing shows an error, not a zero:

oops = vaultsum("Instacalc Tutorial/Tutorial Expensez/**", amount)

Next: [07 - Tables of data](07%20-%20Tables%20of%20data.md).
