````markdown
# 🛢️ Company Database Schema

This project contains a sample **company database** built for practicing **SQL and DBMS concepts**.  
It models a corporate structure with employees, branches, clients, suppliers, and sales.

## 📂 Contents
- `company.sql` → Schema + sample data (employees, branches, clients, suppliers, works_with table).

## 📊 Schema Overview
- **Employee** → Stores employee details, managers, salaries, and branch assignments.  
- **Branch** → Each branch with a manager and start date.  
- **Client** → Clients linked to branches.  
- **Works_With** → Many-to-many relationship between employees and clients with total sales.  
- **Branch_Supplier** → Branch suppliers with supply type.

## 🔍 Example Queries
```sql
-- List all employees working in Scranton branch
SELECT e.first_name, e.last_name
FROM employee e
JOIN branch b ON e.branch_id = b.branch_id
WHERE b.branch_name = 'Scranton';

-- Find total sales made by Jim Halpert
SELECT SUM(total_sales) AS total_sales
FROM works_with w
JOIN employee e ON w.emp_id = e.emp_id
WHERE e.first_name = 'Jim' AND e.last_name = 'Halpert';
````

## 🚀 Usage

1. Run `company.sql` in your MySQL / MariaDB environment.
2. Execute queries to practice **joins, foreign keys, subqueries, aggregation, and constraints**.

---

✍️ Created for DBMS interview preparation and SQL practice.

```

Would you like me to also make a **root README** (for the full repo in case you add more schemas later), or just keep this one inside the `company-db` folder for now?
```
