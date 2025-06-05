**Project & Budget Tracking App – Notes**

>This is a custom-built app that pulls project and invoice data from QuickBooks Online and stores it in a structured MySQL database. The goal is to provide project managers and admin staff with an internal dashboard that summarizes budgets, expenses, and outstanding invoices.

---

**Core Features (Planned and In Progress)**

- Python backend to interact with the QuickBooks Online API
- OAuth2 authentication to access secure financial data
- Store data in a local MySQL database (projects, clients, invoices)
- Front-end web interface (planned) using Flask or similar
- CSV export and basic filtering/reporting tools for non-technical users

---

**Data Structure (MySQL Tables)**

- `clients` – client name, contact info, QBO ID
- `projects` – linked to clients, with budgets and timelines
- `invoices` – linked to projects, with amounts, due dates, statuses

---

**Security Considerations**

- OAuth2 token handling using `python-dotenv`
- Environment variables for API keys and secrets
- Parameterized queries to prevent SQL injection
- Planned user-based access control and read-only export roles

---

**Current Status**

- [x] MySQL schema designed and tested
- [x] QuickBooks app created and connected to sandbox
- [x] OAuth2 token flow working (manual copy/paste)
- [ ] Automate token refresh
- [ ] Build basic Flask front-end
- [ ] Add CSV export from filtered views

---

**Notes**

- Sandbox testing only — no live data used
- Using `mysql-connector-python` for DB connection
- Possible future integration with Google Sheets or Power BI
