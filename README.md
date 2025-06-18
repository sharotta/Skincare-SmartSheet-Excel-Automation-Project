#  Skincare SmartSheet: Excel Automation for Small Business Operations
A fully functional Excel-based SmartSheet for skincare businesses to track customer invoices, inventory, sales, and stock alerts; built with formulas, conditional formatting, and automation.

## Project Overview
The **Skincare SmartSheet** is a fully automated Excel system built to help small skincare brands manage:

- Inventory tracking  
- Order processing  
- Invoice generation  
- Sales logging  
- Visual stock alerts

It’s designed for small businesses operating without websites — such as those selling through **Instagram**, **WhatsApp**, or **in-store** — offering a low-code solution that mimics a lightweight ERP system.

## Project Objectives

- Automate order and sales tracking in Excel  
- Provide real-time inventory updates  
- Eliminate manual data entry errors  
- Generate print-ready invoices  
- Empower small skincare brands to operate efficiently with no coding knowledge

## File Structure
This project contains a single Excel workbook with the following core sheets:

1. **Product Inventory Tracker**  
2. **Order Form**  
3. **Sales Log**  
4. **Invoice Generator**  
5. *(Helper Table & Macro Sheet – backend automation)*

## Key Features

### 1. Product Inventory Tracker

- Tracks stock by category, product name, and unit price  
- Auto-updates current stock using:  
  `=Opening Stock - Sold Quantity`  
- Conditional alerts for restock using:  
  `=IF(Current Stock < Reorder Level, "⚠️ LOW", "✅ OK")`  
- Uses `SUMIFS()` to calculate sold quantity directly from the invoice log
  
### 2. Dynamic Order Form
![WhatsApp Image 2025-06-18 at 3 03 07 PM (1)](https://github.com/user-attachments/assets/a56bdd65-5a60-4f89-8789-5c1659826c3c)

- Clean form interface for customer and product order entry  
- Drop-down selections for **Product category**, **Product Name**, and **quantity**  
- Auto-fills unit price and calculates:  
  - `Total = Unit Price × Quantity`  
  - `Subtotal`  
  - `VAT = Subtotal × 7.5%`  
  - `Grand Total = Subtotal + VAT`  
- **Submit Button** triggers a macro to:
  - Log orders into the sales sheet  
  - Clear the form for the next entry

### 3. Sales Log
- Automatically logs every submitted order  
- Pulls data via macro from a helper table  
- Ensures new entries appear first (reverse chronological)  
- Uses logic to increment order IDs and avoid duplicates

### 4. Invoice Generator
![WhatsApp Image 2025-06-18 at 3 03 07 PM](https://github.com/user-attachments/assets/7304e1a4-37d5-4b4a-ad00-735ced59da4f)

- Auto-populates invoice with:
  - Order ID  
  - Customer details  
  - Product breakdown with VAT  
  - Total amounts  
- Uses `INDEX()` and `FILTER()` to display the latest order only  
- Print-ready format with placeholder for company branding

## Why This Project Matters
Many small businesses still use manual tracking via notes or chat logs. This SmartSheet helps by:

✅ Simplifying order and billing processes  
✅ Reducing human error  
✅ Providing real-time inventory visibility  
✅ Enabling professional invoicing without extra tools  
✅ Saving hours of manual admin work

## Business Impact & Metrics
- Reduced order processing time by **over 60%**  
- Eliminated **90%+ manual entry errors**  
- Generated invoices in **under 10 seconds**  
- Prevented **stockouts** with visual alerts
  
## Tools & Excel Techniques Used
- Microsoft Excel  
- **VLOOKUP**, **XLOOKUP**, **INDEX**, **FILTER**, **SUMIFS**  
- Data Validation (Drop-downs)  
- Conditional Formatting  
- Macro Recording (No VBA coding required)

## What I Learned
- How to structure an Excel workbook like a business tool  
- How to simulate ERP operations using simple formulas  
- How to balance automation and usability for non-tech-savvy users

## Use Cases
- Small to medium e-commerce businesses 
- WhatsApp / Instagram vendors
- Product-based entrepreneurs
- Freelancers managing client inventories  
- Inventory and order management training

To understand the full project workflow, Excel logic, and business impact, read the article:
[The SmartSheet That Powers a Skincare Brand | The Data Lens](https://medium.com/@sharon_dolapo_johnson/skincare-smart-sheet-automating-retail-operations-with-excel-19a4ffd4a9fc))


