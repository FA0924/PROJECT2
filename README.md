<h1 align="center"> 🛠️ Home Appliance Repair Management System</h1>
<div align="center">

![Logo](https://i.postimg.cc/6qjw7wJz/Group-9-(1).png)
</div>



<p align="center">
  <img src="https://img.shields.io/badge/Status-Completed-success?style=for-the-badge" alt="Status">
  <img src="https://img.shields.io/badge/Backend-C%23-blue?style=for-the-badge" alt="C#">
  <img src="https://img.shields.io/badge/Frontend-HTML%2C%20CSS%2C%20JavaScript%2C-lightgrey?style=for-the-badge" alt="Concepts">
  <img src="https://img.shields.io/badge/Author-Group 1-blueviolet?style=for-the-badge" alt="Author">
</p>

---

## 📖 Overview
This system helps a home appliance repair company manage their operations.
It handles customers, technicians, repair orders, invoices, and reports.

---

## ✨ Features
- 👤 **Customers:** Add, Edit, Delete, View  
- 🛠️ **Technicians:** Add, Edit, Delete, View  
- 📋 **Repair Orders:** Create, Assign Technician, Update Status, Complete, Cancel, View  
- 💰 **Invoices:** Automatically generated for completed orders  
- 📊 **Reports:** Orders by status, technician, and date  

---

## 💻 Console Application
**Main Menu:**  
- 👤 Customers  
- 🛠️ Technicians  
- 📋 Repair Orders  
- 📊 Reports  
- ❌ Exit  

**Repair Orders Menu:**  
- ➕ Add Order  
- 👨‍🔧 Assign Technician  
- 🔄 Update Status  
- ✅ Complete Order (Enter Costs → Generate Invoice)  
- 🚫 Cancel Order  
- 👀 View Orders  

---

## 🌐 Web Prototype
Static HTML/CSS/Bootstrap pages:  
- 📊 Dashboard  
- 👤 Customers (List, Add, Edit)  
- 🛠️ Technicians (List, Add, Edit)  
- 📋 Repair Orders (List, Create, Assign, Update Status)  
- 💰 Invoices (List, View)  
- 📈 Reports (Charts & Tables)

> ⚠️ Note: Web pages are static and not connected to the database.  

---

## 🗄️ Database ERD / Schema
![Erd](https://i.postimg.cc/FsT1c5gC/erdplus-(12).png)  
ERD Home Appliance Repair Management System  

![Schema](https://i.postimg.cc/rwqbB3vZ/Whats-App-Image-2025-11-18-at-11-59-19-AM.jpg)  
Schema Home Appliance Repair Management System  

### Entities and Attributes
1. **Customer**  
   - CustomerId (PK)  
   - Name  
   - Phone  
   - Address  

2. **Technician**  
   - TechnicianId (PK)  
   - Name  
   - Phone  
   - Specialty  

3. **RepairOrder**  
   - RepairOrderId (PK)  
   - CustomerId (FK → Customer)  
   - TechnicianId (FK → Technician, *optional*)  
   - ApplianceType  
   - ProblemDescription  
   - RequestDate  
   - Status (Pending, Assigned, In Progress, Completed, Cancelled)  

4. **RepairOrderPart**  
   - RepairOrderPartId (PK)  
   - RepairOrderId (FK → RepairOrder)  
   - PartName  
   - PartCost  

5. **Invoice**  
   - InvoiceId (PK)  
   - RepairOrderId (FK → RepairOrder)  
   - ServiceCost  
   - PartsCost  
   - TotalAmount  
   - InvoiceDate  

### Relationships
- 👤 **Customer → RepairOrder**: One-to-Many  
- 🛠️ **Technician → RepairOrder**: One-to-Many  
- 🔧 **RepairOrder → RepairOrderPart**: One-to-Many  
- 💰 **RepairOrder → Invoice**: One-to-One  

---

## ⚙️ Installation
1. Clone the repository:  
```bash
git clone <repository-url>
```
2. Open the solution in Visual Studio
3. Restore NuGet packages
4. Run EF migrations:
```bash
Update-Database
```

5. Run the console application
---
### 📊 Usage
- Navigate menus to manage customers, technicians, and repair orders
- Complete orders to generate invoices automatically
- Generate reports to track operations

### 🚀 Future Enhancements
- 🔑 Add login and user roles
- 🌐 Connect web pages to the database
- 🔔 Notifications for customers and technicians
- 🧩 Spare parts inventory management
- 📱 Mobile app interface

--- 
## 👥 Team:
#### Group 1:
##### 👨🏻‍💻Fayadh Alhabsi
##### 👩🏻‍💻Fatima Alshanfari
##### 👩🏻‍💻Raya Alamri
##### 👩🏻‍💻Fatma Younis
##### 👩🏻‍💻Noura  Almaqbali


---

<p align="center"><b>✨ “The project was successfully completed through teamwork and achieving all planned goals.” ✨</b></p>
