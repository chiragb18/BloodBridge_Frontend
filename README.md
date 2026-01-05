# 🩸 BloodBridge – Blood Bank Management System (Frontend)

BloodBridge is a real-time blood bank management frontend application built with **Angular**.  
It provides role-based dashboards for **Admin**, **Hospital**, and **Donor**, enabling seamless blood requests, approvals, and inventory tracking.

---

## 🚀 Features

### 🏥 Hospital Dashboard
- Request blood units for patients
- View request status (Pending / Approved / Partial / Rejected)
- Real-time updates when admin takes action
- Clean and user-friendly request form

### 🛡️ Admin Dashboard
- View all hospital blood requests in real time
- Approve, partially approve, or reject requests based on inventory
- Manage donor requests
- Visual blood inventory overview
- Role-based secure access

### 🧑‍🤝‍🧑 Donor Dashboard
- Submit blood donation requests
- View donation history
- Track approval status

---

## 🔄 Project Flow

### 1️⃣ Authentication & Role Selection
- User logs in as **Admin**, **Hospital**, or **Donor**
- Dashboard loads based on role

### 2️⃣ Hospital → Admin Flow
- Hospital submits a blood request
- Request instantly appears on Admin Dashboard
- Admin checks inventory
- Admin approves / partially approves / rejects
- Status updates in real time on Hospital Dashboard

### 3️⃣ Donor → Admin Flow
- Donor sends donation request
- Admin approves or rejects
- Approved donations update inventory

### 4️⃣ Inventory Management
- Inventory updates automatically after approvals
- Admin can monitor blood group-wise stock levels

---

## 🧩 Tech Stack

- **Frontend:** Angular (Standalone Components)
- **Styling:** Custom CSS (Dashboard UI)
- **State Management:** RxJS (BehaviorSubject)
- **Storage:** LocalStorage (Mock Persistence)
- **Deployment:** Vercel

---

## 📁 Project Structure

```text
src/
 ├── app/
 │   ├── dashboards/
 │   │   ├── admin-dashboard/
 │   │   ├── hospital-dashboard/
 │   │   └── donor-dashboard/
 │   ├── services/
 │   │   ├── user.service.ts
 │   │   └── blood-request.service.ts
 │   ├── auth/
 │   └── app.routes.ts
 └── assets/

---

⚙️ Setup & Run Locally
git clone https://github.com/<your-username>/bloodbridge-frontend.git
cd bloodbridge-frontend
npm install
ng serve

Open 👉 http://localhost:4200

🌍 Deployment

The project is deployed on Vercel.

https://bloodbridge-frontend.vercel.app
