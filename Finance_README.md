# 💰 **Dago Coffee – Finance Subsystem API**

### System Integration Final Project

* **Subsystem:** *Finance*
* **Port:** `5003`

The Finance subsystem **approves procurement**, **logs financial decisions**, and **performs weekly sales scoring** using data from Sales.



---

## Responsibilities

✔ Evaluate purchase requests
✔ Approve or reject based on budget rules
✔ Log all finance decisions
✔ Fetch weekly orders from Sales
✔ Compute revenue metrics & sales score

---

## API Interfaces

| Endpoint               | Method | Description                  |
| ---------------------- | ------ | ---------------------------- |
| `/PurchaseRequest`     | POST   | Receive procurement requests |
| `/finance/history`     | GET    | Finance decision history     |
| `/finance/request-log` | GET    | Raw request logs             |
| `/sales/score-weekly`  | POST   | Compute weekly sales metrics |
| `/sales/logs`          | GET    | View sales scoring history   |
| `/ui`                  | GET    | Finance dashboard            |

---

## Sales Metrics Calculated

✔ Total revenue
✔ Total orders
✔ Average order value
✔ Top product
✔ Sales score (log-scaled)

---

## Databases

```
indago_financial_records.db
indago_request_log.db
indago_sales_log.db
```

---

## Run

```bash
python finance_app.py
```

UI:

```
http://localhost:5003/ui
```

---
