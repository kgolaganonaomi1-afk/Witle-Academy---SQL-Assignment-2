## 🧠 Witle Academy SQL Assignment 2 


---
## 🗺️ Project overview:

You have joined Sizwe Coffee as a junior data analyst. The financial year ended on 30 June 2025 and the year-end review is in two weeks. 
Nomsa Dlamini, the Financial Director, and Bongani Twala, the National Sales Manager, have each sent you a list of things they want to understand before that meeting. 


# The tasks 
###### Task 1 - Channel performance 
###### Task 2 - Where the profit actually comes from 
###### Task 3 - The collections problem 
###### Task 4 - The ten accounts that matter most 
###### Task 5 - A commercial gap 
###### Task 6 - Are the sales representatives hitting target? 
###### Every sales representative must appear, including any who generated no revenue. 
###### Task 7 - The shape of the year 
###### Task 8 - Why has the margin moved? 

----

## 📦 The dataset

The full dataset contains six CSV files. 

| File | Rows | Description |
| ----------------------- | ------- | ---------------------------------------------------- |
| `customers.csv` | 1,400 | One row per customer - name, channel, segment, province, credit limit, assigned sales,representative  |
| `products.csv` | 23 | One row per SKU - product line, pack size, list price, unit cost  |
| `sales_orders.csv` | 45,144 |  One row per order - customer, order date, delivery date, channel, sales representative |
| `sales_lines.csv` | 168,172 | One row per order line - SKU, units, unit price, discount, line revenue, cost of goods  |
| `ar_ledger` | 48,144 |  One row per customer invoice - amount, due date, amount settled, settlement date |
| `reps.csv` | 18 | Sales representatives - territory, monthly target |
| `rep_visits.csv` | 9,400 | Visits made by sales representatives to customers, with the outcome |
| `trade_promotions` | 640 | Promotional support given to a customer on a SKU |
| `vendors.csv` | 74 | Suppliers - type, payment terms |

## How the tables connect.

• sales_orders.customer_id → customers.customer_id

• sales_orders.order_id → sales_lines.order_id

• sales_lines.sku → products.sku

• sales_orders.rep_id and customers.rep_id → reps.rep_id 

• ar_ledger.customer_id → customers.customer_id

• rep_visits.customer_id and trade_promotions.customer_id → customers.customer_id

Two things to notice before you start. Revenue lives on `sales_lines`, not on `sales_orders` - an order 
has no value of its own, only the sum of its lines. And `channel` appears on both `customers` and 
`sales_orders` - use whichever the question points at, and be ready to explain why they agree. 


**Skills demonstrated**
- SQL — Joins, Aggregations, CASE expressions, CTEs, window functions, ranking
- DAX — time intelligence, ranking, customer cohort logic
- Data validation and reconciliation
- Data quality auditing and remediation
- Technical writing and documentation


## 💻 How to run: Tools & skills used

**Tools**
- Databricks (SQL)
- DAX
- GitHub
  
----

##### Task 1 - Channel performance 
Nomsa needs the revenue split by channel for FY2024 and FY2025 side by side, with the growth rate between them. One row per channel, three figures on each. 
FY2024 is orders placed on or before 30 June 2024. FY2025 is everything after that.
##### Task 1 Answer - Channel performance 



##### Task 2 - Where the profit actually comes from 
For each product line, return revenue, cost of goods, gross profit and gross margin percentage. Sort by gross profit. In one or two sentences under your query: which line earns the most profit, and is it the same line that earns the highest margin? 
##### Task 2 Answer - Where the profit actually comes from 



##### Task 3 - The collections problem 
Nomsa suspects the business is being paid more slowly than it used to be, and wants to know where the problem sits. For each channel, return the number of invoices, how many have been settled, how many are still open, the average number of days taken to settle, and the total value still outstanding. In two or three sentences: what does this tell you, and which channel would you investigate first? 
##### Task 3 Answer - The collections problem 



##### Task 4 - The ten accounts that matter most 
Bongani wants a one-page list of the ten largest customers by FY2025 revenue, showing the trading name, segment, province, the sales representative who owns the account, and the revenue. Not every customer has a sales representative. Make sure your query does not silently drop anyone. 
##### Task 4 Answer - The ten accounts that matter most 



##### Task 5 - A commercial gap 
Trade promotions are how Sizwe supports its wholesale accounts. Bongani thinks some sizeable customers have been getting nothing. Return the fifteen highest-revenue Wholesale customers who have never received a trade promotion, with their segment and province. One sentence: what would you recommend doing about the top three? 
##### Task 5 Answer - A commercial gap 



##### Task 6 - Are the sales representatives hitting target? 
Each sales representative carries a monthly revenue target. Return every sales representative with their territory, their monthly target, their actual FY2025 monthly average, and that average as a percentage of target. Sort by percentage of target, best first. Every sales representative must appear, including any who generated no revenue. 
##### Task 6 Answer - Are the sales representatives hitting target? 



##### Task 7 - The shape of the year 
Return monthly revenue across the full two years, with the percentage change on the previous month and a rolling three-month average alongside it. In two sentences: is there a seasonal pattern, and when is Sizwe's quietest month?
##### Task 7 Answer - The shape of the year 



##### Task 8 - Why has the margin moved? 
Gross margin fell from 34.7% in FY2024 to 33.0% in FY2025, while revenue grew nearly 9%. Nobody can explain it. For each product line, return revenue and gross margin for each financial year, plus that line's share of total revenue in that year. Then answer, in a short paragraph: what caused the margin decline? Your answer must point at specific numbers in your result. 
##### Task 8 - Why has the margin moved? 



## 🔍 Key insights

----


## 📬 References

🔗[DAX function reference](https://learn.microsoft.com/dax/)

📘[Nova Retail Group — Sales Analytics by Clarence Mantiya](https://github.com/Clarence-Mantiya/test-project2/blob/main/README.md?plain=1) for Github layout


---

## ⭐ Let's Connect

- 💼 LinkedIn: https://www.linkedin.com/in/kgolagano-naomi-selebano/
- 📧 Email: kgolaganonaomi1@gmail.com

