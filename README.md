# 🏢 Warehouse Management & Billing System — Arun Traders

A comprehensive, full-stack **Warehouse Management System (WMS)**, **Billing**, **Inventory**, and **Accounting** application built with React, Node.js, Express, SQLite, and Electron. Designed for high-efficiency wholesale and retail operations with dual-unit support (Boxes & Pieces), dynamic GST calculations, real-time stock tracking, and multi-device access.

---

## 🌟 Key Features

### 🛒 Sales & Billing POS
- **Lightning-Fast Billing**: Optimized keyboard navigation (Enter key unit toggle, Arrow key grid movement).
- **Dual-Unit System**: Support for base units (Pieces) and bulk units (Boxes/Packs) with dynamic price calculation (`Box Rate = Price × Conversion`).
- **Keyboard Shortcuts**:
  - `F4`: Toggle Unit (PCS/BOX)
  - `F5`: Remove Item Row
  - `F7`: Quick Add Item
  - `F8`: Quick Add Customer
  - `F9`: Toggle Free Item
- **Dynamic GST Calculation**: Auto-splits Intra-State (CGST + SGST) and Inter-State (IGST) taxes.
- **Invoice Printing**: Thermal receipt & standard A4 formats.
- **CSV Invoice Import**: Bulk import billing entries directly from CSV files.

### 📦 Inventory & Warehouse Management (WMS)
- **Real-Time Stock Tracking**: Automated stock updates on sales and purchase entries.
- **WMS Selections & Discrepancies**: Manage daily picking selections, item requests, and stock audit discrepancies.
- **Stock Adjustments & Low Stock Alerts**: Instant notifications for items falling below minimum reorder levels.
- **Bulk GST Rate Updates**: Apply GST updates across multiple inventory items simultaneously.

### 💳 Customer Payments & Collections
- **Invoice-Linked Collections**: Track payments against specific invoices or total customer balances.
- **Outstanding Credit Dues**: Real-time customer balance tracking and ledger updates.

### 📊 Trading Reports & Analytics
- **Sales & Purchase Registers**: All, Cash, and Credit filters.
- **Turnover & Location Reports**: Area-wise and Zone-wise sales summaries.
- **Stock Valuation & Reorder Reports**: Live inventory valuation and reorder recommendations.
- **CSV Data Export**: Export reports directly to spreadsheet formats.

---

## 🛠️ Technology Stack

- **Frontend**: React 19, Vite, Lucide Icons, Recharts, Custom CSS (Glassmorphism & High-Contrast Design System).
- **Backend API**: Node.js, Express REST Server.
- **Database**: SQLite (WASM via `sql.js`) with auto-save & automatic schema migrations.
- **Desktop Runtime**: Electron 33.
- **Cloud Deployment**: Render integration via `render.yaml` Blueprint.

---

## 🚀 Quick Start & Installation

### Prerequisites
- Node.js (v18 or higher)
- npm

### 1. Clone the Repository
```bash
git clone https://github.com/Gokul-fullstack/Ware-House-Management.git
cd Ware-House-Management
```

### 2. Install Dependencies
```bash
npm install
```

### 3. Running in Development Mode
To launch the Web Development Server:
```bash
npm run dev
```

To launch the Electron Desktop Application:
```bash
npm run electron:dev
```

### 4. Production Build & Server
To build the frontend and run the standalone Node server:
```bash
npm run build
npm start
```
The server will run on `http://localhost:3456`.

---

## 🌐 Multi-Device & Local Wi-Fi Hosting

You can host the app on a main shop PC and access it from any mobile phone, tablet, or secondary laptop connected to the same Wi-Fi network:

1. Start the server on your primary PC.
2. Find your PC's IP address (`ipconfig` in terminal, e.g., `192.168.1.18`).
3. Open any web browser on your tablet/phone and visit:
   ```text
   http://192.168.1.18:3456
   ```

---

## ☁️ Cloud Deployment (Render)

This repository includes a `render.yaml` configuration for seamless deployment on [Render](https://render.com).

- **Build Command**: `npm install --include=dev && npm run build`
- **Start Command**: `node electron/server.js`
- **Environment**: Node.js

---

## 📝 Default Credentials

- **Username**: `admin`
- **Password**: `admin123`

---

## 📄 License
ISC License — Created for Arun Traders.
