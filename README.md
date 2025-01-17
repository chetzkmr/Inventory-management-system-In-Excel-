Inventory Management System with Auto-Update and Dashboard

Project Overview

This project is an Inventory Management System designed to streamline the management of inventory, purchases, sales, vendors, and customers. The system provides a dynamic dashboard for visual insights, automatic updates for stock levels, and notifications for low-stock items. It is built using Excel with advanced formulas and data visualization tools.

Features

1. Dynamic Dashboard

Visual representation of key metrics:

Top 5 Customers

Top 5 Products

Total Customers and Products

Sales Amount, Stock Amount, and Profit/Loss

Notifications: Alerts for products with stock levels below 5 units.

Bar charts and summary tables for quick decision-making.

2. Customer Management

Comprehensive customer details stored in the Customers sheet.

Customer IDs linked with sales records using VLOOKUP for seamless data retrieval.

3. Product Management

Detailed product information maintained in the Products sheet.

Each product identified by a unique HSN Code.

4. Vendor Management

Vendor details managed in the Vendors sheet.

Enables tracking of suppliers for purchases.

5. Purchase and Sales Tracking

Purchase Sheet:

Tracks all purchase transactions.

Total cost calculated using the formula:

=IFERROR(VLOOKUP([@[HSN Code]],productsdata[#All],3,0), " ")

Total amount = Units Purchased × Cost.

Sales Sheet:

Records sales transactions.

Customer names retrieved using VLOOKUP based on Customer IDs.

6. Inventory Management

Inventory Table:

Stock levels auto-updated using the formula:

=SUMIF(Table5[Product Name],[@[Product Name]],Table5[Units])

Tracks purchase and sales units for each product.

7. Profit and Loss Analysis

Pivot Tables in the Pivots Sheet provide:

Purchase Amount, Sales Amount, and Stock Amount.

Profit/Loss calculations for business insights.

Sheets Description

Dashboard: Interactive visualizations and KPIs.

Customers: Detailed customer data.

Products: Product catalog with HSN Codes.

Vendors: Vendor information.

New Entry: Input sheet for adding new records.

Purchase: Tracks purchases with cost calculations.

Sales: Records sales transactions.

Inventory: Current stock levels with auto-updates.

Pivots: Data analysis using pivot tables.

Key Formulas Used

Cost Calculation:

=IFERROR(VLOOKUP([@[HSN Code]],productsdata[#All],3,0), " ")

Total Amount:

=Units × Cost

Stock Level Updates:

=SUMIF(Table5[Product Name],[@[Product Name]],Table5[Units])

VLOOKUP for Customer Name Retrieval:

=VLOOKUP([@[Customer ID]],customerdata[#All],2,0)

Technologies Used

Microsoft Excel

Formulas: VLOOKUP, IFERROR, SUMIF.

Pivot Tables for data analysis.

Data visualization for the dashboard.
