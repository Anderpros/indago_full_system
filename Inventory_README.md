# 📦 **Dago Coffee – Inventory & Procurement Subsystem API**

### System Integration Final Project

* **Subsystem:** *Inventory + Procurement*
* **Port:** `5002`

This subsystem **tracks raw materials**, **consumes stock from Kitchen production**, and **automatically triggers procurement requests to Finance** when stock is low.



---

## Responsibilities

✔ Maintain inventory levels
✔ Receive batch consumption from Kitchen
✔ Detect low stock automatically
✔ Trigger procurement requests to Finance
✔ Log all procurement activity

---

## API Interfaces

| Endpoint                   | Method | Description                               |
| -------------------------- | ------ | ----------------------------------------- |
| `/stock`                   | GET    | Get current inventory stock               |
| `/consume?date=YYYY-MM-DD` | POST   | Pull batch consumption from Kitchen       |
| `/purchase-request`        | POST   | Manually send purchase request to Finance |
| `/ui`                      | GET    | Inventory UI dashboard                    |

---

## Cross-Subsystem Communication

| Target      | Endpoint                     |
| ----------- | ---------------------------- |
| **Kitchen** | `GET /batch?date=YYYY-MM-DD` |
| **Finance** | `POST /PurchaseRequest`      |

---

## Database

```
indago_inventory.db
```

Tables:

* `inventory`
* `procurement_log`

---

## Run

```bash
python app.py
```

UI:

```
http://localhost:5002/ui
```

---
