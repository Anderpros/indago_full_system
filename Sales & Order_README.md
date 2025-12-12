☕ Dago Coffee – Sales & Order Subsystem API
System Integration Final Project

Author: Group 1 (Leonard, Abi, Gabby)

Subsystem: Sales & Order

Port: 5001

(Part of the Dago Coffee Integrated System: Sales/Order, Inventory+Procurement, Finance, Kitchen)

This subsystem manages order input and aggregation, serving as the source of truth for orders used by Kitchen and Finance.

order_app

🔹 Responsibilities

✔ Accept individual orders
✔ Store orders in SQLite
✔ Aggregate daily orders into weekly summaries
✔ Provide weekly order data to other subsystems

📡 API Interfaces
Endpoint	Method	Description
/add-order	POST	Add individual customer order
/aggregate	POST	Aggregate individual orders into weekly orders
/orders-weekly	GET	Provide weekly aggregated orders to Kitchen & Finance
/	GET	UI dashboard
📁 Data Storage
indago_individual_orders.db
indago_weekly_orders.db


Individual orders → individual_orders

Aggregated orders → weekly_orders

🚀 Run
python app.py


UI:

http://localhost:5001
