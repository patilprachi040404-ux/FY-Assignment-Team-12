# Customer, Product, Sales & Return Management System

## 📌 Project Overview

The **Customer, Product, Sales & Return Management System** is a database management project designed to manage customer information, product information, sales transactions, and product return requests efficiently.

The system helps maintain organized records and provides a simple workflow for managing sales and returns.

---

## 🎯 Objectives

* Manage customer details efficiently.
* Maintain product and stock information.
* Record and manage sales transactions.
* Allow customers to submit return requests.
* Track and update return status.
* Manage refund and stock updates for approved returns.
* Reduce manual record keeping and data duplication.
* Provide accurate and organized database records.

---

## 🚀 Features

### 1. Customer Details

The system allows the user/admin to:

* Add new customer details.
* View customer information.
* Update customer information.
* Delete customer records.
* Search customer details.

### 2. Product Details

The product module manages:

* Product ID
* Product Name
* Category
* Price
* Stock Quantity
* Product information
* Stock updates

### 3. Sales Details

The sales module allows the user to:

* Select a customer.
* Select a product.
* Enter purchase quantity.
* Check product availability.
* Calculate total amount.
* Record sales transactions.
* Update product stock after a sale.

### 4. Return Request

The return module allows the user/customer to:

* Select a previous sale.
* Select the product to be returned.
* Enter return quantity.
* Enter return reason.
* Submit a return request.
* Store return request details.

### 5. Return Status

The system allows the admin to:

* View return requests.
* Review return requests.
* Approve or reject requests.
* Update return status.
* Calculate/process refund for approved returns.
* Update product stock after an approved return.
* Mark the return request as completed.

---

## 🔄 System Workflow

```text
START
  |
  v
Customer Details
  |
  v
Product Details
  |
  v
Sales Details
  |
  v
Check Stock
  |
  +---- No ----> Out of Stock
  |
 Yes
  |
  v
Complete Sale
  |
  v
Update Stock
  |
  v
Return Request
  |
  v
Review Return Request
  |
  v
Approve / Reject
  |
  +---- Reject ----> Return Status: Rejected
  |
 Approve
  |
  v
Calculate Refund
  |
  v
Update Stock
  |
  v
Return Status: Completed
  |
  v
END
```

---

## 🗄️ Main Database Entities

The project mainly contains the following entities:

### Customer

| Field         | Description                |
| ------------- | -------------------------- |
| Customer_ID   | Unique customer identifier |
| Customer_Name | Customer name              |
| Email         | Customer email             |
| Phone         | Customer contact number    |
| Address       | Customer address           |

### Product

| Field          | Description               |
| -------------- | ------------------------- |
| Product_ID     | Unique product identifier |
| Product_Name   | Product name              |
| Category       | Product category          |
| Price          | Product price             |
| Stock_Quantity | Available stock           |

### Sales

| Field          | Description            |
| -------------- | ---------------------- |
| Sale_ID        | Unique sale identifier |
| Customer_ID    | Customer reference     |
| Product_ID     | Product reference      |
| Sale_Date      | Date of sale           |
| Quantity       | Quantity purchased     |
| Total_Amount   | Total sales amount     |
| Payment_Status | Payment status         |

### Return Request

| Field           | Description              |
| --------------- | ------------------------ |
| Return_ID       | Unique return identifier |
| Sale_ID         | Related sale             |
| Customer_ID     | Customer reference       |
| Product_ID      | Product reference        |
| Return_Date     | Date of return request   |
| Return_Quantity | Quantity being returned  |
| Return_Reason   | Reason for return        |

### Return Status

| Field            | Description                         |
| ---------------- | ----------------------------------- |
| Return_Status_ID | Unique status identifier            |
| Return_ID        | Return request reference            |
| Status           | Pending/Approved/Rejected/Completed |
| Refund_Amount    | Refund amount                       |
| Refund_Status    | Refund status                       |
| Remarks          | Additional information              |

---

## 🔗 Relationships

The major relationships in the system are:

* One **Customer** can have many **Sales**.
* One **Product** can appear in many **Sales**.
* One **Customer** can create multiple **Return Requests**.
* One **Product** can have multiple **Return Requests**.
* A **Sales** record can be associated with a **Return Request**.
* Each **Return Request** has a corresponding **Return Status**.

---

## 🛠️ Technologies Used

Update this section according to your actual implementation.

* **Frontend:** HTML, CSS, JavaScript
* **Backend:** [Add your backend technology]
* **Database:** MySQL
* **IDE:** [Add your IDE]
* **Version Control:** Git / GitHub

---

## 📂 Project Structure

```text
Customer-Product-Sales-Return-Management/
│
├── README.md
├── frontend/
│   ├── index.html
│   ├── style.css
│   └── script.js
│
├── backend/
│   └── [backend files]
│
├── database/
│   └── database.sql
│
├── diagrams/
│   ├── ER-Diagram.png
│   └── Flowchart.png
│
└── documentation/
    └── Project-Report.pdf
```

---

## ⚙️ Installation & Setup

### Step 1: Clone the Repository

```bash
git clone <your-github-repository-url>
```

### Step 2: Open the Project

```bash
cd Customer-Product-Sales-Return-Management
```

### Step 3: Setup Database

1. Open MySQL.
2. Create a new database.
3. Import the `database.sql` file.
4. Configure the database connection in the backend.

### Step 4: Run the Application

Run the backend using your selected backend technology and open the frontend/application in your browser.

---

## 🧪 System Operations

### Customer Management

```text
Add Customer
     ↓
Validate Details
     ↓
Save Customer
     ↓
Display Customer
```

### Product Management

```text
Add Product
     ↓
Validate Product
     ↓
Save Product
     ↓
Manage Stock
```

### Sales Management

```text
Select Customer
     ↓
Select Product
     ↓
Enter Quantity
     ↓
Check Stock
     ↓
Calculate Total
     ↓
Confirm Sale
     ↓
Update Stock
```

### Return Management

```text
Select Previous Sale
     ↓
Select Product
     ↓
Enter Return Reason
     ↓
Submit Request
     ↓
Review Request
     ↓
Approve / Reject
     ↓
Update Return Status
     ↓
Process Refund & Update Stock
```

---

## 🔐 Data Validation

The system should validate:

* Required customer information.
* Valid product information.
* Valid sales quantity.
* Product stock availability.
* Valid return quantity.
* Return request associated with an existing sale.
* Return status before processing refund.

---

## 📊 Expected Benefits

* Easy customer record management.
* Better product and stock tracking.
* Organized sales records.
* Simple return request management.
* Easy return status tracking.
* Reduced manual errors.
* Centralized database management.

---

## 🔮 Future Enhancements

Possible future improvements include:

* User authentication and role-based access.
* Online payment integration.
* Email/SMS notifications for return status.
* Sales and return reports.
* Dashboard with sales statistics.
* Invoice generation.
* Advanced product search and filtering.
* Automated refund processing.

---

## 👩‍💻 Project Information

**Project Name:** Customer, Product, Sales & Return Management System

**Project Type:** Database Management System / Mini Project

**Domain:** Sales & Return Management

**Database:** MySQL

**Repository:** Add your GitHub repository link here.

---

## 📄 License

This project is developed for **educational/academic purposes**.

---

## 🙏 Acknowledgement

This project was developed as part of an academic project to understand database design, entity relationships, sales management, and return management processes.
