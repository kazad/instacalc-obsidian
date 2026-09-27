# A loan, as a document

![Demo: Making a note presentable](https://raw.githubusercontent.com/kazad/instacalc-obsidian/main/media/lessons/10-making-a-note-presentable.gif)

Decorators make a worksheet easier to read. They hide the working, highlight the answer, and label the inputs.

# Inputs

price = 450000 @label(Property price) @prefix($)  
deposit = 90000 @label(Deposit) @prefix($)  
rate = 5.4% @label(Interest rate)  
years = 30 @label(Term)

# Working

principal = price - deposit @hidden  
r = rate / 12 @hidden  
n = years * 12 @hidden

---

# The number

payment = principal * r / (1 - (1 + r)^-n) @hero @label(Monthly payment) @prefix($)  
total paid = payment * n @label(Paid over the term) @prefix($)  
interest = total paid - principal @label(Of which interest) @prefix($)

## The decorators used here

| Directive | Effect |  
|---|---|  
| `# Title` | a section header |  
| `@hero` | the headline number, larger and accented |  
| `@hidden` | computed, not shown — its value still flows on |  
| `@label(…)` | names the value under the expression |  
| `@prefix($)` | renders before the number |  
| `---` | a divider |

Next: [11 - Formulas that compute](11%20-%20Formulas%20that%20compute.md).
