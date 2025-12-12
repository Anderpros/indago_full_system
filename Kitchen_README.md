
# 🍳 **Dago Coffee – Kitchen Subsystem API**

### System Integration Final Project

* **Subsystem:** *Kitchen*
* **Port:** `5004`

The Kitchen subsystem **executes production**, **calculates material consumption using recipes**, and **records batch usage for Inventory**.



---

## Responsibilities

✔ Fetch orders from Sales
✔ Apply recipes (Bill of Materials)
✔ Validate stock with Inventory
✔ Record batch consumption per date
✔ Provide consumption data to Inventory

---

## API Interfaces

| Endpoint                 | Method | Description                 |
| ------------------------ | ------ | --------------------------- |
| `/start-production`      | POST   | Start production for a date |
| `/batch?date=YYYY-MM-DD` | GET    | Get material consumption    |
| `/ui`                    | GET    | Kitchen UI                  |

---

## Recipe Logic

Each product consumes predefined raw materials:

```json
Latte → beans (8g), milk (200ml)
Capucino → beans (10g), milk (150ml)
```

---

## Database

```
indago_kitchen.db
```

Table:

* `batch_consumption` (append-only)

---

## Run

```bash
python kitchen_app_with_ui.py
```

UI:

```
http://localhost:5004/ui
```

---
