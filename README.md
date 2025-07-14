# 📦 Timetabling and Warehouse Allocation

This repository contains two real-world optimization problems modeled using **Integer Linear Programming (ILP)** and solved using **Gurobi** in Python. The project demonstrates the use of mathematical modeling to address practical challenges in scheduling and logistics.

Developed as part of the course **Operational Research** at the **Aristotle University of Thessaloniki (AUTH)**, School of Electrical & Computer Engineering.

---

## 🧠 Problem 1: School Timetabling

### 🎯 Objective

Design a weekly schedule for two different school classes, assigning subjects and teachers to specific time slots while satisfying:

- The required weekly hours for each subject
- Teacher availability
- No double-booking of teachers or classes
- Subject-teacher compatibility

### ⚙️ Approach

- Modeled as a **Mixed Integer Linear Program (MILP)**
- Binary decision variables represent whether a subject is taught in a specific time slot by a specific teacher in a specific class
- Solved using the `gurobipy` API

### ✅ Results

- Generated valid, conflict-free weekly timetables for both classes
- All constraints were successfully satisfied

Example output (simplified):

```
Class 1 – Monday
08:00-09:00: Math (Teacher 1)
09:00-10:00: History (Teacher 2)
...

Class 2 – Tuesday
08:00-09:00: Physics (Teacher 3)
...
```

---

## 🧠 Problem 2: Warehouse Allocation (Capacitated Facility Location)

### 🎯 Objective

Select a subset of 12 candidate warehouse locations to open and assign 12 service points to them, minimizing the total cost (fixed + transportation) while satisfying:

- Each service point is served by exactly one open warehouse
- Opened warehouses must respect capacity constraints

### 📊 Given

- A 12×12 transportation cost matrix
- Fixed costs to open each warehouse
- Capacity and demand values

### ⚙️ Approach

- ILP model with binary variables:
  - Whether each warehouse is opened
  - Whether each service point is assigned to a warehouse
- Constraints ensure valid assignments and capacity limits

### ✅ Results

- Optimal selection of warehouses to open
- Each service point was assigned to exactly one open warehouse
- Total cost minimized and all constraints respected

Example (simplified):

```
Opened Warehouses: [3, 7, 9]
Assignments:
  Service Point 1 → Warehouse 3
  Service Point 2 → Warehouse 9
  ...
```

---

## 🛠 Technologies Used

- **Language**: Python 3
- **Solver**: Gurobi Optimizer
- **API**: `gurobipy`
- **Notebook**: Jupyter (.ipynb)
- **Problem Type**: Integer Linear Programming (ILP), Facility Location, Timetabling

---

## 📁 Repository Structure

```
timetabling-and-warehouse-allocation/
├── OR_assignment.ipynb     # Full notebook with models, solutions, and output
└── README.md               # Project description and explanation (this file)
```

---

## ✍️ Author

**Panagiotis Koutris**  
📧 pkoutris@ece.auth.gr  
🎓 Undergraduate Student, AUTh – School of Electrical & Computer Engineering

---

## 📝 License

This project is provided for **academic and educational purposes** only.
