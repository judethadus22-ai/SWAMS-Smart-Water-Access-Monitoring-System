# Smart Water Access & Monitoring System

A desktop-based **Community Data Processing System** developed natively in Python to process, store, and analyze suburban household water utilization logs[span_0](start_span)[span_0](end_span). This software explicitly aligns with **Sustainable Development Goal 6 (Clean Water and Sanitation)** by establishing computational guardrails on storage thresholds and offering diagnostic visual tools to target conservation and identify utility leaks early.

---

## 🚀 Key Features

* **Household Registry:** Captures unique Identification Numbers (IDs), full legal names, gender, verification status, contact details, and location identifiers via an interactive desktop form.
* **Usage Recording & Data Persistence:** Tracks active water utilization metrics measured in Litres (L) and automatically registers transactional timestamps within an embedded relational database.
* **Live Storage Diagnostics:** Features an algorithmic monitor that dynamically updates tank capacity levels and surfaces conditional status alerts (**NORMAL**, **WARNING**, or **CRITICAL**) using explicit UI color coding.
* **Visual Data Analytics:** Automatically generates dynamic data distributions mapping volumetric trends and categorical consumption shares across household configurations using `matplotlib` pipelines.
* **Administrative Authentication:** Safeguards community database registries with a secure login frame before granting administrative rights.

---

## 🛠️ System Architecture & Technology Stack

The desktop application satisfies academic project constraints by bypassing terminal-only script flows in favor of an intuitive Graphical User Interface (GUI) and persistent relational backend layer.

* **Language:** Python 3
* **Frontend UI Framework:** `tkinter`
* **Database Engine:** `sqlite3` (Embedded)
* **Data Visualization:** `matplotlib`

### Relational Database Schema
The database layer is managed through two core relational tables utilizing strict parametrized assertions for secure data mutation pipelines:
1. `households`: Manages demographic properties (ID, Name, Gender, Status, Contact, Community).
2. `usage_logs`: Stores transactional sequential consumption data, linking back to households via foreign keys.

---

## 📂 Project Structure

```text
├── main.py        # Application entry point, window initiation, and layout management
├── project.py     # Functional operational logic, relational query execution, and core logic
└── README.md      # Project overview and execution documentation
